---
description: Restituisce il tipo di bus di I/O utilizzato per inviare dati alla GPU.
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9d7d4daaec3d52b7aabafe61c5763304c400b6a36be1367e01b0a9163f2f9e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828681"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a>D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES

Restituisce il tipo di bus di I/O utilizzato per inviare dati alla GPU.



| Requisito | Valore |
|-------------|--------------------------------------------------------------------------------------------------------------|
| Query GUID  | **D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**                                                           |
| Dati di input  | [**INPUT DELLA QUERY D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)                         |
| Restituisce i dati | [**OUTPUT DI D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_**](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a>Commenti

Questa query restituisce anche informazioni sull'accessibilità del contenuto quando viene inserito nella memoria video.

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

 

 




