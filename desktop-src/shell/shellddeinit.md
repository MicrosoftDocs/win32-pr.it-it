---
description: Registra i servizi di Dynamic Data Exchange della shell (DDE) nel processo corrente, notificando al sistema che il processo corrente desidera ospitare oggetti DDE.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: ShellDDEInit (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980442"
---
# <a name="shellddeinit-function"></a>ShellDDEInit (funzione)

Registra i servizi di Dynamic Data Exchange della shell (DDE) nel processo corrente, notificando al sistema che il processo corrente desidera ospitare oggetti DDE.

## <a name="syntax"></a>Sintassi


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*init* \[ in\]
</dt> <dd>

Tipo: **bool**

**True** per registrare il processo corrente come host DDE; **False** per annullare la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Il processo che chiama questa funzione funge da Shell e viene usato per visualizzare il contenuto delle cartelle aperte con il verbo ' Open ' di [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .

Questa funzione non dispone di un file di intestazione o di libreria associato, quindi deve essere chiamata in base al valore ordinale. Chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL (Shdocvw.dll) per ottenere un handle del modulo. Chiamare quindi [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con tale handle di modulo e il numero ordinale di funzione 118 per ottenere l'indirizzo della funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP, Windows 2000 Professional \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shdocvw.dll (versione 6,0 o successiva)</dt> </dl> |



 

 
