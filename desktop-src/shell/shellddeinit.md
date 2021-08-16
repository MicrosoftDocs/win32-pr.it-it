---
description: Registra i servizi DDE (Shell Dynamic Data Exchange) nel processo corrente, notificando al sistema che il processo corrente vuole ospitare oggetti DDE.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: Funzione ShellDDEInit
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
ms.openlocfilehash: 27d2e304cf3a67f522bbeec4835f5faa98b24d1509363873bb51387391f94b1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676713"
---
# <a name="shellddeinit-function"></a>Funzione ShellDDEInit

Registra i servizi DDE (Shell Dynamic Data Exchange) nel processo corrente, notificando al sistema che il processo corrente vuole ospitare oggetti DDE.

## <a name="syntax"></a>Sintassi


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*init* \[ Pollici\]
</dt> <dd>

Tipo: **BOOL**

**TRUE** per registrare il processo corrente come host DDE. **FALSE** per annullare la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Il processo che chiama questa funzione funge da Shell e viene usato per visualizzare il contenuto delle cartelle aperte con il verbo [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 'open'.

Questa funzione non ha un file di intestazione o di libreria associato, quindi deve essere chiamata dal valore ordinale. Chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome dll (Shdocvw.dll) per ottenere un handle del modulo. Chiamare quindi [**GetProcAddress con l'handle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) del modulo e il numero ordinale della funzione 118 per ottenere l'indirizzo della funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional \[ solo app desktop\]<br/>                                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shdocvw.dll (versione 6.0 o successiva)</dt> </dl> |



 

 
