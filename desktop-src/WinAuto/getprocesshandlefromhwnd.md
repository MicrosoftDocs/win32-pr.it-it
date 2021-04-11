---
title: GetProcessHandleFromHwnd (funzione)
description: Recupera un handle di processo da un handle di finestra.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- Accessibilità di Windows per la funzione GetProcessHandleFromHwnd
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
ms.openlocfilehash: bee00f36f236396816e7bb54cadbe6914f3437e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119863"
---
# <a name="getprocesshandlefromhwnd-function"></a>GetProcessHandleFromHwnd (funzione)

Recupera un handle di processo da un handle di finestra.

## <a name="syntax"></a>Sintassi


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Tipo: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

Handle di finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **handle**](/windows/desktop/WinProg/windows-data-types)**

Se l'operazione riesce, restituisce l'handle del processo a cui appartiene la finestra.

Se ha esito negativo, restituisce **null**.

## <a name="remarks"></a>Commenti

Nelle versioni precedenti del sistema operativo un processo poteva aprire un altro processo (ad esempio, per accedere alla sua memoria) usando [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess). Questa funzione ha esito positivo se il chiamante dispone dei privilegi appropriati; in genere il chiamante e il processo di destinazione devono essere lo stesso utente.

In Windows Vista, tuttavia, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) ha esito negativo nello scenario in cui il chiamante ha uiAccess e il processo di destinazione è elevato. In questo caso, il proprietario del processo di destinazione si trova nel gruppo Administrators, ma il processo chiamante è in esecuzione con il token con restrizioni, quindi non ha l'appartenenza a questo gruppo e viene negato l'accesso al processo con privilegi elevati. Se il chiamante ha UIAccess, tuttavia, può usare un hook di Windows per inserire il codice nel processo di destinazione e, dal processo di destinazione, restituire un handle al chiamante.

**GetProcessHandleFromHwnd** è una funzione utile che usa questa tecnica per ottenere l'handle del processo a cui appartiene l'HWND specificato. Si noti che ha esito positivo solo nei casi in cui il chiamante e il processo di destinazione vengono eseguiti con lo stesso utente. L'handle restituito ha i privilegi seguenti: processo duplicato Gestisci processo macchina virtuale processo macchina virtuale \_ \_ lettura processo macchina virtuale \| \_ \_ \| \_ \_ \| \_ \_ scrittura \| sincronizzazione. Se sono necessari altri privilegi, potrebbe essere necessario implementare la tecnica di hook in modo esplicito anziché usare questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Oleacc.dll</dt> </dl> |



 

