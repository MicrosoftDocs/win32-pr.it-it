---
description: Recupera i tipi di indirizzi di rete accettati da un controllo di indirizzo di rete specificato.
title: Messaggio NCM_GETALLOWTYPE (Shellapi. h)
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
ms.openlocfilehash: 5d93cb3cff575c18764e352da54a717d7c557001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049601"
---
# <a name="ncm_getallowtype-message"></a>\_Messaggio NCM GETALLOWTYPE

Recupera i tipi di indirizzi di rete accettati da un controllo di indirizzo di rete specificato.


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

Restituisce i tipi di indirizzi di rete consentiti come una o più costanti [**\_ stringa di rete**](net-string.md) .

## <a name="remarks"></a>Commenti

La maschera restituita è il criterio usato per convalidare un indirizzo di rete nel messaggio [**NCM \_ GetAddress**](ncm-getaddress.md) .

Utilizzare questo messaggio solo per un controllo degli indirizzi di rete. Per creare un'istanza di, usare la classe **msctls \_ Netaddress** definita in Shellapi. h. Chiamare [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) in fase di esecuzione prima di inviare questo messaggio. Viene inizializzata la libreria di controlli comuni che contiene il controllo degli indirizzi di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md)
</dt> <dt>

[**\_GetAllowType NetAddr**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




