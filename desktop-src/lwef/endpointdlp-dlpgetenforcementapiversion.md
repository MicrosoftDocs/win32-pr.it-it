---
description: Recupera la versione dell'API prevenzione perdita dati (DLP) dell'endpoint nel dispositivo corrente.
title: Funzione DlpGetEnforcementApiVersion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495767"
---
# <a name="dlpgetenforcementapiversion-function"></a>Funzione DlpGetEnforcementApiVersion

Recupera la versione dell'API prevenzione della perdita dei dati (DLP) dell'endpoint nel dispositivo corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MajorVersion* \[ Pollici\]
</dt> <dd>

Valore **DWORD che** specifica il numero di versione principale.

</dd> </dl>

<dl> <dt>

*MajorVersion* \[ Pollici\]
</dt> <dd>

Valore **DWORD che** specifica il numero di versione secondaria.

</dd> </dl>


## <a name="return-value"></a>Valore restituito

Restituisce un HRESULT che include, ma non solo, i valori seguenti.

| HRESULT | Descrizione |
|---------|-------------|
| S_OK | La funzione è stata completata correttamente |




## <a name="remarks"></a>Osservazioni


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |