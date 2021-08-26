---
description: TAPI divide i servizi di comunicazione in Basic, Supplemental ed Extended. Per altre informazioni, vedere Livelli di servizio TAPI.
ms.assetid: e2e6b113-b6b0-43a1-ac95-6e8e188a6120
title: Livelli di servizio TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c72f09f7a076364918815ba5fdb79591f6f5b12382ac2aa529e0859eec53f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012131"
---
# <a name="tspi-levels-of-service"></a>Livelli di servizio TSPI

TAPI divide i servizi di comunicazione in Basic, Supplemental ed Extended. Per altre [informazioni, vedere Livelli di servizio TAPI.](./tapi-levels-of-service.md)

È necessario un provider di servizi di configurazione per implementare tutte le funzioni di telefonia di base. [Funzioni di telefonia di base TSPI](tspi-basic-telephony-functions.md) contiene un riepilogo di queste funzioni.

La telefonia supplementare include funzionalità disponibili nei sistemi PBX moderni, ad esempio blocco, trasferimento, conferenza, parcheggio e così via. Un provider di servizi deve fornire un servizio di telefonia supplementare solo se può implementare il significato esatto definito da TAPI. In caso contrario, la funzionalità deve essere fornita come servizio di telefonia estesa. Tutte le funzionalità supplementari sono facoltative. Un provider di servizi specifica i servizi che supporta tramite risposte a funzioni come [**TSPI \_ lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) o [**TSPI \_ lineGetAddressCaps.**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps) Un singolo servizio supplementare può essere costituito da più chiamate di funzione e messaggi. Telefono i servizi dei dispositivi sono parte della telefonia supplementare.

I servizi di telefonia estesa consentono a un provider di implementare funzioni specifiche del dispositivo. Il provider di servizi deve identificare in modo univoco le estensioni usando un identificatore *di estensione*. Le applicazioni recuperano e usano questo identificatore univoco per determinare le estensioni supportate dal provider di servizi.

Le estensioni possono essere applicate a diversi produttori. Funzioni e messaggi speciali, ad esempio [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) e [**phoneDevSpecific,**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) sono disponibili in TAPI. Vengono usati per consentire l'estensione del set di funzioni (a differenza delle enumerazioni, dei flag di bit e dei membri della struttura dei dati) supportate dal provider di servizi. Anche i parametri per ogni funzione sono definiti dal provider di servizi.

Un identificatore viene assegnato a un set di estensioni (prima della distribuzione), non a ogni singola istanza di un'implementazione di tali estensioni. L'utilità EXTIDGEN in TSPI genera identificatori di estensione univoci per i provider di servizi. Usa un indirizzo della scheda Ethernet, un numero casuale e l'ora del giorno per generare un identificatore, pertanto è estremamente improbabile che l'identificatore di estensione risultante sia in conflitto con qualsiasi altro provider di servizi. Di conseguenza, non è necessario che i fornitori registrino gli identificatori di estensione.

L'utilità EXTIDGEN non genera identificatori di estensione a meno che nel computer in cui viene eseguita non sia in esecuzione anche NetBIOS o altro software di rete.

 

 
