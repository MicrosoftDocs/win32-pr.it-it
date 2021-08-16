---
description: Invia una stringa Unicode al debugger per la visualizzazione.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Funzione OutputDebugStringWrapW (Shlwapip.h)
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
ms.openlocfilehash: cce8754b01ddf156951964b7189b4a7189759c52cdcd08e08091ca62b2e950bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858790"
---
# <a name="outputdebugstringwrapw-function"></a>Funzione OutputDebugStringWrapW

\[Questa funzione è disponibile per l'uso in Windows XP. Potrebbe non essere disponibile nelle versioni successive. Usare [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) al suo posto.\]

Invia una stringa Unicode al debugger per la visualizzazione.

> [!Note]  
> **OutputDebugStringWrapW** è un wrapper per la **funzione OutputDebugStringW.** Per altre note sull'utilizzo, vedere la pagina [**OutputDebugString.**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)

 

## <a name="syntax"></a>Sintassi


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpOutputString* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore alla stringa Unicode con terminazione Null da visualizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

**OutputDebugStringWrapW** offre la possibilità di usare stringhe Unicode nei sistemi operativi precedenti Windows XP. Il metodo preferito è usare [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) insieme a Microsoft Layer for Unicode (MSLU).

**OutputDebugStringWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 115.

Se l'applicazione non dispone di un debugger, il debugger di sistema visualizza la stringa. Se l'applicazione non ha debugger e il debugger di sistema non è attivo, **OutputDebugStringWrapW** non esegue alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shlwapip.h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Outputdebugstring**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
