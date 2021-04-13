---
description: Restituisce il tipo di bus di I/O utilizzato per inviare i dati alla GPU.
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types. h)
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
ms.openlocfilehash: 5119da4e7efaf0c27db1065dacc56e3388a77474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401540"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a>\_ACCESSIBILITYATTRIBUTES D3DAUTHENTICATEDQUERY

Restituisce il tipo di bus di I/O utilizzato per inviare i dati alla GPU.



| Requisito | Valore |
|-------------|--------------------------------------------------------------------------------------------------------------|
| GUID query  | **\_ACCESSIBILITYATTRIBUTES D3DAUTHENTICATEDQUERY**                                                           |
| Dati di input  | [**\_Input query \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)                         |
| Restituisce i dati | [**\_Output QUERYINFOBUSTYPE \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a>Commenti

Questa query restituisce anche informazioni sul modo in cui il contenuto viene inserito nella memoria video.

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

 

 




