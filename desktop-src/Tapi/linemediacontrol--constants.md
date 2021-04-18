---
description: Le \_ costanti del flag di bit LINEMEDIACONTROL descrivono un set di operazioni generiche sui flussi multimediali.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: Costanti LINEMEDIACONTROL_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3241a3b5f4f8a0363f30ce7aefaded0c63fc4189
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330742"
---
# <a name="linemediacontrol_-constants"></a>\_Costanti LINEMEDIACONTROL

Le costanti del flag di bit **LINEMEDIACONTROL \_** descrivono un set di operazioni generiche sui flussi multimediali. Le interpretazioni sono determinate dal flusso multimediale. Il dispositivo a linee deve avere la funzionalità di controllo del supporto per l'efficacia di qualsiasi operazione di controllo del supporto.

<dl> <dt>

<span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ None**
</dt> <dd> <dl> <dt>



Non è necessario apportare alcuna modifica al flusso multimediale.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL \_ pausa**
</dt> <dd> <dl> <dt>



Sospende temporaneamente il flusso multimediale.

La velocità del flusso multimediale viene restituita al normale.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**\_RATEDOWN LINEMEDIACONTROL**
</dt> <dd> <dl> <dt>



La velocità del flusso multimediale è diminuita in base a una quantità definita dal flusso.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**\_RATENORMAL LINEMEDIACONTROL**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**\_Rateup LINEMEDIACONTROL**
</dt> <dd> <dl> <dt>



La velocità del flusso multimediale viene aumentata in base a una quantità definita dal flusso.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**reimpostazione LINEMEDIACONTROL \_**
</dt> <dd> <dl> <dt>



Reimpostare il flusso multimediale. Equivalente a una fine dell'input. Vengono rilasciati tutti i buffer.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**Riprendi LINEMEDIACONTROL \_**
</dt> <dd> <dl> <dt>



Riprendere un flusso multimediale sospeso.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**\_inizio LINEMEDIACONTROL**
</dt> <dd> <dl> <dt>



Avviare il flusso multimediale.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**\_volumedown LINEMEDIACONTROL**
</dt> <dd> <dl> <dt>



L'ampiezza del flusso multimediale è diminuita in base a una quantità definita dal flusso.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**\_VOLUMENORMAL LINEMEDIACONTROL**
</dt> <dd> <dl> <dt>



L'ampiezza del flusso multimediale viene restituita al normale.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**\_VOLUMEUP LINEMEDIACONTROL**
</dt> <dd> <dl> <dt>



L'ampiezza del flusso multimediale viene aumentata in base a una quantità definita dal flusso.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo. I 16 bit di ordine inferiore sono riservati.

Il controllo multimediale viene fornito per migliorare le prestazioni delle azioni sui flussi multimediali in risposta ad eventi correlati alla telefonia. L'applicazione deve normalmente gestire un flusso multimediale tramite l'API specifica del supporto. La funzionalità di controllo dei supporti disponibile qui non è destinata a sostituire le API multimediali native.

Le azioni di controllo del supporto possono essere associate al rilevamento di cifre, al rilevamento di toni, alla transizione in uno stato di chiamata e al rilevamento di un tipo di supporto. Per determinare se il controllo multimediale è disponibile sulla linea, consultare le funzionalità del dispositivo di una linea.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




