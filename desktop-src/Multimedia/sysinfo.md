---
title: comando sysinfo
description: Il comando sysinfo recupera le informazioni sul sistema MCI. Il comando sysinfo è un comando di sistema MCI; viene interpretato direttamente da MCI.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- comando di sysinfo Windows Multimedia
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302584"
---
# <a name="sysinfo-command"></a><span data-ttu-id="79dc6-105">comando sysinfo</span><span class="sxs-lookup"><span data-stu-id="79dc6-105">sysinfo command</span></span>

<span data-ttu-id="79dc6-106">Il comando sysinfo recupera le informazioni sul sistema MCI.</span><span class="sxs-lookup"><span data-stu-id="79dc6-106">The sysinfo command retrieves MCI system information.</span></span> <span data-ttu-id="79dc6-107">Il comando sysinfo è un comando di sistema MCI; viene interpretato direttamente da MCI.</span><span class="sxs-lookup"><span data-stu-id="79dc6-107">The sysinfo command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="79dc6-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="79dc6-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a><span data-ttu-id="79dc6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="79dc6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79dc6-110">*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="79dc6-110">*lpszDeviceID*</span></span> 
</dt> <dd>

<span data-ttu-id="79dc6-111">Identificatore di un dispositivo MCI o di un tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79dc6-111">Identifier of an MCI device or device type.</span></span> <span data-ttu-id="79dc6-112">Se viene specificato un tipo di dispositivo, deve trattarsi di un nome di tipo dispositivo MCI standard, come elencato nel materiale di riferimento per il comando [**Capability**](capability.md) .</span><span class="sxs-lookup"><span data-stu-id="79dc6-112">If a device type is specified, it must be a standard MCI device-type name, as listed in the reference material for the [**capability**](capability.md) command.</span></span> <span data-ttu-id="79dc6-113">È possibile specificare "All" quando il flag specificato in *lpszRequest* consente tale possibilità.</span><span class="sxs-lookup"><span data-stu-id="79dc6-113">You can specify "all" when the flag specified in *lpszRequest* allows that possibility.</span></span>

</dd> <dt>

<span data-ttu-id="79dc6-114">*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="79dc6-114">*lpszRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="79dc6-115">Uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="79dc6-115">One of the following flags.</span></span>



| <span data-ttu-id="79dc6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="79dc6-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="79dc6-117">Significato</span><span class="sxs-lookup"><span data-stu-id="79dc6-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <span data-ttu-id="79dc6-118"><dt>**installname**</dt></span><span class="sxs-lookup"><span data-stu-id="79dc6-118"><dt>**installname**</dt></span></span> </dl>               | <span data-ttu-id="79dc6-119">Restituisce il nome elencato nel registro di sistema o il file di SYSTEM.INI usato per installare il dispositivo aperto con l'identificatore di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="79dc6-119">Returns the name listed in the registry or the SYSTEM.INI file used to install the open device with the specified device identifier.</span></span><br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <span data-ttu-id="79dc6-120"><dt>**quantità**</dt></span><span class="sxs-lookup"><span data-stu-id="79dc6-120"><dt>**quantity**</dt></span></span> </dl>                        | <span data-ttu-id="79dc6-121">Restituisce il numero di dispositivi MCI elencati nel registro di sistema o il file di SYSTEM.INI del tipo specificato nel parametro *lpszDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="79dc6-121">Returns the number of MCI devices listed in the registry or the SYSTEM.INI file of the type specified in the *lpszDeviceID* parameter.</span></span> <span data-ttu-id="79dc6-122">Questo identificatore di dispositivo deve essere un nome di tipo dispositivo MCI standard.</span><span class="sxs-lookup"><span data-stu-id="79dc6-122">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="79dc6-123">Eventuali cifre dopo il tipo di dispositivo verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="79dc6-123">Any digits after the device type are ignored.</span></span> <span data-ttu-id="79dc6-124">Se si specifica "All" per *lpszDeviceID* , viene restituito il numero totale di dispositivi MCI nel sistema.</span><span class="sxs-lookup"><span data-stu-id="79dc6-124">Specifying "all" for *lpszDeviceID* returns the total number of MCI devices in the system.</span></span><br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <span data-ttu-id="79dc6-125"><dt>**quantità aperta**</dt></span><span class="sxs-lookup"><span data-stu-id="79dc6-125"><dt>**quantity open**</dt></span></span> </dl>         | <span data-ttu-id="79dc6-126">Restituisce il numero di dispositivi Open MCI del tipo specificato in *lpszDeviceID*.</span><span class="sxs-lookup"><span data-stu-id="79dc6-126">Returns the number of open MCI devices of the type specified in *lpszDeviceID*.</span></span> <span data-ttu-id="79dc6-127">Questo identificatore di dispositivo deve essere un nome di tipo dispositivo MCI standard.</span><span class="sxs-lookup"><span data-stu-id="79dc6-127">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="79dc6-128">Se si specifica "All" per *lpszDeviceID* , viene restituito il numero totale di dispositivi Open MCI presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="79dc6-128">Specifying "all" for *lpszDeviceID* returns the total number of open MCI devices in the system.</span></span><br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <span data-ttu-id="79dc6-129"><dt>\* \* name \* index \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="79dc6-129"><dt>\*\*name \*index\*\*\*</dt></span></span> </dl>                | <span data-ttu-id="79dc6-130">Restituisce il nome di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="79dc6-130">Returns the name of an MCI device.</span></span> <span data-ttu-id="79dc6-131">L'identificatore del dispositivo deve essere un nome di tipo dispositivo MCI standard.</span><span class="sxs-lookup"><span data-stu-id="79dc6-131">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="79dc6-132">L' *Indice* è compreso tra 1 e il numero di dispositivi di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="79dc6-132">The *index* ranges from 1 to the number of devices of that type.</span></span> <span data-ttu-id="79dc6-133">Se per *lpszDeviceID* è specificato "All", *index* è compreso tra 1 e il numero totale di dispositivi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="79dc6-133">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of devices in the system.</span></span><br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <span data-ttu-id="79dc6-134"><dt>***Indice* nome aperto**</dt></span><span class="sxs-lookup"><span data-stu-id="79dc6-134"><dt>**name *index* open**</dt></span></span> </dl> | <span data-ttu-id="79dc6-135">Restituisce il nome di un dispositivo MCI aperto.</span><span class="sxs-lookup"><span data-stu-id="79dc6-135">Returns the name of an open MCI device.</span></span> <span data-ttu-id="79dc6-136">L'identificatore del dispositivo deve essere un nome di tipo dispositivo MCI standard.</span><span class="sxs-lookup"><span data-stu-id="79dc6-136">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="79dc6-137">L' *Indice* è compreso tra 1 e il numero di dispositivi aperti del tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79dc6-137">The *index* ranges from 1 to the number of open devices of that device type.</span></span> <span data-ttu-id="79dc6-138">Se per *lpszDeviceID* è specificato "All", *index* è compreso tra 1 e il numero totale di dispositivi aperti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="79dc6-138">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of open devices in the system.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="79dc6-139">*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="79dc6-139">*lpszFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="79dc6-140">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="79dc6-140">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="79dc6-141">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="79dc6-141">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="79dc6-142">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="79dc6-142">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="79dc6-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="79dc6-143">Examples</span></span>

<span data-ttu-id="79dc6-144">Il comando seguente restituisce il numero di dispositivi audio e di forma d'onda aperti.</span><span class="sxs-lookup"><span data-stu-id="79dc6-144">The following command returns the number of open waveform-audio devices.</span></span>

``` syntax
sysinfo waveaudio quantity open
```

<span data-ttu-id="79dc6-145">Il comando che segue restituisce il nome (alias del dispositivo) del primo dispositivo Open Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="79dc6-145">The following command returns the name (device alias) of the first open waveform-audio device.</span></span>

``` syntax
sysinfo waveaudio name 1 open
```

## <a name="requirements"></a><span data-ttu-id="79dc6-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79dc6-146">Requirements</span></span>



| <span data-ttu-id="79dc6-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="79dc6-147">Requirement</span></span> | <span data-ttu-id="79dc6-148">Valore</span><span class="sxs-lookup"><span data-stu-id="79dc6-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="79dc6-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79dc6-149">Minimum supported client</span></span><br/> | <span data-ttu-id="79dc6-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="79dc6-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="79dc6-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79dc6-151">Minimum supported server</span></span><br/> | <span data-ttu-id="79dc6-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="79dc6-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="79dc6-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79dc6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79dc6-154">MCI</span><span class="sxs-lookup"><span data-stu-id="79dc6-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="79dc6-155">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="79dc6-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="79dc6-156">**funzionalità**</span><span class="sxs-lookup"><span data-stu-id="79dc6-156">**capability**</span></span>](capability.md)
</dt> </dl>

 

