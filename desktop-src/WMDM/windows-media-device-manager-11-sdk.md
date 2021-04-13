---
title: Windows Media Gestione dispositivi 11 SDK
description: Windows Media Gestione dispositivi 11 SDK
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Media Gestione dispositivi, informazioni
- Gestione dispositivi, informazioni
- Protocollo MTP (Media Transfer Protocol)
- MTP (Media Transfer Protocol)
- Classe di archiviazione di massa (MSC)
- MSC (classe di archiviazione di massa)
- Windows Media Gestione dispositivi, applicazioni desktop
- Gestione dispositivi, applicazioni desktop
- applicazioni desktop, informazioni
- Windows Media Gestione dispositivi, provider di servizi
- Gestione dispositivi, provider di servizi
- provider di servizi, informazioni
- Windows Media Gestione dispositivi, plug-in
- Gestione dispositivi, plug-Insp
- plug-in, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399855"
---
# <a name="windows-media-device-manager-11-sdk"></a>Windows Media Gestione dispositivi 11 SDK

> [!IMPORTANT]
> Le API di Windows Media Gestione dispositivi sono ora incluse nel Windows SDK. Non sono necessari download aggiuntivi dell'SDK.

 

Microsoft Windows Media Gestione dispositivi Software Development Kit (SDK) consente di creare applicazioni desktop e componenti in grado di comunicare con i dispositivi portatili connessi. Windows Media Gestione dispositivi consente all'applicazione o al componente di enumerare, esplorare ed effettuare lo scambio di file con un dispositivo, eseguire query per i metadati e richiedere informazioni sui conteggi di riproduzione. Le applicazioni o i componenti basati su Windows Media Gestione dispositivi hanno un'API coerente per la comunicazione con un'ampia gamma di dispositivi, tra cui il protocollo MTP (Media Transfer Protocol), la classe di archiviazione di massa (MSC), RAPI e altri dispositivi basati sulle versioni più recenti e precedenti della tecnologia Windows Media.

È possibile compilare gli elementi seguenti utilizzando Windows Media Gestione dispositivi SDK:

-   Applicazioni desktop, ad esempio lettori multimediali personalizzati. Tutte le comunicazioni tra un'applicazione e un dispositivo portatile devono passare attraverso Windows Media Gestione dispositivi, che funge da broker tra l'applicazione, il sistema Microsoft Digital Rights Management e il provider di servizi.
-   Provider di servizi, che fungono da collegamento di comunicazione tra un dispositivo personalizzato e un'applicazione desktop. Sebbene Microsoft fornisca diversi provider di servizi in grado di comunicare con la maggior parte dei dispositivi, è possibile creare un provider di servizi personalizzato per personalizzare la comunicazione tra un dispositivo e un'applicazione desktop.
-   Plug-in, che possono eseguire attività quali la richiesta e la registrazione dei conteggi dei Play nei dispositivi. Questi plug-in possono essere collegati ad altre applicazioni desktop, ad esempio Windows Media Player per inviare informazioni ai provider di contenuti per gestire i pagamenti di Royalty agli artisti.

Per scaricare Windows Media Gestione dispositivi SDK, vedere [la pagina di download di Windows Media](https://msdn.microsoft.com/windows/desktop/aa904949) sul sito Web MSDN.

Questo SDK è un componente di Microsoft Windows Media Software Development Kit. Altri componenti includono Windows Media Format SDK, Windows Media Services SDK, Windows Media Encoder SDK, Windows Media Rights Manager SDK e Windows Media Player SDK.

Questa documentazione include le sezioni seguenti.



| Sezione                                            | Descrizione                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Per iniziare](getting-started.md)             | Descrive le novità di questa versione di Windows Media Gestione dispositivi, offre una panoramica del funzionamento di Windows Media Gestione dispositivi, descrive gli elementi necessari per lo sviluppo di un'applicazione o un provider di servizi e illustra gli esempi forniti con l'SDK. |
| [Guida per programmatori](programming-guide.md)         | Viene illustrato come compilare applicazioni e provider di servizi.                                                                                                                                                                                                      |
| [Guida di riferimento alla programmazione](programming-reference.md) | Fornisce informazioni di riferimento su C++ per le interfacce, i metodi, le classi e le strutture supportate da Windows Media Gestione dispositivi SDK.                                                                                                                      |
| [*Glossario*](wmdm-glossary.md)                    | Definisce i termini usati in questa documentazione.                                                                                                                                                                                                                       |



 

 

 




