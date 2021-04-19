---
description: Restituisce un handle per il dispositivo associato a questo canale autenticato.
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_DEVICEHANDLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3ebf54530a4ae029a52632eb5bb5afc51b5f152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305425"
---
# <a name="d3dauthenticatedquery_devicehandle"></a>\_DEVICEHANDLE D3DAUTHENTICATEDQUERY

Restituisce un handle per il dispositivo associato a questo canale autenticato. È possibile utilizzare questo handle per verificare se due canali autenticati comunicano con lo stesso dispositivo.



| Requisito | Valore |
|-------------|----------------------------------------------------------------------------------------------------------------|
| GUID query  | **\_DEVICEHANDLE D3DAUTHENTICATEDQUERY**                                                                        |
| Dati di input  | [**\_Input query \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)                           |
| Restituisce i dati | [**\_Output QUERYDEVICEHANDLE \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

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

 

 




