---
description: Specificare i livelli di protezione per il sistema di gestione della generazione della copia&\# 8212; Analogico (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: CGMS-flag di protezione (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401552"
---
# <a name="cgms-a-protection-flags"></a>CGMS-flag di protezione

Le costanti nella tabella seguente specificano i livelli di protezione per l'analogico del sistema di gestione della generazione di copia (CGMS-A).



| Costante/valore                                                                                                                                                                                                                                                                                                 | Descrizione                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <dt>**OPM \_ CGMSA \_ off**</dt> <dt>0x00</dt> </dl>                                                                                       | CGMS-A è disabilitato. <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <dt>**OPM \_ Copia di CGMSA \_ \_ liberamente**</dt> <dt>0x01</dt> </dl>                                                              | Il livello di protezione è copy free.<br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <dt>**OPM \_ CGMSA \_ Copia \_ non \_ più**</dt> <dt>0x02</dt> </dl>                                                          | Il livello di protezione non è più disponibile per la copia. <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <dt>**OPM \_ CGMSA \_ copia 0x03 di \_ una \_ generazione**</dt> <dt></dt> </dl>                                     | Il livello di protezione è copia di una generazione. <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <dt>**OPM \_ CGMSA \_ copy \_ Never**</dt> <dt>0x04</dt> </dl>                                                                 | Il livello di protezione non è mai copiato.<br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <dt>**OPM \_ Il \_ controllo di ridistribuzione CGMSA è \_ \_ obbligatorio**</dt> <dt>0x08</dt> </dl> | È necessario il controllo di ridistribuzione (detto anche *flag di trasmissione*). Questo flag può essere combinato con gli altri flag.<br/> |



## <a name="remarks"></a>Commenti

Questi flag sono equivalenti alle costanti di enumerazione del **\_ livello di \_ protezione \_ Copp CGMSA** utilizzate nel protocollo di protezione output (Copp) certificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti Media Foundation](media-foundation-constants.md)
</dt> </dl>

 

 




