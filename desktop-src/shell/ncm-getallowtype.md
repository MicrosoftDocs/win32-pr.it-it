---
description: Recupera i tipi di indirizzi di rete accettati da un controllo degli indirizzi di rete specificato.
title: NCM_GETALLOWTYPE messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11b937ca851f00c51090683db4aebfc3db63cbf83efc95bad7a6f456d8f58988
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858810"
---
# <a name="ncm_getallowtype-message"></a>Messaggio NCM \_ GETALLOWTYPE

Recupera i tipi di indirizzi di rete accettati da un controllo degli indirizzi di rete specificato.


```C++
NCM_GETALLOWTYPE

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce i tipi di indirizzi di rete consentiti come una o più costanti [**\_ NET STRING.**](net-string.md)

## <a name="remarks"></a>Commenti

La maschera restituita è il criterio usato per convalidare un indirizzo di rete nel [**messaggio NCM \_ GETADDRESS.**](ncm-getaddress.md)

Usare questo messaggio solo per un controllo degli indirizzi di rete. Per creare un'istanza, usare la **classe msctls \_ netaddress** definita in Shellapi.h. Chiamare [**InitNetworkAddressControl in**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) fase di esecuzione prima di inviare questo messaggio. In questo modo viene inizializzata la libreria di controlli comuni che contiene il controllo degli indirizzi di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md)
</dt> <dt>

[**NetAddr \_ GetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




