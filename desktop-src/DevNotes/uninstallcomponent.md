---
description: Rimuove un pacchetto di eccezioni.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: UninstallComponent (funzione)
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
ms.openlocfilehash: a541f51b030c9be7a26d573794e4df3a7cfc6f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324438"
---
# <a name="uninstallcomponent-function"></a>UninstallComponent (funzione)

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

*CompGuid* \[ in, facoltativo\]
</dt> <dd>

GUID del componente eccezione da disinstallare.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Flag utilizzati per controllare i comportamenti di installazione. Questo parametro può essere una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                         | Significato                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**\_flag comp \_ NOUI**</dt> </dl>                                          | Disattiva tutta l'interfaccia utente.<br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**\_dllcache di \_ aggiornamento \_ flag comp**</dt> </dl>        | Forza l'aggiornamento della directory DLLCACHE quando viene aggiornato un file di sistema.<br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**i \_ flag comp \_ usano la \_ \_ cache svcpack**</dt> </dl> | USA i file memorizzati nella cache da un'installazione di Windows Service Pack per sostituire i file di cui è stato eseguito il backup.<br/> |



 

</dd> <dt>

*VerMajor* \[ in, facoltativo\]
</dt> <dd>

Versione principale del componente eccezione da disinstallare.

</dd> <dt>

*VersioneSecondaria* \[ in, facoltativo\]
</dt> <dd>

Versione secondaria del componente eccezione da disinstallare.

</dd> <dt>

*VerBuild* \[ in, facoltativo\]
</dt> <dd>

Versione di build del componente eccezione da disinstallare.

</dd> <dt>

*VerQFE* \[ in, facoltativo\]
</dt> <dd>

Revisione dell'hotfix del componente eccezione da disinstallare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

I pacchetti di eccezioni sono file di sistema Windows rilasciati al di fuori di una versione completa di Windows del pacchetto e che aggiornano i file del sistema operativo. I pacchetti di eccezioni vengono creati solo dai team del sistema operativo a cui è stata concessa l'autorizzazione per aggiornare i file di sistema di Windows.

Per installare e disinstallare i file non protetti dalla protezione dei file di Windows, utilizzare le funzioni descritte in [funzioni di installazione generali](https://msdn.microsoft.com/library/ms794585.aspx). Per installare i driver di dispositivo, è necessario che i venditori usino funzioni documentate in [funzioni di installazione del dispositivo](https://msdn.microsoft.com/library/ms792954.aspx) e [funzioni Configuration Manager PNP](https://msdn.microsoft.com/library/ms790838.aspx).

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**InstallComponentW**](installcomponentw.md)
</dt> </dl>

 

 
