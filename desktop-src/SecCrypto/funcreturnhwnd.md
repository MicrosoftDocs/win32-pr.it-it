---
description: Utilizzato da un provider del servizio di crittografia (CSP) per ottenere l'handle di finestra che il provider di servizi di crittografia deve usare come padre o proprietario di qualsiasi interfaccia utente visualizzata.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: CRYPT_RETURN_HWND puntatore a funzione (Cspdk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 387e1e9140dac8081acf851eb7125a612506783adbeefe1174137ff7f74fae9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006749"
---
# <a name="crypt_return_hwnd-function-pointer"></a>Puntatore a funzione \_ CRYPT RETURN \_ HWND

La funzione di callback **FuncReturnhWnd** viene usata da un [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) per ottenere l'handle di finestra che il provider di servizi di crittografia deve usare come padre o proprietario di qualsiasi interfaccia utente visualizzata.

## <a name="syntax"></a>Sintassi


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phWnd* \[ in, out\]
</dt> <dd>

Indirizzo di una **variabile HWND** che riceve l'handle della finestra padre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo puntatore a funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Cspdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
