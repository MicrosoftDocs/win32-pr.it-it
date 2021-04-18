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
# <a name="uninstallcomponent-function"></a><span data-ttu-id="07263-103">UninstallComponent (funzione)</span><span class="sxs-lookup"><span data-stu-id="07263-103">UninstallComponent function</span></span>

<span data-ttu-id="07263-104">Rimuove un pacchetto di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="07263-104">Removes an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="07263-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07263-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="07263-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="07263-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07263-107">*CompGuid* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="07263-107">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07263-108">GUID del componente eccezione da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="07263-108">The GUID of the exception component being uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="07263-109">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07263-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07263-110">Flag utilizzati per controllare i comportamenti di installazione.</span><span class="sxs-lookup"><span data-stu-id="07263-110">The flags used to control installation behaviors.</span></span> <span data-ttu-id="07263-111">Questo parametro può essere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="07263-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="07263-112">Valore</span><span class="sxs-lookup"><span data-stu-id="07263-112">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="07263-113">Significato</span><span class="sxs-lookup"><span data-stu-id="07263-113">Meaning</span></span>                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="07263-114"><dt>**\_flag comp \_ NOUI**</dt></span><span class="sxs-lookup"><span data-stu-id="07263-114"><dt>**COMP\_FLAGS\_NOUI**</dt></span></span> </dl>                                          | <span data-ttu-id="07263-115">Disattiva tutta l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="07263-115">Suppresses all UI.</span></span><br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="07263-116"><dt>**\_dllcache di \_ aggiornamento \_ flag comp**</dt></span><span class="sxs-lookup"><span data-stu-id="07263-116"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt></span></span> </dl>        | <span data-ttu-id="07263-117">Forza l'aggiornamento della directory DLLCACHE quando viene aggiornato un file di sistema.</span><span class="sxs-lookup"><span data-stu-id="07263-117">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="07263-118"><dt>**i \_ flag comp \_ usano la \_ \_ cache svcpack**</dt></span><span class="sxs-lookup"><span data-stu-id="07263-118"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt></span></span> </dl> | <span data-ttu-id="07263-119">USA i file memorizzati nella cache da un'installazione di Windows Service Pack per sostituire i file di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="07263-119">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="07263-120">*VerMajor* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="07263-120">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07263-121">Versione principale del componente eccezione da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="07263-121">The major version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="07263-122">*VersioneSecondaria* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="07263-122">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07263-123">Versione secondaria del componente eccezione da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="07263-123">The minor version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="07263-124">*VerBuild* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="07263-124">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07263-125">Versione di build del componente eccezione da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="07263-125">The build version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="07263-126">*VerQFE* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="07263-126">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07263-127">Revisione dell'hotfix del componente eccezione da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="07263-127">The hotfix revision of the Exception component to be uninstalled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07263-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07263-128">Return value</span></span>

<span data-ttu-id="07263-129">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="07263-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07263-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="07263-130">Remarks</span></span>

<span data-ttu-id="07263-131">I pacchetti di eccezioni sono file di sistema Windows rilasciati al di fuori di una versione completa di Windows del pacchetto e che aggiornano i file del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="07263-131">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="07263-132">I pacchetti di eccezioni vengono creati solo dai team del sistema operativo a cui è stata concessa l'autorizzazione per aggiornare i file di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="07263-132">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="07263-133">Per installare e disinstallare i file non protetti dalla protezione dei file di Windows, utilizzare le funzioni descritte in [funzioni di installazione generali](https://msdn.microsoft.com/library/ms794585.aspx).</span><span class="sxs-lookup"><span data-stu-id="07263-133">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="07263-134">Per installare i driver di dispositivo, è necessario che i venditori usino funzioni documentate in [funzioni di installazione del dispositivo](https://msdn.microsoft.com/library/ms792954.aspx) e [funzioni Configuration Manager PNP](https://msdn.microsoft.com/library/ms790838.aspx).</span><span class="sxs-lookup"><span data-stu-id="07263-134">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="07263-135">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="07263-135">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="07263-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07263-136">Requirements</span></span>



| <span data-ttu-id="07263-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="07263-137">Requirement</span></span> | <span data-ttu-id="07263-138">Valore</span><span class="sxs-lookup"><span data-stu-id="07263-138">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07263-139">DLL</span><span class="sxs-lookup"><span data-stu-id="07263-139">DLL</span></span><br/> | <dl> <span data-ttu-id="07263-140"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07263-140"><dt>Msoobci.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07263-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07263-141">See also</span></span>

<dl> <span data-ttu-id="07263-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="07263-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="07263-143">**InstallComponentW**</span><span class="sxs-lookup"><span data-stu-id="07263-143">**InstallComponentW**</span></span>](installcomponentw.md)
</dt> </dl>

 

 
