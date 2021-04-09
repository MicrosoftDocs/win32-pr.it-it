---
title: Uso di IMAPi
description: Negli argomenti seguenti viene illustrato l'utilizzo dell'API per la creazione di immagini master.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccd44d01e925d07d251e93a29c5268cc7e9c5076
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856949"
---
# <a name="using-imapi"></a>Uso di IMAPi

Negli argomenti seguenti viene illustrato l'utilizzo dell'API per la creazione di immagini master.

## <a name="usage-scenarios"></a>Scenari di utilizzo

La documentazione seguente fornisce indicazioni dettagliate per gli scenari IMAP comuni.



| Scenario                                                                                                         | Descrizione                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Verifica del supporto delle unità](checking-drive-support.md)                                                             | Viene illustrato il rilevamento del supporto per un'unità multimediale.<br/>                                                                                                   |
| [Verifica del supporto multimediale](checking-media-support.md)                                                             | Viene illustrato il rilevamento del supporto per i supporti.<br/>                                                                                                           |
| [Masterizzazione di un'immagine del disco](burning-a-disc.md)                                                                       | Viene illustrata la masterizzazione di un disco utilizzando IMAPi.<br/>                                                                                                       |
| [Aggiunta di un'immagine di avvio](adding-a-boot-image.md)                                                                   | Si basa sull'esempio di [masterizzazione di un'immagine del disco](burning-a-disc.md) aggiungendo codice per includere un'immagine di avvio nella sezione di avvio del disco.<br/>               |
| [Creazione di un disco multisessione](creating-a-multisession-disc.md)                                                 | Viene illustrata la creazione di un disco multisessione con IMAPi.<br/>                                                                                              |
| [Monitoraggio dello stato di avanzamento con gli eventi](monitoring-progress-with-events.md)                                           | Viene illustrato l'utilizzo di interfacce specifiche per consentire l'implementazione di un gestore eventi in modo che sia possibile ricevere informazioni sullo stato di avanzamento. <br/>        |
| [Prevenzione della disconnessione o della sospensione durante un'ustione](preventing-logoff-or-suspend-during-a-burn.md)                     | Contiene informazioni che descrivono in dettaglio le considerazioni relative allo sviluppo di applicazioni per quanto riguarda gli scenari che coinvolgono l'utente ' disconnessione ' è suspend ' in Windows.<br/> |
| [Fornire le autorizzazioni utente per i dispositivi con masterizzazione multimediale](providing-user-permissions-for-media-burning-devices.md) | Descrive il processo necessario per verificare che un utente disponga di autorizzazioni adeguate per l'utilizzo di dispositivi con masterizzazione multimediale in Windows XP e Windows Server 2003.<br/>             |



 

## <a name="application-compatibility"></a>Compatibilità delle applicazioni

La documentazione seguente contiene informazioni importanti da tenere in considerazione durante lo sviluppo di un'applicazione che usa IMAPi.



| Informazioni aggiuntive                                                   | Descrizione                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Layout multisessione IMAPi](imapi-multisession-layout.md) | Descrive il layout del disco usato da IMAPi per implementare la multisessione. Queste informazioni vengono utilizzate per garantire l'interoperabilità tra IMAPi e altri software di masterizzazione, oltre a consentire la creazione di immagini di dischi multisessione compatibili con IMAP.<br/> |



 

 

 





