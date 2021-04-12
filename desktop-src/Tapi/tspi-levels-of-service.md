---
description: TAPI divide i servizi di comunicazione in base, supplementare ed esteso. Per ulteriori informazioni, vedere livelli di servizio TAPI.
ms.assetid: e2e6b113-b6b0-43a1-ac95-6e8e188a6120
title: Livelli di servizio TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d829199bdcfce350d82f3c56cbbf9414fc46b35b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529209"
---
# <a name="tspi-levels-of-service"></a>Livelli di servizio TSPI

TAPI divide i servizi di comunicazione in base, supplementare ed esteso. Per ulteriori informazioni, vedere [livelli di servizio TAPI](./tapi-levels-of-service.md) .

Per implementare tutte le funzioni di telefonia di base, è necessario un TSP. Le [funzioni di telefonia Basic TSPI](tspi-basic-telephony-functions.md) contengono un riepilogo di queste funzioni.

La telefonia supplementare include le funzionalità disponibili nei PBX moderni, ad esempio l'attesa, il trasferimento, la conferenza, il parco e così via. Un provider di servizi deve fornire un servizio di telefonia supplementare solo se può implementare il significato esatto definito da TAPI. In caso contrario, la funzionalità deve essere fornita come servizio di telefonia estesa. Tutte le funzionalità supplementari sono facoltative. Un provider di servizi specifica i servizi supportati tramite risposte a funzioni quali [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) o [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps). Un singolo servizio supplementare può essere costituito da più chiamate di funzione e messaggi. I servizi del dispositivo telefonico fanno parte della telefonia supplementare.

I servizi di telefonia estesa consentono a un provider di implementare funzioni specifiche del dispositivo. Il provider di servizi deve identificare in modo univoco le estensioni usando un *identificatore di estensione*. Le applicazioni recuperano e usano questo identificatore univoco per determinare le estensioni supportate dal provider di servizi.

Le estensioni possono essere applicate a diversi produttori. In TAPI sono disponibili funzioni e messaggi speciali, ad esempio [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) e [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) . Vengono utilizzati per consentire l'estensione del set di funzioni (a differenza delle enumerazioni, dei flag di bit e dei membri della struttura di dati) supportati dal provider di servizi. I parametri per ogni funzione sono definiti anche dal provider di servizi.

Un identificatore viene assegnato a un set di estensioni (prima della distribuzione), non a ogni singola istanza di un'implementazione di tali estensioni. L'utilità EXTIDGEN in TSPI genera identificatori di estensione univoci per i provider di servizi. Usa un indirizzo di adapter Ethernet, un numero casuale e l'ora del giorno per generare un identificatore, quindi è estremamente improbabile che l'identificatore dell'estensione risultante sia in conflitto con qualsiasi altro provider di servizi. Di conseguenza, non è necessario che i fornitori registrino gli identificatori di estensione.

L'utilità EXTIDGEN non genera identificatori di estensione, a meno che il computer in cui è in esecuzione esegua anche NetBIOS o altro software di rete.

 

 
