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
# <a name="installcomponentw-function"></a><span data-ttu-id="f519f-103">InstallComponentW (funzione)</span><span class="sxs-lookup"><span data-stu-id="f519f-103">InstallComponentW function</span></span>

<span data-ttu-id="f519f-104">Installa un pacchetto di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="f519f-104">Installs an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="f519f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f519f-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f519f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f519f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f519f-107">*InfPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f519f-107">*InfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f519f-108">Percorso del INF dell'eccezione da elaborare.</span><span class="sxs-lookup"><span data-stu-id="f519f-108">The path to the exception INF to process.</span></span>

</dd> <dt>

<span data-ttu-id="f519f-109">*CompGuid* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f519f-109">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f519f-110">Il GUID del componente eccezione da installare.</span><span class="sxs-lookup"><span data-stu-id="f519f-110">The GUID of the exception component being installed.</span></span>

</dd> <dt>

<span data-ttu-id="f519f-111">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f519f-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f519f-112">Flag utilizzati per controllare i comportamenti di installazione.</span><span class="sxs-lookup"><span data-stu-id="f519f-112">The flags used to control installation behaviors.</span></span> <span data-ttu-id="f519f-113">Questo parametro può essere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f519f-113">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="f519f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f519f-114">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="f519f-115">Significato</span><span class="sxs-lookup"><span data-stu-id="f519f-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <span data-ttu-id="f519f-116"><dt>**Comp \_ FLAG \_ Force**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="f519f-116"><dt>**COMP\_FLAGS\_FORCE**</dt> <dt>0x00000020</dt></span></span> </dl>                             | <span data-ttu-id="f519f-117">Ignora il controllo della versione sulle sostituzioni di file.</span><span class="sxs-lookup"><span data-stu-id="f519f-117">Skips the version check on file replacements.</span></span><br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <span data-ttu-id="f519f-118"><dt>**Comp \_ FLAG \_ necessari per la \_ disinstallazione**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="f519f-118"><dt>**COMP\_FLAGS\_NEEDS\_UNINSTALL**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="f519f-119">Eseguire il backup dei file aggiornati per l'utilizzo da parte di una disinstallazione del componente.</span><span class="sxs-lookup"><span data-stu-id="f519f-119">Back up files that are updated to be used by an uninstall of the component.</span></span><br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <span data-ttu-id="f519f-120"><dt>**Comp \_ FLAG \_ senza \_ sovrascrittura**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="f519f-120"><dt>**COMP\_FLAGS\_NO\_OVERWRITE**</dt> <dt></dt></span></span> </dl>                 | <span data-ttu-id="f519f-121">Ignora il backup dei file se la versione del componente dell'eccezione è identica a quella di un componente installato.</span><span class="sxs-lookup"><span data-stu-id="f519f-121">Skips backing up files if the Exception component version is the same as an installed component.</span></span> <span data-ttu-id="f519f-122">Questo flag viene utilizzato in uno scenario di reinstallazione.</span><span class="sxs-lookup"><span data-stu-id="f519f-122">This flag is used in a reinstallation scenario.</span></span><br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="f519f-123"><dt>**Comp \_ FLAGs \_ NOUI**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="f519f-123"><dt>**COMP\_FLAGS\_NOUI**</dt> <dt>0x00000002</dt></span></span> </dl>                                | <span data-ttu-id="f519f-124">Disattiva tutta l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f519f-124">Suppresses all UI.</span></span><br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="f519f-125"><dt>**Comp \_ FLAG \_ aggiornamento \_ dllcache**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="f519f-125"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="f519f-126">Forza l'aggiornamento della directory DLLCACHE quando viene aggiornato un file di sistema.</span><span class="sxs-lookup"><span data-stu-id="f519f-126">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="f519f-127"><dt>**Comp \_ FLAG \_ uso \_ \_ della cache svcpack**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="f519f-127"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="f519f-128">USA i file memorizzati nella cache da un'installazione di Windows Service Pack per sostituire i file di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="f519f-128">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="f519f-129">*VerMajor* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f519f-129">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f519f-130">Versione principale del componente dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="f519f-130">The major version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="f519f-131">*VersioneSecondaria* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f519f-131">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f519f-132">Versione secondaria del componente dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="f519f-132">The minor version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="f519f-133">*VerBuild* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f519f-133">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f519f-134">Versione di build del componente dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="f519f-134">The build version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="f519f-135">*VerQFE* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f519f-135">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f519f-136">Revisione dell'hotfix del componente dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="f519f-136">The hotfix revision of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="f519f-137">*Nome* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f519f-137">*Name* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f519f-138">Stringa descrittiva del componente visualizzato dalla finestra di dialogo protezione file Windows se il sistema operativo rileva che un file protetto da protezione file Windows è danneggiato, alterato o danneggiato.</span><span class="sxs-lookup"><span data-stu-id="f519f-138">The descriptive string of the component shown by the Windows File Protection dialog box if the operating system detects that a Windows File Protection protect file is damaged, tampered with, or corrupted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f519f-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f519f-139">Return value</span></span>

<span data-ttu-id="f519f-140">Questa funzione restituisce un valore **HRESULT** (S \_ OK o un codice di errore).</span><span class="sxs-lookup"><span data-stu-id="f519f-140">This function returns an **HRESULT** value (S\_OK or a failure code).</span></span> <span data-ttu-id="f519f-141">Un codice di errore può essere controllato rispetto a un valore di 0x20000100 per determinare se l'errore è dovuto al fatto che è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="f519f-141">A failure code can be checked against a value of 0x20000100 to determine whether the failure is because a reboot is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="f519f-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="f519f-142">Remarks</span></span>

<span data-ttu-id="f519f-143">I pacchetti di eccezioni sono file di sistema Windows rilasciati al di fuori di una versione completa di Windows del pacchetto e che aggiornano i file del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f519f-143">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="f519f-144">I pacchetti di eccezioni vengono creati solo dai team del sistema operativo a cui è stata concessa l'autorizzazione per aggiornare i file di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="f519f-144">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="f519f-145">Per installare e disinstallare i file non protetti dalla protezione dei file di Windows, utilizzare le funzioni descritte in [funzioni di installazione generali](https://msdn.microsoft.com/library/ms794585.aspx).</span><span class="sxs-lookup"><span data-stu-id="f519f-145">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="f519f-146">Per installare i driver di dispositivo, è necessario che i venditori usino funzioni documentate in [funzioni di installazione del dispositivo](https://msdn.microsoft.com/library/ms792954.aspx) e [funzioni Configuration Manager PNP](https://msdn.microsoft.com/library/ms790838.aspx).</span><span class="sxs-lookup"><span data-stu-id="f519f-146">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="f519f-147">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f519f-147">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f519f-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f519f-148">Requirements</span></span>



| <span data-ttu-id="f519f-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="f519f-149">Requirement</span></span> | <span data-ttu-id="f519f-150">Valore</span><span class="sxs-lookup"><span data-stu-id="f519f-150">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f519f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f519f-151">DLL</span></span><br/> | <dl> <span data-ttu-id="f519f-152"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f519f-152"><dt>Msoobci.dll</dt></span></span> </dl> |



 

 
