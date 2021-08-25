---
description: Crea oggetti di output protetti per un dispositivo di visualizzazione.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: Funzione CreateOPMProtectedOutputs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: fe2bcc0d190cf94a48b10f3d588ab4acd2d93913552f8ccef9d7eb92fefa598b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829061"
---
# <a name="createopmprotectedoutputs-function"></a>Funzione CreateOPMProtectedOutputs

> [!IMPORTANT]
> Questa funzione viene usata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alle funzionalità nel driver video. Le applicazioni non devono chiamare questa funzione.

 

Crea oggetti di output protetti per un dispositivo di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pstrDeviceName* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ STRING UNICODE**](/windows/win32/api/subauth/ns-subauth-unicode_string) contenente il nome del dispositivo di visualizzazione, come restituito dalla [**funzione GetMonitorInfo.**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa)

</dd> <dt>

*vos* \[ Pollici\]
</dt> <dd>

Membro dell'enumerazione **VIDEO OUTPUT \_ \_ \_ \_ SEMANTICS DXGKMDT OPM,** che specifica se l'output protetto avrà la semantica COPP (Certified Output Protection Protocol) o OPM.

</dd> <dt>

*dwOPMProtectedOutputArraySize* \[ Pollici\]
</dt> <dd>

Numero di elementi nella matrice *pohOPMProtectedOutputArray.*

</dd> <dt>

*pdwNumOPMProtectedOutputsInArray* \[ Cambio\]
</dt> <dd>

Riceve il numero di elementi copiati dalla funzione nella matrice *pohOPMProtectedOutputArray.*

</dd> <dt>

*pohOPMProtectedOutputArray* \[ Cambio\]
</dt> <dd>

Matrice che riceve handle per gli oggetti di output protetti. Ogni handle deve essere rilasciato chiamando [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **STATUS \_ SUCCESS**. In caso contrario, restituisce un **codice di errore NTSTATUS.**

## <a name="remarks"></a>Commenti

Anziché usare questa funzione, le applicazioni devono chiamare una delle funzioni seguenti:

-   [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente Gdi32.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni OPM](opm-functions.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 
