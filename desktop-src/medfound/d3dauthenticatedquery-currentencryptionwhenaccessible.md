---
description: Restituisce il tipo di crittografia applicato prima che il contenuto diventi accessibile alla CPU o al bus.
ms.assetid: 89526bb2-1316-4730-b599-3690b1838c3e
title: D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a8b3374e6d50a50d32b60113318e5d1099083226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225815"
---
# <a name="d3dauthenticatedquery_currentencryptionwhenaccessible"></a>\_CURRENTENCRYPTIONWHENACCESSIBLE D3DAUTHENTICATEDQUERY

Restituisce il tipo di crittografia applicato prima che il contenuto diventi accessibile alla CPU o al bus.



| Requisito | Valore |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| GUID query  | **\_CURRENTENCRYPTIONWHENACCESSIBLE D3DAUTHENTICATEDQUERY**                                                                                   |
| Dati di input  | [**\_Input query \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)                                                         |
| Restituisce i dati | [**\_Output QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md) |



 

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

 

 




