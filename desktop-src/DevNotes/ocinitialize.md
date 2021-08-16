---
description: Inizializza la gestione componenti facoltativa.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: Funzione OcInitialize
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
ms.openlocfilehash: 08e7ffd7f8ad6faa2b08f937627627b6e74bbc09505482c589023db5dae37677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826746"
---
# <a name="ocinitialize-function"></a>Funzione OcInitialize

Inizializza la gestione componenti facoltativa.

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

*Callback* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ CALLBACK \_ CLIENT OCM**](ocm-client-callbacks.md) che specifica le funzioni di callback che devono essere utilizzate dal gestore OC per eseguire varie attività.

</dd> <dt>

*MasterOcInfName* \[ Pollici\]
</dt> <dd>

Percorso del file OC master con estensione inf.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Questo parametro può essere uno o più dei valori seguenti.

<dl> <dt>

<span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OETTAT \_ FORCENEWINF** (0x00000001)
</dt> <dt>

<span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OETTAT \_ KILLSUBCOMPS** (0x00000002)
</dt> <dt>

<span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OETTAT \_ RUNQUIET** (0x00000004)
</dt> <dt>

<span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OETTAT \_ LANGUAGEAWARE** (0x00000008)
</dt> </dl> </dd> <dt>

*ShowError* \[ Cambio\]
</dt> <dd>

Se la funzione ha esito negativo, questo parametro indica se visualizzare un messaggio di errore.

</dd> <dt>

*Log* \[ Pollici\]
</dt> <dd>

Handle per il log.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce il valore del contesto di gestione OC.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CALLBACK CLIENT OCM \_ \_**](ocm-client-callbacks.md)
</dt> <dt>

[**OcTerminate**](octerminate.md)
</dt> </dl>

 

 
