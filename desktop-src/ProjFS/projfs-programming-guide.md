---
title: Guida alla programmazione del file System proiettato
description: Informazioni concettuali sull'implementazione di un'applicazione del provider ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: a6b2d186ac3e674c3fa68e17ecd523b2c94f2401
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047061"
---
# <a name="projected-file-system-projfs-programming-guide"></a>Guida alla programmazione del file System proiettato (ProjFS)

Il file System proiettato da Windows (ProjFS) consente a un'applicazione in modalità utente denominata "provider" di proiettare i dati gerarchici nella file system, facendoli apparire come file e directory nel file system.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento                                                                                                       | Descrizione |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Panoramica del provider](provider-overview.md)                                                                   | Panoramica concettuale di un'applicazione provider.
| [Stato della cache nella radice di virtualizzazione](cache-state.md)                                                    | Descrive i diversi Stati della cache che un file o una directory gestita dal provider può avere. 
| [Abilitazione del file System proiettato di Windows](enabling-windows-projected-file-system.md)                         | Viene descritto come abilitare il componente facoltativo ProjFS.
| [Ciclo di vita dell'istanza di virtualizzazione](virtualization-instance-lifecycle.md)                                   | Panoramica del ciclo di vita di un'istanza di virtualizzazione ProjFS.
| [Enumerazione di file e directory](enumerating-files-and-directories.md)                                   | Viene descritto il modo in cui un provider ProjFS partecipa all'enumerazione di directory.
| [Fornire dati di file](providing-file-data.md)                                                               | Descrive il modo in cui un provider fornisce informazioni sui segnaposto e i dati dei file.
| [Notifiche delle operazioni del file System](file-system-operation-notifications.md)                               | Viene descritto come un provider può ricevere notifiche di file system operazioni.
| [Gestione delle modifiche della visualizzazione](handling-view-changes.md)                                                           | Viene descritto come aggiornare la visualizzazione client dell'archivio di backup di un provider.
| [Gestione asincrona del callback](asynchronous-callback-handling.md)                                         | Viene descritto in che modo il provider è in grado di servire in modo asincrono i callback.
| [Riferimento all'API del file System proiettato di Windows](/windows/desktop/api/_projfs) | Informazioni di riferimento per l'interfaccia di programmazione ProjFS.

## <a name="additional-resources"></a>Risorse aggiuntive

|                                                                                                              |                                                                                   |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Esempio RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Un provider ProjFS di esempio che proietta il registro di sistema di Windows nell'file system. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->