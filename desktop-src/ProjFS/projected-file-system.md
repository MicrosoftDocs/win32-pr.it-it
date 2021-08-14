---
title: Windows File system proiettato
description: Panoramica del Windows file system proiettato (ProjFS)
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: d5cb20b123e72ec8e031036019a16ef1bbe2b8dc4b9bb53446c8faaced4d796b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792658"
---
# <a name="windows-projected-file-system-projfs"></a>Windows File system proiettato (ProjFS)

Il Windows Projected File System (ProjFS) consente a un'applicazione in modalità utente denominata "provider" di proiettare dati gerarchici da un archivio dati di backup nel file system, rendendoli visualizzati come file e directory nel file system. Ad esempio, un provider semplice potrebbe proiettare il registro Windows nel file system, facendo in modo che le chiavi e i valori del Registro di sistema vengano visualizzati rispettivamente come file e directory. Un esempio di provider più complesso è [VFS per Git,](https://github.com/Microsoft/VFSForGit)usato per virtualizzare repository Git di dimensioni molto grandi.

> [!NOTE]
> ProjFS è progettato per l'uso con archivi dati di backup ad alta velocità. Uno degli obiettivi di progettazione è far apparire i dati proiettati come se fossero presenti in locale, nascondendo il fatto che i dati potrebbero essere remoti. Di conseguenza, ProjFS non fornisce: meccanismi per segnalare lo stato di avanzamento del richiamo dei dati; indicazione dello stato online e offline di un file; né altre funzionalità che possono risultare utili quando si lavora con archivi dati di backup lenti. Per questi scenari, prendere in considerazione l'uso [dell'API File cloud](../cfapi/cloud-files-api-portal.md).

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento                                                                                                       | Descrizione |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Windows Guida per programmatori del file system proiettato](projfs-programming-guide.md)                              | Informazioni concettuali sull'implementazione di un'applicazione provider ProjFS.
| [Windows Informazioni di riferimento sulle API del file system proiettate](projfs-reference.md)                                          | Informazioni di riferimento per l'interfaccia di programmazione ProjFS.
| [Windows Glossario del file system proiettato](projfs-glossary.md)                                                | Termini speciali usati in ProjFS.

## <a name="additional-resources"></a>Risorse aggiuntive

| Argomento                                                                                                             | Descrizione                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Esempio di RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Provider ProjFS di esempio che proietta il Windows di sistema nel file system. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->