---
description: Ottiene le dimensioni della matrice che deve essere allocata prima di chiamare CreateOPMProtectedOutputs.
ms.assetid: 65edce14-f225-4b7f-b953-32b085e1cabf
title: Funzione GetSuggestedOPMProtectedOutputArraySize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSuggestedOPMProtectedOutputArraySize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: c84738fe37661d2a593432b571c6022b0369e28ee3b2a3cb028b8eb84276a21a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879378"
---
# <a name="getsuggestedopmprotectedoutputarraysize-function"></a>Funzione GetSuggestedOPMProtectedOutputArraySize

> [!IMPORTANT]
> Questa funzione viene usata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alle funzionalità nel driver video. Le applicazioni non devono chiamare questa funzione.

 

Ottiene la dimensione della matrice che deve essere allocata prima [**di chiamare CreateOPMProtectedOutputs.**](createopmprotectedoutputs.md)

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI GetSuggestedOPMProtectedOutputArraySize(
  _In_  PUNICODE_STRING pstrDeviceName,
  _Out_ DWORD           *pdwSuggestedOPMProtectedOutputArraySize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pstrDeviceName* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ STRING UNICODE**](/windows/win32/api/subauth/ns-subauth-unicode_string) che contiene il nome del dispositivo di visualizzazione, come restituito dalla [**funzione GetMonitorInfo.**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa)

</dd> <dt>

*pdwSuggestedOPMProtectedOutputArraySize* \[ Cambio\]
</dt> <dd>

Riceve le dimensioni che devono essere allocate per la matrice, in numero di elementi della matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **STATUS \_ SUCCESS**. In caso contrario, restituisce un **codice di errore NTSTATUS.**

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico Gdi32.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni OPM](opm-functions.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 
