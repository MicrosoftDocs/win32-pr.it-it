---
description: Crea un'istanza del motore di acquisizione.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: Funzione MFCreateCaptureEngine
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: 18d264b30b8f3ed4d06e80f236908dd7bc81dbe96c4eb9c3231fa330331e34f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940251"
---
# <a name="mfcreatecaptureengine-function"></a>Funzione MFCreateCaptureEngine

\[MFCreateCaptureEngine non è supportato e potrebbe essere modificato o non disponibile in futuro. \]

Crea un'istanza del motore di acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppCaptureEngine* \[ Cambio\]
</dt> <dd>

Riceve un puntatore [**all'interfaccia IMFCaptureEngine.**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) Il chiamante deve rilasciare l'interfaccia .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce S \_ OK. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione e non è dichiarata in un file di intestazione pubblico. È necessario usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico MFCaptureEngine.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                     |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                        |
| DLL<br/>                      | <dl> <dt>MFCaptureEngine.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation funzioni](media-foundation-functions.md)
</dt> </dl>

 

 
