---
description: Visualizza un messaggio di errore nella descrizione del fumetto associata al controllo dell'indirizzo di rete.
title: NCM_DISPLAYERRORTIP messaggio (Shellapi.h)
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
ms.openlocfilehash: 046119c93ec6a80fcfcedbd562d04665d5642fd832f2385bab914cc732499e5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111471"
---
# <a name="ncm_displayerrortip-message"></a>Messaggio \_ DISPLAYERRORTIP NCM

Visualizza un messaggio di errore nella descrizione del fumetto associata al controllo dell'indirizzo di rete.


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

Se il messaggio ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Inviare questo messaggio per visualizzare un messaggio di errore quando un indirizzo digitato nel controllo non viene convalidato in base ai tipi di indirizzi di rete consentiti impostati con il messaggio [**NCM \_ SETALLOWTYPE.**](ncm-setallowtype.md) Usare il [**messaggio NCM \_ GETADDRESS**](ncm-getaddress.md) per convalidare l'indirizzo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NetAddr \_ DisplayErrorTip**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




