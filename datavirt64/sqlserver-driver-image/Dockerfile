# Copyright 2016 Red Hat
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
# ------------------------------------------------------------------------
#
# This is a Dockerfile for a Microsoft SQL Server JDBC driver add-on for EAP.

FROM scratch

# Labels
LABEL name="Microsoft SQL Server JDBC Driver" \
      version="6.4.0"

# Copy add-on details
COPY install.sh \
     install.properties \
     /extensions/
COPY modules /extensions/modules/

# Download the driver into the module folder
ADD http://central.maven.org/maven2/com/microsoft/sqlserver/mssql-jdbc/6.4.0.jre8/mssql-jdbc-6.4.0.jre8.jar \
    /extensions/modules/system/layers/openshift/com/microsoft/mssql/main/
