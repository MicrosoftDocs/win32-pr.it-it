---
description: Restituisce il numero di processi a cui è consentito aprire risorse condivise con accesso limitato.
ms.assetid: e1b9ef18-fd08-4639-9ba9-4bccd33f5d16
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5238d027b5fe8ed7ebd1ab941b3877d5b545239b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305418"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocesscount"></a>\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT D3DAUTHENTICATEDQUERY

Restituisce il numero di processi a cui è consentito aprire risorse condivise con accesso limitato.



| Requisito | Valore |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID query  | **\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT D3DAUTHENTICATEDQUERY**                                                                                                |
| Dati di input  | [**\_Input query \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)                                                                           |
| Restituisce i dati | [**\_Output QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md) |



 

## <a name="remarks"></a>Commenti

I tipi di canale seguenti supportano questa query:

-   **\_D3d9 D3DAUTHENTICATEDCHANNEL**
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

 

 




