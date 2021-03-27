---
description: Imposta i tipi di indirizzi di rete accettati da un controllo di indirizzo di rete specificato.
title: Messaggio NCM_SETALLOWTYPE (Shellapi. h)
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
ms.openlocfilehash: d9cc822e07022a01439fbe7e41243bd1b78e636b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753055"
---
# <a name="ncm_setallowtype-message"></a>\_Messaggio NCM SETALLOWTYPE

Imposta i tipi di indirizzi di rete accettati da un controllo di indirizzo di rete specificato.


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*addrMask* \[ in\]
</dt> <dd>Specifica i tipi di indirizzo di rete come una o più <a href="net-string.md">**costanti \_ stringa net**</a> .</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se l'esito è positivo o un valore di errore in caso contrario.

## <a name="remarks"></a>Commenti

Il set di maschere è il criterio utilizzato per convalidare un indirizzo di rete nel messaggio [**NCM \_ GetAddress**](ncm-getaddress.md) .

Utilizzare questo messaggio solo per un controllo degli indirizzi di rete. Per creare un'istanza di, usare la classe **msctls \_ Netaddress** definita in Shellapi. h. Chiamare [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) in fase di esecuzione prima di inviare questo messaggio. Viene inizializzata la libreria di controlli comuni che contiene il controllo degli indirizzi di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**\_SetAllowType NetAddr**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




