---
description: L'API contiene un meccanismo che consente ai fornitori del provider di servizi di estendere l'API di telefonia usando estensioni specifiche del dispositivo.
ms.assetid: 02749ce5-40db-487e-b51e-e3692266342c
title: Servizi di telefonia estesa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a319f59f51643fb5bf13ec95800d40ffa6d8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311892"
---
# <a name="extended-telephony-services"></a>Servizi di telefonia estesa

L'API contiene un meccanismo che consente ai fornitori del provider di servizi di estendere l'API di telefonia usando estensioni specifiche del dispositivo. I servizi di telefonia estesa (o servizi specifici del dispositivo) includono tutte le estensioni per l'API definita da un particolare provider di servizi. Poiché l'API definisce solo il meccanismo di estensione, è necessario che il provider di servizi specifichi completamente la definizione del comportamento del servizio Extended-Telephony.

## <a name="tapi-2x-extended-telephony"></a>Telefonia estesa TAPI 2. x

Il meccanismo di estensione consente ai fornitori del provider di servizi di definire nuovi valori per alcuni tipi di enumerazione e flag di bit e di aggiungere membri alla maggior parte delle strutture di dati. L'interpretazione delle estensioni è stata disattivata dall'identificatore di estensione del provider di servizi, un identificatore per la specifica del set di estensioni supportate, che può attraversare diversi produttori. Per consentire a un'applicazione di comunicare direttamente con un provider di servizi, sono disponibili funzioni e messaggi speciali, ad esempio [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) e [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) . Il provider di servizi definisce anche i parametri per ogni funzione.

I fornitori non devono effettuare la registrazione per poter assegnare gli identificatori di estensione. Al contrario, un'utilità denominata EXTIDGEN (Extidgen.exe) viene fornita all'interno della piattaforma Software Development Kit (SDK) che consente la generazione locale degli identificatori di estensione. Questo identificatore univoco è costituito da un indirizzo di adapter Ethernet, un numero casuale e l'ora del giorno. Un identificatore viene assegnato a un set di estensioni (prima della distribuzione), non a ogni singola istanza di un'implementazione di tali estensioni.

 

 
