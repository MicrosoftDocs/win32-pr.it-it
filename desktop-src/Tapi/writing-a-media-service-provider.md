---
description: Un provider di servizi multimediali deve implementare un subset minimo di interfacce MSPI ITMSPAddress ITTerminalSupport ITStreamControl e ITStream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Scrittura di un provider di servizi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f99cc8a52b7362caa01d9743fea7fc848faec2ae451b96ec916f4f3aa5c287
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739021"
---
# <a name="writing-a-media-service-provider"></a>Scrittura di un provider di servizi multimediali

Un provider di servizi multimediali deve implementare un subset minimo di interfacce MSPI: [**ITMSPAddress,**](/windows/desktop/api/msp/nn-msp-itmspaddress) [**ITTerminalSupport,**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream). Il supporto di SubStream è facoltativo. Inoltre, un determinato msp può implementare metodi aggiuntivi, ad esempio i controlli necessari per hardware specializzato.

I documenti di materiale seguenti:

-   Le classi di [base DI TAPI 3 MSP,](tapi-3-msp-base-classes.md)che sono un set di classi C++ progettate per semplificare l'attività di compilazione di un msp DirectShow basato su DirectShow. Le classi di base implementano tutte le interfacce MSPI in modo generico. I diversi msp possono eseguire l'override di funzioni specifiche di MSP e fornire implementazioni personalizzate.
-   TapI [3 Terminal Manager,](tapi-3-terminal-manager.md)che fornisce interfacce e metodi usati da un msp per controllare i terminali.
-   [Terminali collegabili](writing-a-pluggable-terminal.md)che consentono a un'applicazione anziché a un msp di creare terminali. Gli sviluppatori che hanno già esperienza nella scrittura di provider di servizi saranno i principali creatori di terminali collegabili. La versione iniziale implementata per questa versione è destinata alle applicazioni server per conferenze che devono aggiungere client non Windows 2000 o non multicast alle conferenze multicast SDP/IP DI TAPI 3.

 

 
