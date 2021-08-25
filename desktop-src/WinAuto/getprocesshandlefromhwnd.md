---
title: Funzione GetProcessHandleFromHwnd
description: Recupera un handle di processo da un handle di finestra.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- Accessibilità della funzione GetProcessHandleFromHwnd Windows
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4096f77b4295e9567f17f747a5aee1edae1b592cb49c89547102cb6d017b7814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860351"
---
# <a name="getprocesshandlefromhwnd-function"></a>Funzione GetProcessHandleFromHwnd

Recupera un handle di processo da un handle di finestra.

## <a name="syntax"></a>Sintassi


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwnd* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

Handle di finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HANDLE**](/windows/desktop/WinProg/windows-data-types)**

Se ha esito positivo, restituisce l'handle del processo proprietario della finestra.

Se non ha esito positivo, restituisce **NULL.**

## <a name="remarks"></a>Commenti

Nelle versioni precedenti del sistema operativo, un processo poteva aprire un altro processo (ad esempio per accedere alla memoria) usando [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess). Questa funzione ha esito positivo se il chiamante dispone dei privilegi appropriati. in genere il chiamante e il processo di destinazione devono essere dello stesso utente.

In Windows Vista, tuttavia, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) ha esito negativo nello scenario in cui il chiamante ha UIAccess e il processo di destinazione è elevato. In questo caso, il proprietario del processo di destinazione si trova nel gruppo Administrators, ma il processo chiamante viene eseguito con il token con restrizioni, quindi non è membro di questo gruppo e viene negato l'accesso al processo con privilegi elevati. Se il chiamante ha UIAccess, tuttavia, può usare un hook di Windows per inserire codice nel processo di destinazione e, dall'interno del processo di destinazione, inviare un handle al chiamante.

**GetProcessHandleFromHwnd** è una funzione comoda che usa questa tecnica per ottenere l'handle del processo proprietario dell'oggetto HWND specificato. Si noti che ha esito positivo solo nei casi in cui il chiamante e il processo di destinazione sono in esecuzione come lo stesso utente. L'handle restituito ha i privilegi seguenti: PROCESS \_ DUP \_ HANDLE PROCESS VM OPERATION PROCESS VM READ PROCESS VM \| WRITE \_ \_ \| \_ \_ \| \_ \_ \| SYNCHRONIZE. Se sono necessari altri privilegi, potrebbe essere necessario implementare la tecnica di hook in modo esplicito anziché usare questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Oleacc.dll</dt> </dl> |



 

