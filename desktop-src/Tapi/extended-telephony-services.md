---
description: L'API contiene un meccanismo che consente ai fornitori di provider di servizi di estendere l'API di telefonia usando estensioni specifiche del dispositivo.
ms.assetid: 02749ce5-40db-487e-b51e-e3692266342c
title: Servizi di telefonia estesa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403f57904138b3797069222875086b0a4990b8e625f701f380120d65c235784e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140704"
---
# <a name="extended-telephony-services"></a>Servizi di telefonia estesa

L'API contiene un meccanismo che consente ai fornitori di provider di servizi di estendere l'API di telefonia usando estensioni specifiche del dispositivo. I servizi di telefonia estesa (o servizi specifici del dispositivo) includono tutte le estensioni all'API definita da un provider di servizi specifico. Poiché l'API definisce solo il meccanismo di estensione, il provider di servizi deve specificare completamente la definizione del Extended-Telephony del servizio.

## <a name="tapi-2x-extended-telephony"></a>Telefonia estesa TAPI 2.x

Il meccanismo di estensione consente ai fornitori di provider di servizi di definire nuovi valori per alcuni tipi di enumerazione e flag di bit e di aggiungere membri alla maggior parte delle strutture di dati. L'interpretazione delle estensioni è indicata dall'identificatore di estensione del provider di servizi, un identificatore per la specifica del set di estensioni supportate, che può attraversare diversi produttori. Nell'API vengono forniti messaggi e funzioni speciali, ad esempio [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) e [**phoneDevSpecific,**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) per consentire a un'applicazione di comunicare direttamente con un provider di servizi. Il provider di servizi definisce anche i parametri per ogni funzione.

I fornitori non devono eseguire la registrazione per poter assegnare gli identificatori di estensione. Viene invece fornita un'utilità denominata EXTIDGEN (Extidgen.exe) all'interno di Platform Software Development Kit (SDK) che consente la generazione locale di identificatori di estensione. Questo identificatore univoco è composto da un indirizzo della scheda Ethernet, un numero casuale e l'ora del giorno. Un identificatore viene assegnato a un set di estensioni (prima della distribuzione), non a ogni singola istanza di un'implementazione di tali estensioni.

 

 
