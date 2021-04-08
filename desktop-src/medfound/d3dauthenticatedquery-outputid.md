---
description: Restituisce uno degli identificatori di output associato a una sessione di crittografia e a un dispositivo Direct3D specificati.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types. h)
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
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749295"
---
# <a name="d3dauthenticatedquery_outputid"></a>\_OUTPUTID D3DAUTHENTICATEDQUERY

Restituisce uno degli identificatori di output associato a una sessione di crittografia e a un dispositivo Direct3D specificati.



| Requisito | Valore |
|-------------|--------------------------------------------------------------------------------------------------------|
| GUID query  | **\_OUTPUTID D3DAUTHENTICATEDQUERY**                                                                    |
| Dati di input  | [**\_Input QUERYOUTPUTID \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryoutputid-input.md)   |
| Restituisce i dati | [**\_Output QUERYOUTPUTID \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryoutputid-output.md) |



 

## <a name="remarks"></a>Commenti

I tipi di canale seguenti supportano questa query:

-   **\_Hardware driver \_ D3DAUTHENTICATEDCHANNEL**
-   **\_Software driver \_ D3DAUTHENTICATEDCHANNEL**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Query di protezione del contenuto](content-protection-queries.md)
</dt> <dt>

[protezione del contenuto basate su GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




