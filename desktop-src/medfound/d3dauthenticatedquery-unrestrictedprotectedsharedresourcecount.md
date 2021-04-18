---
description: Restituisce il numero di risorse condivise protette che possono essere aperte da qualsiasi processo senza restrizioni.
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b2d834927d21c59ed5c70dcf3a001d100340405d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305417"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a>\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT D3DAUTHENTICATEDQUERY

Restituisce il numero di risorse condivise protette che possono essere aperte da qualsiasi processo senza restrizioni.



| Requisito | Valore |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID query  | **\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT D3DAUTHENTICATEDQUERY**                                                                                                    |
| Dati di input  | [**\_Input query \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)                                                                                   |
| Restituisce i dati | [**\_Output QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a>Commenti

L'unico tipo di canale che supporta questa query è il **\_ \_ software del driver D3DAUTHENTICATEDCHANNEL**.

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

 

 




