---
description: Configura un oggetto di output protetto.
ms.assetid: d22a378e-2d4e-4ff4-a18e-136932c24d2b
title: Funzione ConfigureOPMProtectedOutput
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: f62d310526d95cf4ab6d1727a3ba43eec147f320b04c0692a89d52305b7f3589
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743548"
---
# <a name="configureopmprotectedoutput-function"></a>Funzione ConfigureOPMProtectedOutput

> [!IMPORTANT]
> Questa funzione viene usata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alle funzionalità nel driver video. Le applicazioni non devono chiamare questa funzione.

 

Configura un oggetto di output protetto.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI ConfigureOPMProtectedOutput(
  _In_       OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _In_ const DXGKMDT_OPM_CONFIGURE_PARAMETERS *pParameters,
  _In_       ULONG                            ulAdditionalParametersSize,
  _In_ const BYTE                             *pbAdditionalParameters
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*opoOPMProtectedOutput* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto di output protetto. Questo handle viene ottenuto chiamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

</dd> <dt>

*pParameters* \[ Pollici\]
</dt> <dd>

Puntatore a una **struttura DXGKMDT \_ OPM \_ CONFIGURE \_ PARAMETERS** che contiene il comando di configurazione.

</dd> <dt>

*ulAdditionalParametersSize* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer *pbAdditionalParameters,* in byte.

</dd> <dt>

*pbAdditionalParameters* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer che contiene informazioni aggiuntive per il comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **STATUS \_ SUCCESS**. In caso contrario, restituisce un **codice di errore NTSTATUS.**

## <a name="remarks"></a>Commenti

Le applicazioni devono [**chiamare IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) invece di chiamare questa funzione.

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico Gdi32.dll.

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

 

 
