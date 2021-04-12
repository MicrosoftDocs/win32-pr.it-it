---
description: I dati delle chiamate sono un buffer di dimensioni variabili che può essere usato per accumulare informazioni su una sessione di comunicazione. Queste informazioni diventano disponibili per tutte le applicazioni che possiedono o monitorano la sessione.
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: Dati della chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedfd44a46518a58f3a3aeaec59326648669cb49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344761"
---
# <a name="call-data"></a>Dati della chiamata

I dati delle chiamate sono un buffer di dimensioni variabili che può essere usato per accumulare informazioni su una sessione di comunicazione. Queste informazioni diventano disponibili per tutte le applicazioni che possiedono o monitorano la sessione.

Ad esempio, il gestore iniziale di una sessione in entrata potrebbe richiedere e immettere le informazioni sull'account client in un buffer dei dati di chiamata, quindi i gestori successivi non dovranno ripetere la richiesta.

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwCallDataSize** e **DwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**line \_ CALLINFO**](./line-callinfo.md) Message (*dwParam1* impostato su LINECALLINFOSTATE \_ CALLDATA).

**TAPI 3. x:** Vedere [**ITCallInfo::p UT \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB \_ CALLDATABUFFER** member of [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent:: Get \_ La cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) restituisce il membro **\_ CALLDATA di CIC** di [**CALLINFOCHANGE \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).

 

 
