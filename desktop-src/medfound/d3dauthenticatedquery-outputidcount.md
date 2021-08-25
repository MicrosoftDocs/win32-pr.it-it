---
description: Restituisce il numero di identificatori di output associati a una sessione di crittografia e a un dispositivo Direct3D specificati.
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: c6a3da90d467701decfe5f96383e06026325e86c2622ec0f05f4703b06e2cbe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828511"
---
# <a name="d3dauthenticatedquery_outputidcount"></a>D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT

Restituisce il numero di identificatori di output associati a una sessione di crittografia e a un dispositivo Direct3D specificati.



| Requisito | Valore |
|-------------|------------------------------------------------------------------------------------------------------------------|
| Query GUID  | **D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**                                                                         |
| Dati di input  | [**INPUT DI D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_**](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| Restituisce i dati | [**OUTPUT DI \_ QUERYOUTPUTIDCOUNT D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

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

 

 




