---
description: Le \_ costanti LINECALLTREATMENT elencano i trattamenti per le chiamate senza risposta o in attesa. Ad eccezione della convalida dei parametri di base, il trattamento delle chiamate è un pass-through lineare di TAPI al provider di servizi.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: Costanti LINECALLTREATMENT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25a19b5db4525550047c468b496cce2363f6ee2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332725"
---
# <a name="linecalltreatment_-constants"></a>\_Costanti LINECALLTREATMENT

Le **costanti \_ LINECALLTREATMENT** elencano i trattamenti per le chiamate senza risposta o in attesa. Ad eccezione della convalida dei parametri di base, il trattamento delle chiamate è un pass-through lineare di TAPI al provider di servizi.

<dl> <dt>

<span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ occupato**
</dt> <dd> <dl> <dt>



Quando la chiamata non è connessa attivamente a un dispositivo (offerta o ontenuta), la parte riceve un segnale occupato.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**\_musica LINECALLTREATMENT**
</dt> <dd> <dl> <dt>



Quando la chiamata non è connessa attivamente a un dispositivo (offerta o ontenuta), l'entità ascolta la musica.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT \_ risponder**
</dt> <dd> <dl> <dt>



Quando la chiamata non è connessa attivamente a un dispositivo (offerta o ontenuta), l'entità riceve un segnale di riscontro.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT \_ silenzioso**
</dt> <dd> <dl> <dt>



Quando la chiamata non è connessa attivamente a un dispositivo (offerta o ontenuta), la parte sente il silenzio.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Il valore 0x00000000 è riservato per indicare che il provider di servizi non supporta i trattamenti di chiamata. I valori nell'intervallo compreso tra 0x00000005 e 0x000000FF sono riservati per la definizione futura. I valori nell'intervallo compreso tra 0x00000100 e 0xFFFFFFFF sono riservati per l'assegnazione da parte dei provider di servizi e possono includere l'identificazione di selezioni musicali specifiche o annunci registrati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




