---
title: Glossario del file System proiettato di Windows
description: Termini speciali usati in ProjFS.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: a48b68a75323edfb902eb04fbe6d0ecba6988c21
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/21/2020
ms.locfileid: "106299477"
---
# <a name="windows-projected-file-system-glossary"></a>Glossario del file System proiettato di Windows

Termini speciali usati in ProjFS.

<dl>
<dt>

<span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**Archivio di backup**
</dt>
<dd>

Dati gerarchici gestiti dal provider proiettati nella file system come file e directory.
</dd>

<dt>

<span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**segnaposto Dirty**
</dt>
<dd>

Un file o una directory che è stata modificata localmente e non è più una cache dello stato nell'archivio del provider.  Vedere [lo stato della cache nella radice di virtualizzazione](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**file/directory completa**
</dt>
<dd>

Un file o una directory creata nel file system locale o un file che è stato modificato, rendendolo non più una cache dello stato nell'archivio di backup.  Vedere [lo stato della cache nella radice di virtualizzazione](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**segnaposto idrato**
</dt>
<dd>

File il cui contenuto e metadati sono stati memorizzati nella cache su disco.  Vedere [lo stato della cache nella radice di virtualizzazione](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**segnaposto**
</dt>
<dd>

Un file o una directory che non è completamente presente su disco.  Vedere [lo stato della cache nella radice di virtualizzazione](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**rimozione definitiva**
</dt>
<dd>

Segnaposto nascosto speciale che rappresenta un elemento eliminato dalla file system locale.  Vedere [lo stato della cache nella radice di virtualizzazione](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**file/directory virtuale**
</dt>
<dd>

Un file o una directory che non esiste fisicamente sul disco, ma viene proiettata in risultati di enumerazione.  Vedere [lo stato della cache nella radice di virtualizzazione](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**istanza di virtualizzazione**
</dt>
<dd>

Oggetto in memoria che gestisce la comunicazione tra il provider e ProjFS per il set di file e directory che si trovano in una particolare radice di virtualizzazione.
</dd>

<dt>

<span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**radice di virtualizzazione**
</dt>
<dd>

Una directory nella file system in cui vengono proiettati i dati del provider.
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