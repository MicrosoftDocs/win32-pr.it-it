---
description: Rimuove un pacchetto di eccezioni.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: Funzione UninstallComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: d6b4ce8e447bc884d1b3ee64505d230b2e069ce6cda1630b027b8a48da68beda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001111"
---
# <a name="uninstallcomponent-function"></a>Funzione UninstallComponent

Rimuove un pacchetto di eccezioni.

## <a name="syntax"></a>Sintassi


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Guida alla compilazione* \[ in, facoltativo\]
</dt> <dd>

GUID del componente eccezione da disinstallare.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Flag utilizzati per controllare i comportamenti di installazione. Questo parametro può essere una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                         | Significato                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**COMP \_ FLAGS \_ NOUI**</dt> </dl>                                          | Elimina tutta l'interfaccia utente.<br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**AGGIORNAMENTO \_ DEI FLAG COMP \_ \_ DLLCACHE**</dt> </dl>        | Forza l'aggiornamento della directory DLLCACHE quando viene aggiornato un file di sistema.<br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**I \_ FLAG COMP USANO LA \_ CACHE \_ SVCPACK \_**</dt> </dl> | Usa i file memorizzati nella cache da Windows'installazione del Service Pack per sostituisce i file di cui è stato eseguito il backup.<br/> |



 

</dd> <dt>

*VerMajor* \[ in, facoltativo\]
</dt> <dd>

Versione principale del componente Eccezione da disinstallare.

</dd> <dt>

*VerMinor* \[ in, facoltativo\]
</dt> <dd>

Versione secondaria del componente Eccezione da disinstallare.

</dd> <dt>

*VerBuild* \[ in, facoltativo\]
</dt> <dd>

Versione build del componente Eccezione da disinstallare.

</dd> <dt>

*VerQFE* \[ in, facoltativo\]
</dt> <dd>

Revisione dell'hotfix del componente Eccezione da disinstallare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

I pacchetti di Windows sono file di sistema che vengono rilasciati al di fuori di un pacchetto completo Windows versione e che aggiornano i file del sistema operativo. I pacchetti di eccezioni vengono creati solo dai team del sistema operativo a cui è stata concessa l'autorizzazione per aggiornare Windows di sistema.

Per installare e disinstallare i file che non sono protetti Windows Protezione file, usare le funzioni documentate in [Funzioni di installazione generali](https://msdn.microsoft.com/library/ms794585.aspx). Per installare i driver di dispositivo, i venditori devono usare le funzioni documentate in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) e [PnP Gestione configurazione Functions](https://msdn.microsoft.com/library/ms790838.aspx).

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**InstallComponentW**](installcomponentw.md)
</dt> </dl>

 

 
