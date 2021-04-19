---
description: Inizializza il gestore di componenti facoltativo.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: OcInitialize (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326087"
---
# <a name="ocinitialize-function"></a>OcInitialize (funzione)

Inizializza il gestore di componenti facoltativo.

## <a name="syntax"></a>Sintassi


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Callback di* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ \_ callback del client OCM**](ocm-client-callbacks.md) che specifica le funzioni di callback che devono essere utilizzate dal gestore OC per eseguire varie attività.

</dd> <dt>

*MasterOcInfName* \[ in\]
</dt> <dd>

Percorso del file master OC. inf.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Il parametro può essere costituito da uno o più dei valori seguenti.

<dl> <dt>

<span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT \_ FORCENEWINF** (0x00000001)
</dt> <dt>

<span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT \_ KILLSUBCOMPS** (0x00000002)
</dt> <dt>

<span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT \_ RUNQUIET** (0x00000004)
</dt> <dt>

<span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT \_ LANGUAGEAWARE** (0x00000008)
</dt> </dl> </dd> <dt>

*ShowError* \[ out\]
</dt> <dd>

Se la funzione ha esito negativo, questo parametro indica se visualizzare o meno un messaggio di errore.

</dd> <dt>

*Log* \[ di in\]
</dt> <dd>

Handle per il log.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce il valore di contesto di gestione OC.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_callback client \_ OCM**](ocm-client-callbacks.md)
</dt> <dt>

[**OcTerminate**](octerminate.md)
</dt> </dl>

 

 
