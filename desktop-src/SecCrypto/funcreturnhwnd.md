---
description: Utilizzato da un provider del servizio di crittografia (CSP) per ottenere l'handle della finestra che il CSP deve utilizzare come padre o proprietario di qualsiasi interfaccia utente visualizzata.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: Puntatore a funzione CRYPT_RETURN_HWND (Cspdk. h)
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
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317735"
---
# <a name="crypt_return_hwnd-function-pointer"></a>\_Puntatore a \_ funzione HWND restituito dalla crittografia

La funzione di callback **FuncReturnhWnd** viene utilizzata da un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) per ottenere l'handle della finestra che deve essere utilizzato dal CSP come padre o proprietario di qualsiasi interfaccia utente visualizzata.

## <a name="syntax"></a>Sintassi


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phWnd* \[ in uscita\]
</dt> <dd>

Indirizzo di una variabile **HWND** che riceve l'handle della finestra padre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo puntatore a funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
