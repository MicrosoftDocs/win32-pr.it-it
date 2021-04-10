---
description: Restituisce il livello di protezione corrente per il dispositivo.
ms.assetid: 335d21e8-2a98-4824-a60d-1969a40e8d24
title: D3DAUTHENTICATEDQUERY_PROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_PROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 85147d764d5b6580305723e9b05b127b116a660e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225812"
---
# <a name="d3dauthenticatedquery_protection"></a>\_Protezione D3DAUTHENTICATEDQUERY

Restituisce il livello di protezione corrente per il dispositivo.



| Requisito | Valore |
|-------------|------------------------------------------------------------------------------------------------------------|
| GUID query  | **\_Protezione D3DAUTHENTICATEDQUERY**                                                                      |
| Dati di input  | [**\_Input query \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)                       |
| Restituisce i dati | [**\_Output QUERYPROTECTION \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryprotection-output.md) |



 

## <a name="remarks"></a>Commenti

Questa query è valida per tutti i tipi di canale.

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

 

 




