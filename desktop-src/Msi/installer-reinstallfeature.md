---
description: Il metodo ReinstallFeature dell'oggetto del programma di installazione Reinstalla le funzionalità o corregge i problemi con le funzionalità installate.
ms.assetid: cfe2aef4-7742-49cd-b7a3-7d484e1f85e3
title: Installer. ReinstallFeature, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6bac008ee7121bbcb985b9a8ff5ba02df122266
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332168"
---
# <a name="installerreinstallfeature-method"></a><span data-ttu-id="711fb-103">Installer. ReinstallFeature, metodo</span><span class="sxs-lookup"><span data-stu-id="711fb-103">Installer.ReinstallFeature method</span></span>

<span data-ttu-id="711fb-104">Il metodo **ReinstallFeature** dell'oggetto del [**programma di installazione**](installer-object.md) reinstalla le funzionalità o corregge i problemi con le funzionalità installate.</span><span class="sxs-lookup"><span data-stu-id="711fb-104">The **ReinstallFeature** method of the [**Installer**](installer-object.md) object reinstalls features or corrects problems with installed features.</span></span>

## <a name="syntax"></a><span data-ttu-id="711fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="711fb-105">Syntax</span></span>


```JScript
Installer.ReinstallFeature(
  Product,
  Feature,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="711fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="711fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711fb-107">*Prodotto*</span><span class="sxs-lookup"><span data-stu-id="711fb-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="711fb-108">Specifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="711fb-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="711fb-109">*Funzionalità*</span><span class="sxs-lookup"><span data-stu-id="711fb-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="711fb-110">Specifica la funzionalità da reinstallare.</span><span class="sxs-lookup"><span data-stu-id="711fb-110">Specifies the feature to be reinstalled.</span></span> <span data-ttu-id="711fb-111">La funzionalità padre o la funzionalità figlio della funzionalità specificata non è stata reinstallata.</span><span class="sxs-lookup"><span data-stu-id="711fb-111">The parent feature or child feature of the specified feature is not reinstalled.</span></span> <span data-ttu-id="711fb-112">Per reinstallare la funzionalità padre o figlio, è necessario chiamare il metodo **ReinstallFeature** per ogni separatamente oppure usare il metodo [**ReinstallProduct**](installer-reinstallproduct.md) .</span><span class="sxs-lookup"><span data-stu-id="711fb-112">To reinstall the parent or child feature, you must call the **ReinstallFeature** method for each separately or use the [**ReinstallProduct**](installer-reinstallproduct.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="711fb-113">*ReinstallMode*</span><span class="sxs-lookup"><span data-stu-id="711fb-113">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="711fb-114">Specifica il tipo di reinstallazione.</span><span class="sxs-lookup"><span data-stu-id="711fb-114">Specifies the type of reinstallation.</span></span> <span data-ttu-id="711fb-115">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="711fb-115">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="711fb-116">Valore</span><span class="sxs-lookup"><span data-stu-id="711fb-116">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="711fb-117">Significato</span><span class="sxs-lookup"><span data-stu-id="711fb-117">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="711fb-118"><dt>**msiReinstallModeFileMissing**</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-118"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="711fb-119">Reinstalla solo se il file è mancante.</span><span class="sxs-lookup"><span data-stu-id="711fb-119">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="711fb-120"><dt>**msiReinstallModeFileOlderVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-120"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="711fb-121">Reinstalla se il file è mancante o è una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="711fb-121">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="711fb-122"><dt>**msiReinstallModeFileEqualVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-122"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="711fb-123">Reinstalla se il file è mancante o è una versione uguale o precedente.</span><span class="sxs-lookup"><span data-stu-id="711fb-123">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="711fb-124"><dt>**msiReinstallModeFileExact**</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-124"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="711fb-125">Reinstalla se il file è mancante o non è una versione esatta.</span><span class="sxs-lookup"><span data-stu-id="711fb-125">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="711fb-126"><dt>**msiReinstallModeFileVerify**</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-126"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="711fb-127">Verifica i file eseguibili Sum e li reinstalla se sono mancanti o danneggiati.</span><span class="sxs-lookup"><span data-stu-id="711fb-127">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="711fb-128"><dt>**msiReinstallModeFileReplace**</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-128"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="711fb-129">Reinstalla tutti i file indipendentemente dalla versione.</span><span class="sxs-lookup"><span data-stu-id="711fb-129">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="711fb-130"><dt>**msiReinstallModeUserData**</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-130"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="711fb-131">Assicura le voci del registro di sistema obbligatorie per = utente.</span><span class="sxs-lookup"><span data-stu-id="711fb-131">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="711fb-132"><dt>**msiReinstallModeMachineData**</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-132"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="711fb-133">Verifica che le voci del registro di sistema necessarie per = computer.</span><span class="sxs-lookup"><span data-stu-id="711fb-133">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="711fb-134"><dt>**msiReinstallModeShortcut**</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-134"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="711fb-135">Convalida i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="711fb-135">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="711fb-136"><dt>**msiReinstallModePackage**</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-136"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="711fb-137">Usa l'origine della ricache per installare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="711fb-137">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711fb-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="711fb-138">Return value</span></span>

<span data-ttu-id="711fb-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="711fb-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="711fb-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="711fb-140">Requirements</span></span>



| <span data-ttu-id="711fb-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="711fb-141">Requirement</span></span> | <span data-ttu-id="711fb-142">Valore</span><span class="sxs-lookup"><span data-stu-id="711fb-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="711fb-143">Versione</span><span class="sxs-lookup"><span data-stu-id="711fb-143">Version</span></span><br/> | <span data-ttu-id="711fb-144">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="711fb-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="711fb-145">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="711fb-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="711fb-146">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="711fb-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="711fb-147">DLL</span><span class="sxs-lookup"><span data-stu-id="711fb-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="711fb-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="711fb-149">IID</span><span class="sxs-lookup"><span data-stu-id="711fb-149">IID</span></span><br/>     | <span data-ttu-id="711fb-150">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="711fb-150">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="711fb-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="711fb-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711fb-152">**MsiReinstallFeature**</span><span class="sxs-lookup"><span data-stu-id="711fb-152">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
</dt> <dt>

[<span data-ttu-id="711fb-153">Funzioni di installazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="711fb-153">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




