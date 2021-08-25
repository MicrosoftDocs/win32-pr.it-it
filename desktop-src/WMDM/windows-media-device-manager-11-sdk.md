---
title: Windows Media Device Manager 11 SDK
description: Windows Media Device Manager 11 SDK
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Gestione dispositivi multimediali, informazioni su
- Gestione dispositivi, informazioni su
- Media Transfer Protocol (MTP)
- MTP (Media Transfer Protocol)
- Classe Archiviazione di massa (MSC)
- MSC (classe di Archiviazione di massa)
- Windows Gestione dispositivi multimediali, applicazioni desktop
- Gestione dispositivi, applicazioni desktop
- applicazioni desktop, informazioni
- Windows Gestione dispositivi multimediali, provider di servizi
- Gestione dispositivi, provider di servizi
- provider di servizi, informazioni
- Windows Gestione dispositivi multimediali, plug-in
- Gestione dispositivi, plug-insp
- plug-in, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e8b19b035f0210b7928dcc42c19d9519a63fe4eac3e5adaeded780c9d4c729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004811"
---
# <a name="windows-media-device-manager-11-sdk"></a>Windows Media Device Manager 11 SDK

> [!IMPORTANT]
> Le API Windows Gestione dispositivi multimediali sono ora incluse in Windows SDK. Non sono necessari download aggiuntivi dell'SDK.

 

Microsoft Windows Media Device Manager Software Development Kit (SDK) consente di creare applicazioni desktop e componenti in grado di comunicare con dispositivi portatili connessi. Windows Gestione dispositivi multimediali consente all'applicazione o al componente di enumerare, esplorare e scambiare file con un dispositivo, eseguire query sui metadati e richiedere informazioni sul conteggio di riproduzione. Le applicazioni o i componenti creati in Gestione dispositivi multimediali di Windows hanno un'API coerente per la comunicazione con un'ampia gamma di dispositivi, tra cui Media Transfer Protocol (MTP), Mass Archiviazione Class (MSC), RAPI e altri dispositivi compilati sia sulle versioni più recenti che precedenti della tecnologia Windows Media.

È possibile compilare gli elementi seguenti usando l'SDK Windows Media Device Manager:

-   Applicazioni desktop, ad esempio lettori multimediali personalizzati. Tutte le comunicazioni tra un'applicazione e un dispositivo portatile devono essere Windows Gestione dispositivi multimediali, che funge da broker tra l'applicazione, il sistema Microsoft Digital Rights Management e il provider di servizi.
-   Provider di servizi, che fungono da collegamento di comunicazione tra un dispositivo personalizzato e un'applicazione desktop. Anche se Microsoft offre diversi provider di servizi in grado di comunicare con la maggior parte dei dispositivi, è possibile creare un provider di servizi personalizzato per personalizzare la comunicazione tra un dispositivo e un'applicazione desktop.
-   Plug-in, che possono eseguire attività come la richiesta e la registrazione dei conteggi di riproduzione nei dispositivi. Questi plug-in possono essere collegati ad altre applicazioni desktop, ad esempio il Windows Media Player per inviare informazioni ai provider di contenuti per gestire i pagamenti delle royalty agli artisti.

Per scaricare l'SDK Windows Media Device Manager, vedere la pagina [Windows Media Download](https://msdn.microsoft.com/windows/desktop/aa904949) nel sito Web MSDN.

Questo SDK è un componente di Microsoft Windows Media Software Development Kit. Altri componenti includono Windows Media Format SDK, Servizi Windows Media SDK, Windows Media Encoder SDK, Windows Media Rights Manager SDK e Windows Media Player SDK.

Questa documentazione include le sezioni seguenti.



| Sezione                                            | Descrizione                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Per iniziare](getting-started.md)             | Descrive le novità di questa versione di gestione dispositivi multimediali di Windows, offre una panoramica del funzionamento di Gestione dispositivi multimediali di Windows, descrive cosa sarà necessario per sviluppare un'applicazione o un provider di servizi e illustra gli esempi forniti con l'SDK. |
| [Guida per programmatori](programming-guide.md)         | Viene illustrato come compilare applicazioni e provider di servizi.                                                                                                                                                                                                      |
| [Guida di riferimento alla programmazione](programming-reference.md) | Fornisce informazioni di riferimento su C++ per le interfacce, i metodi, le classi e le strutture supportate da Windows Media Device Manager SDK.                                                                                                                      |
| [*Glossario*](wmdm-glossary.md)                    | Definisce i termini usati in questa documentazione.                                                                                                                                                                                                                       |



 

 

 




