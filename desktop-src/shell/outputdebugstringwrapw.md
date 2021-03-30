---
description: Invia una stringa Unicode al debugger per la visualizzazione.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Funzione OutputDebugStringWrapW (Shlwapip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: e8213aee48a90a816e2968aac115159472ed7b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994821"
---
# <a name="outputdebugstringwrapw-function"></a>OutputDebugStringWrapW (funzione)

\[Questa funzione è disponibile per l'utilizzo in Windows XP. Potrebbe non essere disponibile nelle versioni successive. Usare [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) al suo posto.\]

Invia una stringa Unicode al debugger per la visualizzazione.

> [!Note]  
> **OutputDebugStringWrapW** è un wrapper per la funzione **OutputDebugStringW** . Per ulteriori note sull'utilizzo, vedere la pagina [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) .

 

## <a name="syntax"></a>Sintassi


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpOutputString* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore alla stringa Unicode con terminazione null da visualizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

**OutputDebugStringWrapW** offre la possibilità di utilizzare stringhe Unicode nei sistemi operativi precedenti a Windows XP. Il metodo preferito consiste nell'usare [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) insieme a Microsoft Layer for Unicode (MSLU).

**OutputDebugStringWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 115.

Se l'applicazione non dispone di un debugger, il debugger di sistema Visualizza la stringa. Se l'applicazione non dispone di un debugger e il debugger di sistema non è attivo, **OutputDebugStringWrapW** non esegue alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shlwapip. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
