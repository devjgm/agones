# Copyright 2019 Google LLC All Rights Reserved.
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

FROM alpine:3.11

RUN apk --update add ca-certificates && \
    adduser -D agones

COPY --chown=agones:root ./bin/allocator /home/agones/allocator
COPY --chown=agones:root ./bin/LICENSES ./bin/dependencies-src.tgz /home/agones/

USER agones
ENTRYPOINT ["/home/agones/allocator"]
