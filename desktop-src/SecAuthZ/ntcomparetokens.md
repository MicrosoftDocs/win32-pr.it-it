---
description: Confronta due token di accesso e determina se sono equivalenti rispetto a una chiamata alla funzione AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Funzione NtCompareTokens (Ntseapi. h)
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
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310772"
---
# <a name="ntcomparetokens-function"></a>NtCompareTokens (funzione)

La funzione **NtCompareTokens** Confronta due [*token di accesso*](/windows/desktop/SecGloss/a-gly) e determina se sono equivalenti rispetto a una chiamata alla funzione [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) .

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

*FirstTokenHandle* \[ in\]
</dt> <dd>

Handle per il primo token di accesso da confrontare. Il token deve essere aperto per l'accesso alla **\_ query del token** .

</dd> <dt>

*SecondTokenHandle* \[ in\]
</dt> <dd>

Handle per il secondo token di accesso da confrontare. Il token deve essere aperto per l'accesso alla **\_ query del token** .

</dd> <dt>

*Uguale* \[ a out\]
</dt> <dd>

Puntatore a una variabile che riceve un valore che indica se i token rappresentati dai parametri *FirstTokenHandle* e *SecondTokenHandle* sono equivalenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce lo stato \_ Success.

Se la funzione ha esito negativo, restituisce un codice di errore **NTSTATUS** .

## <a name="remarks"></a>Commenti

Due token di controllo di accesso sono considerati equivalenti se si verificano tutte le condizioni seguenti:

-   Ogni [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) presente in uno dei due token è presente anche nell'altro token.
-   Nessuno o entrambi i token sono limitati.
-   Se entrambi i token sono limitati, anche ogni SID limitato in un token viene limitato nell'altro token.
-   Ogni privilegio presente in uno dei due token è presente anche nell'altro token.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Ntseapi. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

