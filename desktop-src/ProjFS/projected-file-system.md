---
title: File System proiettato di Windows
description: Panoramica del file System proiettato di Windows (ProjFS)
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: 8391ec63f23c9ebae5b47e4cac862f6ab3079ceb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872602"
---
# <a name="windows-projected-file-system-projfs"></a>File System proiettato di Windows (ProjFS)

Il file System proiettato da Windows (ProjFS) consente a un'applicazione in modalità utente denominata "provider" di proiettare i dati gerarchici da un archivio dati di supporto nel file system, facendolo apparire come file e directory nel file system. Un provider semplice può, ad esempio, proiettare il registro di sistema di Windows nel file system, rendendo le chiavi e i valori del registro di sistema visualizzati rispettivamente come file e directory. Un esempio di provider più complesso è [VFS per git](https://github.com/Microsoft/VFSForGit), usato per la virtualizzazione di repository git di grandi dimensioni.

> [!NOTE]
> ProjFS è progettato per l'uso con archivi dati di supporto ad alta velocità. Uno degli obiettivi di progettazione consiste nel far apparire i dati proiettati come se fossero presenti localmente, nascondendo il fatto che i dati potrebbero essere remoti. Di conseguenza, ProjFS non fornisce: meccanismi per la segnalazione dello stato di avanzamento del richiamo dei dati; indicazione dello stato online rispetto alla modalità offline di un file; non sono disponibili altre funzionalità che possono risultare utili quando si utilizzano archivi dati di backup lenti. Per questi scenari, è consigliabile usare invece l' [API file Cloud](../cfapi/cloud-files-api-portal.md).

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento                                                                                                       | Descrizione |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Guida alla programmazione del file System di Windows](projfs-programming-guide.md)                              | Informazioni concettuali sull'implementazione di un'applicazione del provider ProjFS.
| [Riferimento all'API del file System proiettato di Windows](projfs-reference.md)                                          | Informazioni di riferimento per l'interfaccia di programmazione ProjFS.
| [Glossario del file System proiettato di Windows](projfs-glossary.md)                                                | Termini speciali usati in ProjFS.

## <a name="additional-resources"></a>Risorse aggiuntive

|                                                                                                              |                                                                                   |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Esempio RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Un provider ProjFS di esempio che proietta il registro di sistema di Windows nell'file system. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->