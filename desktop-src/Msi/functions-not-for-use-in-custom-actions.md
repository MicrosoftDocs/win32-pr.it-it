---
description: Le funzioni di database seguenti non devono mai essere chiamate da un'azione personalizzata.
ms.assetid: 55fdd82b-9f34-4c2c-a837-8a09f21f568a
title: Funzioni non utilizzabili in azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c77c4714ca65614200cf77d6b207b6eebcaf179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314270"
---
# <a name="functions-not-for-use-in-custom-actions"></a><span data-ttu-id="55c6c-103">Funzioni non utilizzabili in azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="55c6c-103">Functions Not for Use in Custom Actions</span></span>

<span data-ttu-id="55c6c-104">Le [funzioni di database](database-functions.md) seguenti non devono mai essere chiamate da un'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="55c6c-104">The following [Database Functions](database-functions.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="55c6c-105">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="55c6c-105">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="55c6c-106">**MsiConfigureProductEx**</span><span class="sxs-lookup"><span data-stu-id="55c6c-106">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="55c6c-107">**MsiCreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="55c6c-107">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)
-   [<span data-ttu-id="55c6c-108">**MsiDatabaseApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="55c6c-108">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)
-   [<span data-ttu-id="55c6c-109">**MsiDatabaseCommit**</span><span class="sxs-lookup"><span data-stu-id="55c6c-109">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)
-   [<span data-ttu-id="55c6c-110">**MsiDatabaseExport**</span><span class="sxs-lookup"><span data-stu-id="55c6c-110">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)
-   [<span data-ttu-id="55c6c-111">**MsiDatabaseGenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="55c6c-111">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)
-   [<span data-ttu-id="55c6c-112">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="55c6c-112">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   [<span data-ttu-id="55c6c-113">**MsiDatabaseMerge**</span><span class="sxs-lookup"><span data-stu-id="55c6c-113">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)
-   [<span data-ttu-id="55c6c-114">**MsiEnableLog**</span><span class="sxs-lookup"><span data-stu-id="55c6c-114">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="55c6c-115">**MsiEnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="55c6c-115">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
-   [<span data-ttu-id="55c6c-116">**MsiGetDatabaseState**</span><span class="sxs-lookup"><span data-stu-id="55c6c-116">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)
-   [<span data-ttu-id="55c6c-117">**MsiOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="55c6c-117">**MsiOpenDatabase**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
-   [<span data-ttu-id="55c6c-118">**MsiPreviewBillboard**</span><span class="sxs-lookup"><span data-stu-id="55c6c-118">**MsiPreviewBillboard**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)
-   [<span data-ttu-id="55c6c-119">**MsiPreviewDialog**</span><span class="sxs-lookup"><span data-stu-id="55c6c-119">**MsiPreviewDialog**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
-   [<span data-ttu-id="55c6c-120">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="55c6c-120">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="55c6c-121">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="55c6c-121">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="55c6c-122">**MsiSetExternalUIRecord**</span><span class="sxs-lookup"><span data-stu-id="55c6c-122">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="55c6c-123">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="55c6c-123">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

<span data-ttu-id="55c6c-124">Le seguenti [funzioni del programma di installazione](installer-function-reference.md) non devono mai essere chiamate da un'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="55c6c-124">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="55c6c-125">**MsiApplyPatch**</span><span class="sxs-lookup"><span data-stu-id="55c6c-125">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [<span data-ttu-id="55c6c-126">**MsiCollectUserInfo**</span><span class="sxs-lookup"><span data-stu-id="55c6c-126">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
-   [<span data-ttu-id="55c6c-127">**MsiConfigureFeature**</span><span class="sxs-lookup"><span data-stu-id="55c6c-127">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
-   [<span data-ttu-id="55c6c-128">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="55c6c-128">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="55c6c-129">**MsiConfigureProductEx**</span><span class="sxs-lookup"><span data-stu-id="55c6c-129">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="55c6c-130">**MsiEnableLog**</span><span class="sxs-lookup"><span data-stu-id="55c6c-130">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="55c6c-131">**MsiGetFeatureInfo**</span><span class="sxs-lookup"><span data-stu-id="55c6c-131">**MsiGetFeatureInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
-   [<span data-ttu-id="55c6c-132">**MsiGetProductCode**</span><span class="sxs-lookup"><span data-stu-id="55c6c-132">**MsiGetProductCode**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)
-   [<span data-ttu-id="55c6c-133">**MsiGetProductProperty**</span><span class="sxs-lookup"><span data-stu-id="55c6c-133">**MsiGetProductProperty**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)
-   [<span data-ttu-id="55c6c-134">**MsiInstallMissingComponent**</span><span class="sxs-lookup"><span data-stu-id="55c6c-134">**MsiInstallMissingComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)
-   [<span data-ttu-id="55c6c-135">**MsiInstallMissingFile**</span><span class="sxs-lookup"><span data-stu-id="55c6c-135">**MsiInstallMissingFile**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)
-   [<span data-ttu-id="55c6c-136">**MsiInstallProduct**</span><span class="sxs-lookup"><span data-stu-id="55c6c-136">**MsiInstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
-   [<span data-ttu-id="55c6c-137">**MsiOpenPackage**</span><span class="sxs-lookup"><span data-stu-id="55c6c-137">**MsiOpenPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)
-   [<span data-ttu-id="55c6c-138">**MsiOpenProduct**</span><span class="sxs-lookup"><span data-stu-id="55c6c-138">**MsiOpenProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenproducta)
-   [<span data-ttu-id="55c6c-139">**MsiReinstallFeature**</span><span class="sxs-lookup"><span data-stu-id="55c6c-139">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   [<span data-ttu-id="55c6c-140">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="55c6c-140">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="55c6c-141">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="55c6c-141">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="55c6c-142">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="55c6c-142">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
-   [<span data-ttu-id="55c6c-143">**MsiUseFeature**</span><span class="sxs-lookup"><span data-stu-id="55c6c-143">**MsiUseFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
-   [<span data-ttu-id="55c6c-144">**MsiUseFeatureEx**</span><span class="sxs-lookup"><span data-stu-id="55c6c-144">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
-   [<span data-ttu-id="55c6c-145">**MsiVerifyPackage**</span><span class="sxs-lookup"><span data-stu-id="55c6c-145">**MsiVerifyPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)

<span data-ttu-id="55c6c-146">Le seguenti [funzioni del programma di installazione](installer-function-reference.md) non devono mai essere chiamate da un'azione personalizzata se viene avviata un'altra installazione.</span><span class="sxs-lookup"><span data-stu-id="55c6c-146">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action if doing so starts another installation.</span></span> <span data-ttu-id="55c6c-147">Possono essere chiamati da un'azione personalizzata che non avvia un'altra installazione.</span><span class="sxs-lookup"><span data-stu-id="55c6c-147">They may be called from a custom action that does not start another installation.</span></span>

-   [<span data-ttu-id="55c6c-148">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="55c6c-148">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
-   [<span data-ttu-id="55c6c-149">**MsiProvideQualifiedComponent**</span><span class="sxs-lookup"><span data-stu-id="55c6c-149">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
-   [<span data-ttu-id="55c6c-150">**MsiProvideQualifiedComponentEx**</span><span class="sxs-lookup"><span data-stu-id="55c6c-150">**MsiProvideQualifiedComponentEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

<span data-ttu-id="55c6c-151">Un'azione personalizzata non deve mai generare un nuovo thread che usa Windows Installer funzioni per modificare lo stato della funzionalità, lo stato del componente o per inviare messaggi da un evento di controllo.</span><span class="sxs-lookup"><span data-stu-id="55c6c-151">A custom action should never spawn a new thread that uses Windows Installer functions to change the feature state, component state, or to send messages from a Control Event.</span></span> <span data-ttu-id="55c6c-152">Il tentativo di eseguire questa operazione comporta l'esito negativo dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="55c6c-152">Attempting to do this causes the installation to fail.</span></span>

 

 



