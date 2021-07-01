---
title: Guida alla programmazione del file system proiettato
description: Informazioni concettuali sull'implementazione di un'applicazione provider ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 86c6f49eaf9da578226031eaf84abff7ebb059c0
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120566"
---
# <a name="projected-file-system-projfs-programming-guide"></a>Guida alla programmazione del file system proiettato (ProjFS)

Windows Projected File System (ProjFS) consente a un'applicazione in modalità utente denominata "provider" di proiettare i dati gerarchici nel file system, rendendoli visualizzati come file e directory nel file system.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento                                                                                                       | Descrizione |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Panoramica del provider](provider-overview.md)                                                                   | Panoramica concettuale di un'applicazione provider.
| [Stato della cache nella radice di virtualizzazione](cache-state.md)                                                    | Descrive i diversi stati della cache che possono avere un file o una directory gestita dal provider. 
| [Abilitazione del file system proiettato di Windows](enabling-windows-projected-file-system.md)                         | Viene descritto come abilitare il componente facoltativo ProjFS.
| [Ciclo di vita dell'istanza di virtualizzazione](virtualization-instance-lifecycle.md)                                   | Panoramica del ciclo di vita di un'istanza di virtualizzazione ProjFS.
| [Enumerazione di file e directory](enumerating-files-and-directories.md)                                   | Viene descritto il modo in cui un provider ProjFS partecipa all'enumerazione delle directory.
| [Fornire dati di file](providing-file-data.md)                                                               | Descrive il modo in cui un provider fornisce informazioni segnaposto e dati di file.
| [Notifiche delle operazioni del file system](file-system-operation-notifications.md)                               | Viene descritto in che modo un provider può ricevere notifiche file system operazioni.
| [Gestione delle modifiche delle visualizzazione](handling-view-changes.md)                                                           | Viene descritto come aggiornare la visualizzazione client dell'archivio di backup di un provider.
| [Gestione dei callback asincroni](asynchronous-callback-handling.md)                                         | Viene descritto come il provider può eseguire in modo asincrono i callback.
| [Informazioni di riferimento sulle API del file system proiettato di Windows](/windows/desktop/api/_projfs) | Informazioni di riferimento per l'interfaccia di programmazione ProjFS.

## <a name="additional-resources"></a>Risorse aggiuntive

| Argomento                                                                                                             | Descrizione                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Esempio di RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Provider ProjFS di esempio che proietta il Registro di sistema di Windows nel file system. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->