---
description: Installa un pacchetto di eccezioni.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: InstallComponentW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallComponentW
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: 4d262322be6084429f03d5725f61c0e0f7140871
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330556"
---
# <a name="installcomponentw-function"></a>InstallComponentW (funzione)

Installa un pacchetto di eccezioni.

## <a name="syntax"></a>Sintassi


```C++
void InstallComponentW(
  _In_           LPCWSTR InfPath,
  _In_opt_ const GUID    *CompGuid,
  _In_           DWORD   Flags,
  _In_opt_       INT     VerMajor,
  _In_opt_       INT     VerMinor,
  _In_opt_       INT     VerBuild,
  _In_opt_       INT     VerQFE,
  _In_opt_       LPCWSTR Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*InfPath* \[ in\]
</dt> <dd>

Percorso del INF dell'eccezione da elaborare.

</dd> <dt>

*CompGuid* \[ in, facoltativo\]
</dt> <dd>

Il GUID del componente eccezione da installare.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Flag utilizzati per controllare i comportamenti di installazione. Questo parametro può essere una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                                                                               | Significato                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <dt>**Comp \_ FLAG \_ Force**</dt> <dt>0x00000020</dt> </dl>                             | Ignora il controllo della versione sulle sostituzioni di file.<br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <dt>**Comp \_ FLAG \_ necessari per la \_ disinstallazione**</dt><dt></dt> </dl>        | Eseguire il backup dei file aggiornati per l'utilizzo da parte di una disinstallazione del componente.<br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <dt>**Comp \_ FLAG \_ senza \_ sovrascrittura**</dt><dt></dt> </dl>                 | Ignora il backup dei file se la versione del componente dell'eccezione è identica a quella di un componente installato. Questo flag viene utilizzato in uno scenario di reinstallazione.<br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**Comp \_ FLAGs \_ NOUI**</dt> <dt>0x00000002</dt> </dl>                                | Disattiva tutta l'interfaccia utente.<br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**Comp \_ FLAG \_ aggiornamento \_ dllcache**</dt><dt></dt> </dl>        | Forza l'aggiornamento della directory DLLCACHE quando viene aggiornato un file di sistema.<br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**Comp \_ FLAG \_ uso \_ \_ della cache svcpack**</dt><dt></dt> </dl> | USA i file memorizzati nella cache da un'installazione di Windows Service Pack per sostituire i file di cui è stato eseguito il backup.<br/>                                                                |



 

</dd> <dt>

*VerMajor* \[ in, facoltativo\]
</dt> <dd>

Versione principale del componente dell'eccezione.

</dd> <dt>

*VersioneSecondaria* \[ in, facoltativo\]
</dt> <dd>

Versione secondaria del componente dell'eccezione.

</dd> <dt>

*VerBuild* \[ in, facoltativo\]
</dt> <dd>

Versione di build del componente dell'eccezione.

</dd> <dt>

*VerQFE* \[ in, facoltativo\]
</dt> <dd>

Revisione dell'hotfix del componente dell'eccezione.

</dd> <dt>

*Nome* \[ in, facoltativo\]
</dt> <dd>

Stringa descrittiva del componente visualizzato dalla finestra di dialogo protezione file Windows se il sistema operativo rileva che un file protetto da protezione file Windows è danneggiato, alterato o danneggiato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce un valore **HRESULT** (S \_ OK o un codice di errore). Un codice di errore può essere controllato rispetto a un valore di 0x20000100 per determinare se l'errore è dovuto al fatto che è necessario riavviare il computer.

## <a name="remarks"></a>Commenti

I pacchetti di eccezioni sono file di sistema Windows rilasciati al di fuori di una versione completa di Windows del pacchetto e che aggiornano i file del sistema operativo. I pacchetti di eccezioni vengono creati solo dai team del sistema operativo a cui è stata concessa l'autorizzazione per aggiornare i file di sistema di Windows.

Per installare e disinstallare i file non protetti dalla protezione dei file di Windows, utilizzare le funzioni descritte in [funzioni di installazione generali](https://msdn.microsoft.com/library/ms794585.aspx). Per installare i driver di dispositivo, è necessario che i venditori usino funzioni documentate in [funzioni di installazione del dispositivo](https://msdn.microsoft.com/library/ms792954.aspx) e [funzioni Configuration Manager PNP](https://msdn.microsoft.com/library/ms790838.aspx).

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



 

 
