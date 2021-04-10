---
description: Una coda di chiamata o un punto di route è un indirizzo speciale all'interno dell'opzione in cui le chiamate sono temporaneamente mantenute in sospeso.
ms.assetid: 1c801401-be05-4b5f-bc4f-628dde0f3cf7
title: Code di chiamata e punti di route
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66895101b72ca8e16810d3766edf897efcfedddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227366"
---
# <a name="call-queues-and-route-points"></a>Code di chiamata e punti di route

Una coda di chiamata o un punto di route è un indirizzo speciale all'interno dell'opzione in cui le chiamate sono temporaneamente mantenute in sospeso. Questa caratteristica è rappresentata dalla coda LINEADDRCAPFLAGS bits \_ e da LINEADDRCAPFLAGS \_ punto rotta nel membro **dwAddrCapFlags** in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps). Tutte le chiamate visualizzate su tale indirizzo sono in attesa di azione da parte dell'applicazione e possono essere eseguite azioni predefinite, ad esempio il trasferimento a un agente o un trunk, se l'applicazione non esegue alcuna azione entro un periodo di tempo definito. L'applicazione deve essere configurata dall'amministratore di sistema in modo da sapere quali azioni devono essere eseguite in relazione a ogni indirizzo di coda o punto di route e la quantità di tempo disponibile per decidere l'azione da intraprendere.

Le applicazioni possono determinare il numero di chiamate in sospeso in una coda o in un punto di route usando [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus). La funzione [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) può essere utilizzata per ottenere informazioni quali l'ID chiamante, l'ID, l'origine in ingresso o in uscita e così via, e utilizzate dall'applicazione per prendere decisioni sulla gestione delle chiamate; le chiamate possono essere reindirizzate, trasferite in modo cieco, eliminate e così via o semplicemente consentite per passare automaticamente dalla coda a una destinazione. Una chiamata passa a LINECALLSTATE \_ disconnessa se viene abbandonata. Le chiamate diventano *inattive* quando lasciano la coda; **lineGetCallInfo** può essere usato per leggere l'identificatore di reindirizzamento per determinare la posizione in cui sono stati trasferiti.

Alcuni commutatori consentono chiamate in una coda o in attesa per ricevere un particolare trattamento, ad esempio il silenzio, la riponderia, il segnale occupato, la musica o l'ascolto di un annuncio registrato. La funzione [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) consente all'applicazione di controllare il trattamento. La struttura delimitata dai membri **dwCallTreatmentListSize** e **dwCallTreatmentListOffset** in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) consente alle applicazioni di determinare i trattamenti supportati. Il membro **dwCallTreatment** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) indica il trattamento corrente e un messaggio di [**riga \_ CALLINFO**](line-callinfo.md) con il \_ trattamento LINECALLINFOSTATE indica quando questo viene modificato. Il bit del LINECALLFEATURE di degestione del \_ membro **DwCallFeatures** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) indica quando l'applicazione è autorizzata a modificare il trattamento. Il \_ set di costanti LINECALLTREATMENT definisce un set limitato di trattamenti di chiamata predefiniti. i provider di servizi possono definire molti più.

 

 



