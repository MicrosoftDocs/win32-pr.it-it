---
description: Imposta i tipi di indirizzi di rete accettati da un controllo degli indirizzi di rete specificato.
title: NCM_SETALLOWTYPE messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d3fc6b8ceb848d4738ff2d77b4441a29354bf09248e0de88008072dbf867e8a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719925"
---
# <a name="ncm_setallowtype-message"></a>Messaggio NCM \_ SETALLOWTYPE

Imposta i tipi di indirizzi di rete accettati da un controllo degli indirizzi di rete specificato.


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*addrMask* \[ Pollici\]
</dt> <dd>Specifica i tipi di indirizzi di rete come una o più costanti <a href="net-string.md">**\_ NET STRING.**</a></dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo oppure un valore di errore in caso contrario.

## <a name="remarks"></a>Commenti

Il set di maschere è il criterio usato per convalidare un indirizzo di rete nel [**messaggio NCM \_ GETADDRESS.**](ncm-getaddress.md)

Usare questo messaggio solo per un controllo degli indirizzi di rete. Per creare un'istanza, usare la **classe msctls \_ netaddress** definita in Shellapi.h. Chiamare [**InitNetworkAddressControl in**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) fase di esecuzione prima di inviare questo messaggio. In questo modo viene inizializzata la libreria di controlli comuni che contiene il controllo degli indirizzi di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




