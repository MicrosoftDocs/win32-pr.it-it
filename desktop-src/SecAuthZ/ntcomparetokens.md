---
description: Confronta due token di accesso e determina se sono equivalenti rispetto a una chiamata alla funzione AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Funzione NtCompareTokens (Ntseapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: a763f6f4238632c3bcc736ebacbd2ff133b1955da673a0397ba9a95ebb87c2fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780563"
---
# <a name="ntcomparetokens-function"></a>Funzione NtCompareTokens

La **funzione NtCompareTokens** confronta due [*token*](/windows/desktop/SecGloss/a-gly) di accesso e determina se sono equivalenti rispetto a una chiamata alla [**funzione AccessCheck.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FirstTokenHandle* \[ Pollici\]
</dt> <dd>

Handle per il primo token di accesso da confrontare. Il token deve essere aperto per **l'accesso \_ TOKEN QUERY.**

</dd> <dt>

*SecondTokenHandle* \[ Pollici\]
</dt> <dd>

Handle per il secondo token di accesso da confrontare. Il token deve essere aperto per **l'accesso \_ TOKEN QUERY.**

</dd> <dt>

*Uguale a* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve un valore che indica se i token rappresentati dai parametri *FirstTokenHandle* e *SecondTokenHandle* sono equivalenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce STATUS \_ SUCCESS.

Se la funzione ha esito negativo, restituisce un **codice di errore NTSTATUS.**

## <a name="remarks"></a>Commenti

Due token di controllo di accesso sono considerati equivalenti se tutte le condizioni seguenti sono vere:

-   Ogni [*ID di*](/windows/desktop/SecGloss/s-gly) sicurezza (SID) presente in uno dei due token è presente anche nell'altro token.
-   Nessuno dei token o entrambi sono limitati.
-   Se entrambi i token sono limitati, anche ogni SID con restrizioni in un token viene limitato nell'altro token.
-   Ogni privilegio presente in uno dei due token è presente anche nell'altro token.

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Ntseapi.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

