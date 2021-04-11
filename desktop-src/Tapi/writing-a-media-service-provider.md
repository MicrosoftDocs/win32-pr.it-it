---
description: Un provider di servizi multimediali deve implementare un subset minimo di interfacce MSPI ITMSPAddress ITTerminalSupport ITStreamControl e ITStream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Scrittura di un provider di servizi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782dddb9a87725bde7c104d459b71204a04de018
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351166"
---
# <a name="writing-a-media-service-provider"></a>Scrittura di un provider di servizi multimediali

Un provider di servizi multimediali deve implementare un subset minimo di interfacce MSPI: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream). Il supporto del sottoflusso è facoltativo. Inoltre, un determinato MSP può implementare metodi aggiuntivi, ad esempio i controlli necessari per l'hardware specializzato.

I documenti materiali seguenti:

-   Le [classi di base msp di TAPI 3](tapi-3-msp-base-classes.md), ovvero un set di classi C++ progettate per semplificare l'attività di compilazione di un MSP basato su DirectShow. Le classi base implementano tutte le interfacce MSPI in modo generico. MSPs differenti possono eseguire l'override di funzioni specifiche di MSP e fornire le proprie implementazioni.
-   [TAPI 3 Terminal Manager](tapi-3-terminal-manager.md), che fornisce interfacce e metodi usati da un MSP per il controllo dei terminali.
-   [Terminali collegabili](writing-a-pluggable-terminal.md), che consentono a un'applicazione anziché a un MSP di creare terminali. Gli sviluppatori che hanno già sperimentato la scrittura di provider di servizi saranno gli autori principali dei terminali collegabili. La versione iniziale implementata per questa versione è destinata alle applicazioni server di conferenza che devono aggiungere client non Windows 2000 o non multicast alle conferenze multicast SDP/IP multiparte di TAPI 3.

 

 
