---
description: Invia una richiesta di stato di OPM a un oggetto di output protetto.
ms.assetid: 4b691b20-25de-4b9e-a725-674a57697b56
title: GetOPMInformation (funzione)
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
ms.openlocfilehash: 450292c0f6352436d7df8c91afff0d08c8c31394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305373"
---
# <a name="getopminformation-function"></a>GetOPMInformation (funzione)

> [!IMPORTANT]
> Questa funzione viene utilizzata da [Output Protection Manager](output-protection-manager.md) (OPM) per accedere alla funzionalità nel driver di visualizzazione. Le applicazioni non devono chiamare questa funzione.

 

Invia una richiesta di stato di OPM a un oggetto di output protetto.

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

*opoOPMProtectedOutput* \[ in\]
</dt> <dd>

Handle per l'oggetto di output protetto. Questo handle viene ottenuto chiamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

</dd> <dt>

*pParameters* \[ in\]
</dt> <dd>

Un puntatore a una struttura **DXGKMDT \_ OPM \_ get \_ info \_ Parameters** che contiene i dati di input per la richiesta di stato.

</dd> <dt>

*pRequestedInformation* \[ out\]
</dt> <dd>

Puntatore a una struttura **di \_ \_ \_ informazioni richiesta da DXGKMDT OPM** che riceve i risultati della richiesta di stato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**. In caso contrario, restituisce un codice di errore **NTSTATUS** .

## <a name="remarks"></a>Commenti

Le applicazioni devono chiamare [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) anziché chiamare questa funzione.

L'oggetto di output protetto deve essere creato con la semantica OPM. Vedere [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di OPM](opm-functions.md)
</dt> <dt>

[Gestione protezione output](output-protection-manager.md)
</dt> </dl>

 

 
