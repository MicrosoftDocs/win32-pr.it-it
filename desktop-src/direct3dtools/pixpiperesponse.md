---
description: Enumerazione utilizzata per inviare risposte dal motore di acquisizione a Diagnostica della grafica.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione PixPipeResponse
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5BFEE25D-3E03-493E-AFEF-DD8C70C53FC5
api_name:
- PixPipeResponse
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ad00d7bada935dd27f711499e5975d31709b9940
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631689"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span id="vspixengine.pixpiperesponse"></span>Enumerazione PixPipeResponse

Enumerazione utilizzata per inviare risposte dal motore di acquisizione a Diagnostica della grafica.

## <a name="syntax"></a>Sintassi


```C++
};
```

## <a name="constants"></a>Costanti

<span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NUOVI \_ DATI \_ DISPONIBILI**  
Risposta che indica che i nuovi dati sono stati scritti nel log di grafica ed è pronto per essere letti.

<span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**DATI \_ DELL'ESPERIMENTO**  
Risposta che indica le informazioni di configurazione relative alla sessione di acquisizione.

<span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**  
Risposta che indica che il motore di acquisizione ha rilevato un errore.

<span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**  
Risposta che indica che il motore di acquisizione ha iniziato ad acquisire informazioni grafiche. Ciò non indica che i dati sono ancora disponibili per essere esaminati.

<span id="PARTIAL_DATA"></span><span id="partial_data"></span>**DATI \_ PARZIALI**  
Risposta che indica che i dati parziali sono stati scritti nel log di grafica.

<span id="READY"></span><span id="ready"></span>**PRONTO**  
Risposta che indica che il motore di acquisizione è pronto per avviare l'acquisizione di informazioni grafiche.

<span id="DONE"></span><span id="done"></span>**FATTO**  
Interno

<span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**  
Risposta che indica che è stata avviata un'acquisizione di frame.

<span id="STATUS"></span><span id="status"></span>**STATO**  
Risposta che indica le informazioni sullo stato dell'app acquisita. ad esempio framerate.

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



