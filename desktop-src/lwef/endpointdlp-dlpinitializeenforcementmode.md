---
description: Notifica al sistema le modalità di imposizione desiderate per un set di operazioni dlp (Data Loss Prevention) dell'endpoint.
title: Funzione DlpInitializeEnforcementMode (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cff3e1609f15f2cbbe6f6d9f76c6433ba3f4e5d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495731"
---
# <a name="dlpinitializeenforcementmode-function"></a>Funzione DlpInitializeEnforcementMode

Notifica al sistema le modalità di imposizione desiderate per un set di operazioni dlp (Data Loss Prevention) dell'endpoint.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Conteggio* \[ Pollici\]
</dt> <dd>

Valore **DWORD** che specifica il numero di operazioni incluse nella *matrice OperationEnforcement.*

</dd> </dl>

<dl> <dt>

*OperationEnforcement* \[ Pollici\]
</dt> <dd>

Matrice di strutture [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) che specificano il livello di imposizione per un'operazione DLP dell'endpoint.

</dd> </dl>


## <a name="return-value"></a>Valore restituito

Restituisce un HRESULT che include, ma non solo, i valori seguenti.

| HRESULT | Descrizione |
|---------|-------------|
| S_OK | La funzione è stata completata correttamente |
| E_INVALIDARG | Uno o più parametri della funzione non sono validi. |
| E_OUTOFMEMORY | Allocazione di memoria per l'operazione non riuscita. |



## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |