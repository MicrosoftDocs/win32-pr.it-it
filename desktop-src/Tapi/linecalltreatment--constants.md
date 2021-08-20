---
description: Le costanti LINECALLTREATMENT elencano i trattamento per le chiamate senza risposta \_ o in attesa. Fatta eccezione per la convalida dei parametri di base, il trattamento delle chiamate è un pass-through diretto tramite TAPI al provider di servizi.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: LINECALLTREATMENT_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88c627a89fdf5ab0592c862f09753e0b913eb4b7197a04d4db8cd06478ef10b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118863839"
---
# <a name="linecalltreatment_-constants"></a>Costanti LINECALLTREATMENT \_

Le **costanti LINECALLTREATMENT \_** elencano i trattamento per le chiamate senza risposta o in attesa. Fatta eccezione per la convalida dei parametri di base, il trattamento delle chiamate è un pass-through diretto tramite TAPI al provider di servizi.

<dl> <dt>

<span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ BUSY**
</dt> <dd> <dl> <dt>



Quando la chiamata non è attivamente connessa a un dispositivo (offerta o acconto), l'entità ascolta un segnale di occupato.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**LINECALLTREATMENT \_ MUSIC**
</dt> <dd> <dl> <dt>



Quando la chiamata non è attivamente connessa a un dispositivo (offerta o in ascolto), l'entità ascolta musica.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT \_ RINGBACK**
</dt> <dd> <dl> <dt>



Quando la chiamata non è attivamente connessa a un dispositivo (offerta o acconto), l'entità ascolta il tono della ringback.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT \_ SILENCE**
</dt> <dd> <dl> <dt>



Quando la chiamata non è attivamente connessa a un dispositivo (offerta o acconto), la parte ascolta il silenzio.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Il valore 0x00000000 è riservato per indicare che il provider di servizi non supporta i trattamento delle chiamate. I valori nell'intervallo 0x00000005 a 0x000000FF sono riservati per una definizione futura. I valori nell'0x00000100 a 0xFFFFFFFF sono riservati per l'assegnazione da parte dei provider di servizi e possono includere l'identificazione di selezioni o annunci registrati specifici.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




