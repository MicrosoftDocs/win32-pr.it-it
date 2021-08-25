---
description: Restituisce uno degli identificatori di output associati a una sessione di crittografia e a un dispositivo Direct3D specificati.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7e8d735cf23ed5bac26ca26b779ba440f7a48301bf33f7de34d1986e75241324
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942751"
---
# <a name="d3dauthenticatedquery_outputid"></a>D3DAUTHENTICATEDQUERY \_ OUTPUTID

Restituisce uno degli identificatori di output associati a una sessione di crittografia e a un dispositivo Direct3D specificati.



| Requisito | Valore |
|-------------|--------------------------------------------------------------------------------------------------------|
| Query GUID  | **D3DAUTHENTICATEDQUERY \_ OUTPUTID**                                                                    |
| Dati di input  | [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_ INPUT**](d3dauthenticatedchannel-queryoutputid-input.md)   |
| Restituisce i dati | [**OUTPUT DI \_ QUERYOUTPUTID D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-queryoutputid-output.md) |



 

## <a name="remarks"></a>Commenti

I tipi di canale seguenti supportano questa query:

-   **HARDWARE DEL DRIVER D3DAUTHENTICATEDCHANNEL \_ \_**
-   **SOFTWARE DEL DRIVER D3DAUTHENTICATEDCHANNEL \_ \_**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[protezione del contenuto query](content-protection-queries.md)
</dt> <dt>

[Criteri basati su GPU protezione del contenuto](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




