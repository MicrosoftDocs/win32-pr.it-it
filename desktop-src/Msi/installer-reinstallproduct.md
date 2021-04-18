---
description: Il metodo ReinstallProduct dell'oggetto Installer reinstalla un prodotto o corregge i problemi di installazione in un prodotto installato.
ms.assetid: ff933cce-9f27-4215-9291-dd860d9c4d08
title: Installer. ReinstallProduct, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1570f5a0dc607b4a011a5b4276a243c59a64392d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329125"
---
# <a name="installerreinstallproduct-method"></a><span data-ttu-id="8a7c7-103">Installer. ReinstallProduct, metodo</span><span class="sxs-lookup"><span data-stu-id="8a7c7-103">Installer.ReinstallProduct method</span></span>

<span data-ttu-id="8a7c7-104">Il metodo **ReinstallProduct** dell'oggetto [**Installer**](installer-object.md) reinstalla un prodotto o corregge i problemi di installazione in un prodotto installato.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-104">The **ReinstallProduct** method of the [**Installer**](installer-object.md) object reinstalls a product or corrects installation problems in an installed product.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a7c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a7c7-105">Syntax</span></span>


```JScript
Installer.ReinstallProduct(
  Product,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="8a7c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a7c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a7c7-107">*Prodotto*</span><span class="sxs-lookup"><span data-stu-id="8a7c7-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="8a7c7-108">Specifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c7-109">*ReinstallMode*</span><span class="sxs-lookup"><span data-stu-id="8a7c7-109">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="8a7c7-110">Specifica il tipo di reinstallazione.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-110">Specifies the type of reinstallation.</span></span> <span data-ttu-id="8a7c7-111">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="8a7c7-112">Valore</span><span class="sxs-lookup"><span data-stu-id="8a7c7-112">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="8a7c7-113">Significato</span><span class="sxs-lookup"><span data-stu-id="8a7c7-113">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="8a7c7-114"><dt>**msiReinstallModeFileMissing**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7c7-114"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="8a7c7-115">Reinstalla solo se il file è mancante.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-115">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="8a7c7-116"><dt>**msiReinstallModeFileOlderVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7c7-116"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="8a7c7-117">Reinstalla se il file è mancante o è una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-117">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="8a7c7-118"><dt>**msiReinstallModeFileEqualVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7c7-118"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="8a7c7-119">Reinstalla se il file è mancante o è una versione uguale o precedente.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-119">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="8a7c7-120"><dt>**msiReinstallModeFileExact**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7c7-120"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="8a7c7-121">Reinstalla se il file è mancante o non è una versione esatta.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-121">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="8a7c7-122"><dt>**msiReinstallModeFileVerify**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7c7-122"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="8a7c7-123">Verifica i file eseguibili Sum e li reinstalla se sono mancanti o danneggiati.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-123">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="8a7c7-124"><dt>**msiReinstallModeFileReplace**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7c7-124"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="8a7c7-125">Reinstalla tutti i file indipendentemente dalla versione.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-125">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="8a7c7-126"><dt>**msiReinstallModeUserData**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7c7-126"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="8a7c7-127">Assicura le voci del registro di sistema obbligatorie per = utente.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-127">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="8a7c7-128"><dt>**msiReinstallModeMachineData**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7c7-128"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="8a7c7-129">Verifica che le voci del registro di sistema necessarie per = computer.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-129">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="8a7c7-130"><dt>**msiReinstallModeShortcut**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7c7-130"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="8a7c7-131">Convalida i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-131">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="8a7c7-132"><dt>**msiReinstallModePackage**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7c7-132"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="8a7c7-133">Usa l'origine della ricache per installare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-133">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a7c7-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a7c7-134">Return value</span></span>

<span data-ttu-id="8a7c7-135">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-135">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a7c7-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a7c7-136">Requirements</span></span>



| <span data-ttu-id="8a7c7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a7c7-137">Requirement</span></span> | <span data-ttu-id="8a7c7-138">Valore</span><span class="sxs-lookup"><span data-stu-id="8a7c7-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a7c7-139">Versione</span><span class="sxs-lookup"><span data-stu-id="8a7c7-139">Version</span></span><br/> | <span data-ttu-id="8a7c7-140">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-140">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8a7c7-141">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8a7c7-141">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8a7c7-142">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="8a7c7-142">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8a7c7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="8a7c7-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="8a7c7-144"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a7c7-144"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8a7c7-145">IID</span><span class="sxs-lookup"><span data-stu-id="8a7c7-145">IID</span></span><br/>     | <span data-ttu-id="8a7c7-146">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8a7c7-146">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="8a7c7-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a7c7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a7c7-148">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="8a7c7-148">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
</dt> <dt>

[<span data-ttu-id="8a7c7-149">Funzioni di installazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="8a7c7-149">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




