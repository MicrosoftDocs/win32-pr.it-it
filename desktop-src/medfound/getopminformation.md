---
description: Invia una richiesta di stato OPM a un oggetto di output protetto.
ms.assetid: 4b691b20-25de-4b9e-a725-674a57697b56
title: Funzione GetOPMInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bd9912289d17085bf94f3ef8316869ffb29d3a5adead4e10fc0e6d24844f4ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777301"
---
# <a name="getopminformation-function"></a>Funzione GetOPMInformation

> [!IMPORTANT]
> Questa funzione viene usata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alle funzionalità nel driver video. Le applicazioni non devono chiamare questa funzione.

 

Invia una richiesta di stato OPM a un oggetto di output protetto.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI GetOPMInformation(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE       opoOPMProtectedOutput,
  _In_  const DXGKMDT_OPM_GET_INFO_PARAMETERS   *pParameters,
  _Out_       DXGKMDT_OPM_REQUESTED_INFORMATION *pRequestedInformation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*opoOPMProtectedOutput* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto di output protetto. Questo handle viene ottenuto chiamando [**CreateOPMProtectedOutputs.**](createopmprotectedoutputs.md)

</dd> <dt>

*pParameters* \[ Pollici\]
</dt> <dd>

Puntatore a una **struttura DXGKMDT \_ OPM GET \_ INFO \_ \_ PARAMETERS** che contiene i dati di input per la richiesta di stato.

</dd> <dt>

*pRequestedInformation* \[ Cambio\]
</dt> <dd>

Puntatore a una **struttura DXGKMDT \_ OPM \_ REQUESTED \_ INFORMATION** che riceve i risultati della richiesta di stato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **STATUS \_ SUCCESS**. In caso contrario, restituisce un **codice di errore NTSTATUS.**

## <a name="remarks"></a>Commenti

Le applicazioni devono [**chiamare IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) invece di chiamare questa funzione.

L'oggetto di output protetto deve essere creato con la semantica OPM. Vedere [**CreateOPMProtectedOutputs.**](createopmprotectedoutputs.md)

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

 

 
