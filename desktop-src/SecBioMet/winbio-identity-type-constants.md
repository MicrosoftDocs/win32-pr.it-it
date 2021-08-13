---
title: WINBIO_IDENTITY_TYPE costanti (Winbio \_ types.h)
description: Specificare il formato delle informazioni sull'identità contenute nella struttura WINBIO \_ IDENTITY.
ms.assetid: 27A01538-9B26-4A29-8ADB-ED9C5D5808B3
topic_type:
- apiref
api_name:
- WINBIO_ID_TYPE_NULL
- WINBIO_ID_TYPE_WILDCARD
- WINBIO_ID_TYPE_GUID
- WINBIO_ID_TYPE_SID
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2f0e51d30e45b16dd7683d746cdef7ab5f75aaf62611102dd4dcd3e7bd07c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910193"
---
# <a name="winbio_identity_type-constants"></a>Costanti IDENTITY \_ \_ TYPE WINBIO

Le costanti **WINBIO \_ IDENTITY TYPE \_ seguenti** possono essere usate per specificare il formato delle informazioni sull'identità contenute nella [**struttura WINBIO \_ IDENTITY.**](winbio-identity.md)



| Costante                                                                                                                                                                                      | Descrizione                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**TIPO DI ID WINBIO \_ \_ \_ NULL**</dt> </dl>             | Al modello non è associato alcun ID. <br/>            |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**CARATTERE JOLLY TIPO ID WINBIO \_ \_ \_**</dt> </dl> | La struttura corrisponde a tutte le identità del modello.<br/> |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**GUID TIPO ID WINBIO \_ \_ \_**</dt> </dl>             | Un GUID identifica il modello.<br/>                |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**SID TIPO DI ID WINBIO \_ \_ \_**</dt> </dl>                | Un SID dell'account identifica il modello.<br/>        |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> <dt>

[**IDENTITÀ \_ WINBIO**](winbio-identity.md)
</dt> </dl>

 

 





