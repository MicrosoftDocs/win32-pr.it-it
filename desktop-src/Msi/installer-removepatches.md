---
description: Il metodo RemovePatches rimuove una o più patch ai prodotti idonei per la ricezione della patch. Il metodo RemovePatches chiama MsiRemovePatches.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Installer. RemovePatches, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2130ae2958f03eb16b5145e5eb61e42f869ad775
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329124"
---
# <a name="installerremovepatches-method"></a><span data-ttu-id="81c5f-104">Installer. RemovePatches, metodo</span><span class="sxs-lookup"><span data-stu-id="81c5f-104">Installer.RemovePatches method</span></span>

<span data-ttu-id="81c5f-105">Il metodo **RemovePatches** rimuove una o più patch ai prodotti idonei per la ricezione della patch.</span><span class="sxs-lookup"><span data-stu-id="81c5f-105">The **RemovePatches** method removes one or more patches to products eligible to receive the patch.</span></span> <span data-ttu-id="81c5f-106">Il metodo **RemovePatches** chiama [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span><span class="sxs-lookup"><span data-stu-id="81c5f-106">The **RemovePatches** method calls [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span>

## <a name="syntax"></a><span data-ttu-id="81c5f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81c5f-107">Syntax</span></span>


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a><span data-ttu-id="81c5f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="81c5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81c5f-109">*Applicazione di patch*</span><span class="sxs-lookup"><span data-stu-id="81c5f-109">*PatchList*</span></span> 
</dt> <dd>

<span data-ttu-id="81c5f-110">Stringa che contiene un elenco delimitato da punti e virgola di patch da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="81c5f-110">A string that contains a semicolon delimited list of patches to remove.</span></span> <span data-ttu-id="81c5f-111">Ogni patch può essere rappresentata dal percorso completo del pacchetto di patch o dal GUID della patch.</span><span class="sxs-lookup"><span data-stu-id="81c5f-111">Each patch can be represented by either the full path to the patch package or by patch GUID.</span></span> <span data-ttu-id="81c5f-112">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="81c5f-112">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="81c5f-113">*ProductCode*</span><span class="sxs-lookup"><span data-stu-id="81c5f-113">*ProductCode*</span></span> 
</dt> <dd>

<span data-ttu-id="81c5f-114">Stringa con il GUID del prodotto da cui devono essere rimosse le patch.</span><span class="sxs-lookup"><span data-stu-id="81c5f-114">A string with the GUID of the product from which the patches are to be removed.</span></span> <span data-ttu-id="81c5f-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="81c5f-115">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="81c5f-116">*UninstallType*</span><span class="sxs-lookup"><span data-stu-id="81c5f-116">*UninstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="81c5f-117">Valore intero che specifica il tipo di rimozione della patch.</span><span class="sxs-lookup"><span data-stu-id="81c5f-117">An integer value that specifies the type of patch removal.</span></span> <span data-ttu-id="81c5f-118">Questo parametro deve essere **msiInstallTypeSingleInstance**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-118">This parameter must be **msiInstallTypeSingleInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="81c5f-119">*PropertyList*</span><span class="sxs-lookup"><span data-stu-id="81c5f-119">*PropertyList*</span></span> 
</dt> <dd>

<span data-ttu-id="81c5f-120">Stringa che specifica le coppie proprietà = valore da includere.</span><span class="sxs-lookup"><span data-stu-id="81c5f-120">A string that specifies the Property=Value pairs to include.</span></span> <span data-ttu-id="81c5f-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="81c5f-121">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81c5f-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81c5f-122">Return value</span></span>

<span data-ttu-id="81c5f-123">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="81c5f-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81c5f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="81c5f-124">Remarks</span></span>

<span data-ttu-id="81c5f-125">Vedere [disinstallazione di patch](uninstalling-patches.md) per un esempio che illustra come un'applicazione può rimuovere una patch da tutti i prodotti disponibili per l'utente.</span><span class="sxs-lookup"><span data-stu-id="81c5f-125">See [Uninstalling Patches](uninstalling-patches.md) for an example that demonstrates how an application can remove a patch from all products that are available to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="81c5f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81c5f-126">Requirements</span></span>



| <span data-ttu-id="81c5f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="81c5f-127">Requirement</span></span> | <span data-ttu-id="81c5f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="81c5f-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81c5f-129">Versione</span><span class="sxs-lookup"><span data-stu-id="81c5f-129">Version</span></span><br/> | <span data-ttu-id="81c5f-130">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="81c5f-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="81c5f-131">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="81c5f-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="81c5f-132">Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="81c5f-132">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="81c5f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="81c5f-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="81c5f-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81c5f-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="81c5f-135">IID</span><span class="sxs-lookup"><span data-stu-id="81c5f-135">IID</span></span><br/>     | <span data-ttu-id="81c5f-136">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="81c5f-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="81c5f-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81c5f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81c5f-138">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="81c5f-138">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="81c5f-139">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="81c5f-139">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[<span data-ttu-id="81c5f-140">Disinstallazione di patch</span><span class="sxs-lookup"><span data-stu-id="81c5f-140">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="81c5f-141">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="81c5f-141">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




