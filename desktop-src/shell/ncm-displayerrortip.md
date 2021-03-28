---
description: Visualizza un messaggio di errore nel fumetto suggerimento associato al controllo dell'indirizzo di rete.
title: Messaggio NCM_DISPLAYERRORTIP (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993776"
---
# <a name="ncm_displayerrortip-message"></a>\_Messaggio NCM DISPLAYERRORTIP

Visualizza un messaggio di errore nel fumetto suggerimento associato al controllo dell'indirizzo di rete.


```C++
NCM_DISPLAYERRORTIP

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

Se il messaggio ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Inviare questo messaggio per visualizzare un messaggio di errore quando un indirizzo digitato nel controllo non viene convalidato in base ai tipi di indirizzi di rete consentiti impostati con il messaggio [**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md) . Usare il messaggio [**NCM \_ GetAddress**](ncm-getaddress.md) per convalidare l'indirizzo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_DisplayErrorTip NetAddr**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




