---
description: Installa un pacchetto di eccezioni.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: Funzione InstallComponentW
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
ms.openlocfilehash: 9deaa460ec58ad0aa07af38aa03f53971068b4a6a1d43131e5473a7e4def908c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955920"
---
# <a name="installcomponentw-function"></a>Funzione InstallComponentW

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

*InfPath* \[ Pollici\]
</dt> <dd>

Percorso del file INF dell'eccezione da elaborare.

</dd> <dt>

*Guida alla compilazione* \[ in, facoltativo\]
</dt> <dd>

GUID del componente eccezione da installare.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Flag utilizzati per controllare i comportamenti di installazione. Questo parametro può essere una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                                                                               | Significato                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <dt>**Comp \_ FLAG \_ FORCE**</dt> <dt>0x00000020</dt> </dl>                             | Ignora il controllo della versione per le sostituzioni di file.<br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <dt>**Comp \_ I FLAG \_ DEVONO ESSERE \_ DISINSTALLATI**</dt><dt></dt> </dl>        | Eseguire il backup dei file aggiornati per essere usati da una disinstallazione del componente.<br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <dt>**Comp \_ FLAG \_ NO \_ OVERWRITE**</dt><dt></dt> </dl>                 | Ignora il backup dei file se la versione del componente Exception è uguale a un componente installato. Questo flag viene usato in uno scenario di reinstallazione.<br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**Comp \_ FLAG \_ NOUI**</dt> <dt>0x00000002</dt> </dl>                                | Elimina tutta l'interfaccia utente.<br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**Comp \_ FLAG \_ AGGIORNA \_ DLLCACHE**</dt><dt></dt> </dl>        | Forza l'aggiornamento della directory DLLCACHE quando viene aggiornato un file di sistema.<br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**Comp \_ I FLAG \_ USANO \_ LA \_ CACHE SVCPACK**</dt><dt></dt> </dl> | Usa i file memorizzati nella cache da Windows'installazione del Service Pack per sostituisce i file di cui è stato eseguito il backup.<br/>                                                                |



 

</dd> <dt>

*VerMajor* \[ in, facoltativo\]
</dt> <dd>

Versione principale del componente Exception.

</dd> <dt>

*VerMinor* \[ in, facoltativo\]
</dt> <dd>

Versione secondaria del componente Exception.

</dd> <dt>

*VerBuild* \[ in, facoltativo\]
</dt> <dd>

Versione build del componente Exception.

</dd> <dt>

*VerQFE* \[ in, facoltativo\]
</dt> <dd>

Revisione dell'hotfix del componente Exception.

</dd> <dt>

*Nome* \[ in, facoltativo\]
</dt> <dd>

Stringa descrittiva del componente visualizzata nella finestra di dialogo Protezione file di Windows se il sistema operativo rileva che un file di protezione della protezione file di Windows è danneggiato, manomesso o danneggiato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce un **valore HRESULT** (S \_ OK o un codice di errore). Un codice di errore può essere verificato rispetto al valore 0x20000100 per determinare se l'errore è dovuto a un riavvio necessario.

## <a name="remarks"></a>Commenti

I pacchetti di Windows sono file di sistema che vengono rilasciati al di fuori di un pacchetto completo Windows versione e che aggiornano i file del sistema operativo. I pacchetti di eccezioni vengono creati solo dai team del sistema operativo a cui è stata concessa l'autorizzazione per aggiornare Windows di sistema.

Per installare e disinstallare i file che non sono protetti Windows Protezione file, usare le funzioni documentate in [Funzioni di installazione generali](https://msdn.microsoft.com/library/ms794585.aspx). Per installare i driver di dispositivo, i venditori devono usare le funzioni documentate in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) e [PnP Gestione configurazione Functions](https://msdn.microsoft.com/library/ms790838.aspx).

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



 

 
