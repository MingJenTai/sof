# SPDX-License-Identifier: BSD-3-Clause

if(CONFIG_BAYTRAIL OR CONFIG_CHERRYTRAIL)
	add_local_sources(sof pmc-ipc.c)
	add_subdirectory(baytrail)
elseif(CONFIG_HASWELL OR CONFIG_BROADWELL)
	add_subdirectory(haswell)
elseif(CONFIG_CAVS)
	add_subdirectory(cavs)
endif()
