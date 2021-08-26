---
description: Restituisce il numero di tipi di crittografia che possono essere usati per crittografare il contenuto prima che diventi accessibile alla CPU o al bus.
ms.assetid: 442b80f5-8467-427d-a01e-5d22f6ddafea
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: f47074947cc2f758d35691e05dda9b39f2f823feb6d647a7d77c0a3cc0030c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942761"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguidcount"></a>CRITTOGRAFIA D3DAUTHENTICATEDQUERYWHENACCESSIBLEGUIDCOUNT \_

Restituisce il numero di tipi di crittografia che possono essere usati per crittografare il contenuto prima che diventi accessibile alla CPU o al bus.



| Requisito | Valore |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Query GUID  | **CRITTOGRAFIA D3DAUTHENTICATEDQUERYWHENACCESSIBLEGUIDCOUNT \_**                                                                                 |
| Dati di input  | [**INPUT DI QUERY D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)                                                         |
| Restituisce i dati | [**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUIDCOUNT \_ OUTPUT**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md) |



 

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

[Impostazioni basate su GPU protezione del contenuto](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




