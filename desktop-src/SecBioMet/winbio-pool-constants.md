---
title: WINBIO_POOL costanti (Winbio \_ types.h)
description: Specificare il tipo di pool di unità biometriche da usare nella sessione.
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fefc43bb9dc4cefbde1ce5622853a3ba2cfae498ff2f8f81e97417e306641db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909798"
---
# <a name="winbio_pool-constants"></a>Costanti POOL WINBIO \_

Le costanti seguenti possono essere usate nella funzione [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) per specificare il tipo di pool di unità biometriche da usare nella sessione.



| Costante                                                                                                                                                                                  | Descrizione                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**POOL WINBIO \_ \_ SCONOSCIUTO**</dt> </dl>          | Il tipo di pool è sconosciuto.<br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**SISTEMA POOL \_ WINBIO \_**</dt> </dl>             | Specifica una raccolta condivisa di unità biometriche gestite dal provider di servizi.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**POOL WINBIO \_ \_ PRIVATO**</dt> </dl>          | Specifica una raccolta di unità biometriche gestite dal chiamante.<br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <dt>**POOL WINBIO \_ \_ NON ASSEGNATO**</dt> </dl> | Riservato.<br/>                                                                         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





