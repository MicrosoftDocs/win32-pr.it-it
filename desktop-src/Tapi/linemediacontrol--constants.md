---
description: Le costanti del flag di bit LINEMEDIACONTROL \_ descrivono un set di operazioni generiche sui flussi multimediali.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: LINEMEDIACONTROL_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54c7c83df769eef91afe7c310452c342a855f44391815bbc4429ac07bb6ec92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309971"
---
# <a name="linemediacontrol_-constants"></a>Costanti \_ LINEMEDIACONTROL

Le costanti del flag di bit **LINEMEDIACONTROL \_** descrivono un set di operazioni generiche sui flussi multimediali. Le interpretazioni sono determinate dal flusso multimediale. Per essere efficace, il dispositivo linea deve avere la funzionalità di controllo dei supporti per qualsiasi operazione di controllo multimediale.

<dl> <dt>

<span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ NONE**
</dt> <dd> <dl> <dt>



Non è necessario a apportare modifiche al flusso multimediale.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL \_ PAUSE**
</dt> <dd> <dl> <dt>



Sospendere temporaneamente il flusso multimediale.

La velocità del flusso multimediale viene restituita alla normalità.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL \_ RATEDOWN**
</dt> <dd> <dl> <dt>



La velocità del flusso multimediale viene ridotta di una quantità definita dal flusso.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL \_ RATENORMAL**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL \_ RATEUP**
</dt> <dd> <dl> <dt>



La velocità del flusso multimediale viene aumentata di una quantità definita dal flusso.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**REIMPOSTAZIONE \_ LINEMEDIACONTROL**
</dt> <dd> <dl> <dt>



Reimpostare il flusso multimediale. Equivale a una fine dell'input. Tutti i buffer vengono rilasciati.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**RIPRESA \_ LINEMEDIACONTROL**
</dt> <dd> <dl> <dt>



Riprendere un flusso multimediale sospeso.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL \_ START**
</dt> <dd> <dl> <dt>



Avviare il flusso multimediale.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL \_ VOLUMEDOWN**
</dt> <dd> <dl> <dt>



L'ampiezza del flusso multimediale viene ridotta di una quantità definita dal flusso.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL \_ VOLUMENORMAL**
</dt> <dd> <dl> <dt>



L'ampiezza del flusso multimediale viene restituita alla normalità.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL \_ VOLUMEUP**
</dt> <dd> <dl> <dt>



L'ampiezza del flusso multimediale viene aumentata di una quantità definita dal flusso.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I 16 bit di ordine elevato possono essere assegnati per le estensioni specifiche del dispositivo. I 16 bit meno bassi sono riservati.

Il controllo multimediale viene fornito per migliorare le prestazioni delle azioni sui flussi multimediali in risposta a eventi correlati alla telefonia. L'applicazione deve in genere gestire un flusso multimediale tramite l'API specifica del supporto. La funzionalità di controllo multimediale fornita qui non è progettata per sostituire le API multimediali native.

Le azioni di controllo dei supporti possono essere associate al rilevamento di cifre, al rilevamento dei toni, alla transizione a uno stato di chiamata e al rilevamento di un tipo di supporto. Consultare le funzionalità del dispositivo di una linea per determinare se il controllo multimediale è disponibile sulla linea.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




