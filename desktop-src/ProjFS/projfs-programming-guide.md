---
title: Guida per programmatori del file system proiettato
description: Informazioni concettuali sull'implementazione di un'applicazione provider ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: d935c99b73e11a2110e739a4e45fdde0f7a24300a2664a2b25d6217bd2235fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792544"
---
# <a name="projected-file-system-projfs-programming-guide"></a>Guida alla programmazione del file system proiettato (ProjFS)

Il Windows Projected File System (ProjFS) consente a un'applicazione in modalità utente denominata "provider" di proiettare dati gerarchici nel file system, rendendoli visualizzati come file e directory nel file system.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento                                                                                                       | Descrizione |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Panoramica del provider](provider-overview.md)                                                                   | Panoramica concettuale di un'applicazione provider.
| [Stato della cache nella radice di virtualizzazione](cache-state.md)                                                    | Descrive i diversi stati della cache che possono avere un file o una directory gestita dal provider. 
| [Abilitazione Windows file system proiettato](enabling-windows-projected-file-system.md)                         | Viene descritto come abilitare il componente facoltativo ProjFS.
| [Ciclo di vita dell'istanza di virtualizzazione](virtualization-instance-lifecycle.md)                                   | Panoramica del ciclo di vita di un'istanza di virtualizzazione ProjFS.
| [Enumerazione di file e directory](enumerating-files-and-directories.md)                                   | Viene descritto il modo in cui un provider ProjFS partecipa all'enumerazione della directory.
| [Fornire dati di file](providing-file-data.md)                                                               | Descrive come un provider fornisce informazioni segnaposto e dati di file.
| [Notifiche delle operazioni del file system](file-system-operation-notifications.md)                               | Viene descritto come un provider può ricevere notifiche di file system operazioni.
| [Gestione delle modifiche della visualizzazione](handling-view-changes.md)                                                           | Viene descritto come aggiornare la visualizzazione client dell'archivio di backup di un provider.
| [Gestione dei callback asincroni](asynchronous-callback-handling.md)                                         | Viene descritto come il provider può eseguire in modo asincrono i callback del servizio.
| [Windows Informazioni di riferimento sulle API del file system proiettato](/windows/desktop/api/_projfs) | Informazioni di riferimento per l'interfaccia di programmazione ProjFS.

## <a name="additional-resources"></a>Risorse aggiuntive

| Argomento                                                                                                             | Descrizione                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Esempio di RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Provider ProjFS di esempio che proietta il registro Windows nel file system. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->