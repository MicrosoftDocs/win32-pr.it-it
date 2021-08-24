---
title: Windows Glossario del file system proiettato
description: Termini speciali usati in ProjFS.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 12b6e90d98fce3882aa5dc8d552f88e9cd9f389d24673fdc5caf175e180082f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030984"
---
# <a name="windows-projected-file-system-glossary"></a>Windows Glossario del file system proiettato

Termini speciali usati in ProjFS.

<dl>
<dt>

<span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**archivio di backup**
</dt>
<dd>

I dati gerarchici gestiti dal provider che vengono proiettati nel file system come file e directory.
</dd>

<dt>

<span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**Segnaposto dirty**
</dt>
<dd>

Un file o una directory che è stata modificata localmente e non è più una cache del relativo stato nell'archivio del provider.  Vedere [Cache State (Stato della cache) in Virtualization Root (Radice di virtualizzazione).](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**file/directory completo**
</dt>
<dd>

Un file o una directory creata nel file system locale o un file che è stato modificato, rendendo non più una cache del relativo stato nell'archivio di backup.  Vedere [Cache State (Stato della cache) in Virtualization Root (Radice di virtualizzazione).](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**segnaposto indossato**
</dt>
<dd>

File i cui contenuti e metadati sono stati memorizzati nella cache su disco.  Vedere [Cache State (Stato della cache) in Virtualization Root (Radice di virtualizzazione).](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**Segnaposto**
</dt>
<dd>

File o directory non completamente presente sul disco.  Vedere [Cache State (Stato della cache) in Virtualization Root (Radice di virtualizzazione).](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**Tombstone**
</dt>
<dd>

Segnaposto nascosto speciale che rappresenta un elemento eliminato dal file system.  Vedere [Cache State (Stato della cache) in Virtualization Root (Radice di virtualizzazione).](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**file/directory virtuale**
</dt>
<dd>

File o directory che non esiste fisicamente su disco, ma che viene proiettato nei risultati dell'enumerazione.  Vedere [Cache State (Stato della cache) in Virtualization Root (Radice di virtualizzazione).](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**istanza di virtualizzazione**
</dt>
<dd>

Oggetto in memoria che gestisce la comunicazione tra il provider e ProjFS per il set di file e directory che si trovano in una determinata radice di virtualizzazione.
</dd>

<dt>

<span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**radice di virtualizzazione**
</dt>
<dd>

Una directory nel file system in cui vengono proiettati i dati del provider.
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->