---
title: Oggetti ADSI di WinNT
description: Il provider ADSI WinNT implementa gli oggetti COM seguenti per supportare le funzionalità e i servizi di diverse interfacce ADSI.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- Provider di servizi WinNT ADSI, oggetti ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d0c9e5c486d07e1e392a9f307ecd9af4509ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116697"
---
# <a name="adsi-objects-of-winnt"></a><span data-ttu-id="3698b-104">Oggetti ADSI di WinNT</span><span class="sxs-lookup"><span data-stu-id="3698b-104">ADSI Objects of WinNT</span></span>

<span data-ttu-id="3698b-105">Il provider ADSI WinNT implementa gli oggetti COM seguenti per supportare le funzionalità e i servizi di diverse interfacce ADSI.</span><span class="sxs-lookup"><span data-stu-id="3698b-105">The ADSI WinNT provider implement the following COM objects to support features and services of various ADSI interfaces.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3698b-106">ADSI (oggetto)</span><span class="sxs-lookup"><span data-stu-id="3698b-106">ADSI Object</span></span></th>
<th><span data-ttu-id="3698b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3698b-107">Description</span></span></th>
<th><span data-ttu-id="3698b-108">Interfacce supportate</span><span class="sxs-lookup"><span data-stu-id="3698b-108">Supported Interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3698b-109"><strong>Classe</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-109"><strong>Class</strong></span></span></td>
<td><span data-ttu-id="3698b-110">Oggetto ADSI che rappresenta una definizione di classe.</span><span class="sxs-lookup"><span data-stu-id="3698b-110">An ADSI object that represents a class definition.</span></span></td>
<td><dl> <span data-ttu-id="3698b-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"> <strong>IADsClass</strong> IADs</a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>IADsClass</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-112"><strong>Computer</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-112"><strong>Computer</strong></span></span></td>
<td><span data-ttu-id="3698b-113">Oggetto ADSI che rappresenta un computer.</span><span class="sxs-lookup"><span data-stu-id="3698b-113">An ADSI object that represents a computer.</span></span></td>
<td><dl> <span data-ttu-id="3698b-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-115"><strong>Dominio</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-115"><strong>Domain</strong></span></span></td>
<td><span data-ttu-id="3698b-116">Oggetto ADSI che rappresenta un dominio nella rete.</span><span class="sxs-lookup"><span data-stu-id="3698b-116">An ADSI object that represents a domain over the network.</span></span></td>
<td><dl> <span data-ttu-id="3698b-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-118"><strong>FileService</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-118"><strong>FileService</strong></span></span></td>
<td><span data-ttu-id="3698b-119">Oggetto ADSI che rappresenta un servizio file.</span><span class="sxs-lookup"><span data-stu-id="3698b-119">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="3698b-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-121"><strong>FileShare</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-121"><strong>FileShare</strong></span></span></td>
<td><span data-ttu-id="3698b-122">Oggetto ADSI che rappresenta una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3698b-122">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="3698b-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-124"><strong>FPNWFileService</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-124"><strong>FPNWFileService</strong></span></span></td>
<td><span data-ttu-id="3698b-125">Oggetto ADSI che rappresenta un servizio file.</span><span class="sxs-lookup"><span data-stu-id="3698b-125">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="3698b-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-127"><strong>FPNWFileShare</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-127"><strong>FPNWFileShare</strong></span></span></td>
<td><span data-ttu-id="3698b-128">Oggetto ADSI che rappresenta una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3698b-128">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="3698b-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-130"><strong>FPNWResource</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-130"><strong>FPNWResource</strong></span></span></td>
<td><span data-ttu-id="3698b-131">Oggetto ADSI che rappresenta una risorsa.</span><span class="sxs-lookup"><span data-stu-id="3698b-131">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="3698b-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-133"><strong>FPNWResourcesCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-133"><strong>FPNWResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="3698b-134">Oggetto ADSI che rappresenta una raccolta di risorse.</span><span class="sxs-lookup"><span data-stu-id="3698b-134">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="3698b-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3698b-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-136"><strong>FPNWSession</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-136"><strong>FPNWSession</strong></span></span></td>
<td><span data-ttu-id="3698b-137">Oggetto ADSI che rappresenta una sessione.</span><span class="sxs-lookup"><span data-stu-id="3698b-137">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="3698b-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-139"><strong>FPNWSessionsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-139"><strong>FPNWSessionsCollection</strong></span></span></td>
<td><span data-ttu-id="3698b-140">Oggetto ADSI che rappresenta una raccolta di sessioni.</span><span class="sxs-lookup"><span data-stu-id="3698b-140">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="3698b-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3698b-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-142"><strong>Gruppo</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-142"><strong>Group</strong></span></span></td>
<td><span data-ttu-id="3698b-143">Oggetto ADSI che rappresenta un gruppo.</span><span class="sxs-lookup"><span data-stu-id="3698b-143">An ADSI object that represents a group.</span></span></td>
<td><dl> <span data-ttu-id="3698b-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl>
<blockquote>
[!Note]<br />
<span data-ttu-id="3698b-145">Impossibile utilizzare GetInfo per i gruppi che contengono membri che sono entità di sicurezza nota nell'ambito WinNT.</span><span class="sxs-lookup"><span data-stu-id="3698b-145">GetInfo cannot be used for groups that contain members that are wellKnown security principals in the WinNT scope.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-146"><strong>GroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-146"><strong>GroupCollection</strong></span></span></td>
<td><span data-ttu-id="3698b-147">Oggetto ADSI che rappresenta una raccolta di gruppi.</span><span class="sxs-lookup"><span data-stu-id="3698b-147">An ADSI object that represents a collection of groups.</span></span></td>
<td><dl> <span data-ttu-id="3698b-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong> IADs</a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-149"><strong>LocalGroup</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-149"><strong>LocalGroup</strong></span></span></td>
<td><span data-ttu-id="3698b-150">Oggetto ADSI che rappresenta un gruppo locale.</span><span class="sxs-lookup"><span data-stu-id="3698b-150">An ADSI object that represents a local group.</span></span></td>
<td><dl> <span data-ttu-id="3698b-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-152"><strong>LocalgroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-152"><strong>LocalgroupCollection</strong></span></span></td>
<td><span data-ttu-id="3698b-153">Oggetto ADSI che rappresenta una raccolta di gruppi locali.</span><span class="sxs-lookup"><span data-stu-id="3698b-153">An ADSI object that represents a collection of local groups.</span></span></td>
<td><dl> <span data-ttu-id="3698b-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong> IADs</a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-155"><strong>Namespace</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-155"><strong>Namespace</strong></span></span></td>
<td><span data-ttu-id="3698b-156">Oggetto ADSI che rappresenta lo spazio dei nomi WinNT.</span><span class="sxs-lookup"><span data-stu-id="3698b-156">An ADSI object that represents the WinNT namespace.</span></span></td>
<td><dl> <span data-ttu-id="3698b-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-158"><strong>PrintJob</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-158"><strong>PrintJob</strong></span></span></td>
<td><span data-ttu-id="3698b-159">Oggetto ADSI che rappresenta un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="3698b-159">An ADSI object that represents a print job.</span></span></td>
<td><dl> <span data-ttu-id="3698b-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-161"><strong>PrintJobsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-161"><strong>PrintJobsCollection</strong></span></span></td>
<td><span data-ttu-id="3698b-162">Oggetto ADSI che rappresenta una raccolta di processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="3698b-162">An ADSI object that represents a collection of print jobs.</span></span></td>
<td><span data-ttu-id="3698b-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3698b-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-164"><strong>PrintQueue</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-164"><strong>PrintQueue</strong></span></span></td>
<td><span data-ttu-id="3698b-165">Oggetto ADSI che rappresenta una coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="3698b-165">An ADSI object that represents a print queue.</span></span></td>
<td><dl> <span data-ttu-id="3698b-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-167"><strong>Proprietà</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-167"><strong>Property</strong></span></span></td>
<td><span data-ttu-id="3698b-168">Oggetto ADSI che rappresenta una definizione di attributo.</span><span class="sxs-lookup"><span data-stu-id="3698b-168">An ADSI object that represents an attribute definition.</span></span></td>
<td><dl> <span data-ttu-id="3698b-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>IADsProperty</strong> IADs</a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"><strong>IADsProperty</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-170"><strong>Risorsa</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-170"><strong>Resource</strong></span></span></td>
<td><span data-ttu-id="3698b-171">Oggetto ADSI che rappresenta una risorsa.</span><span class="sxs-lookup"><span data-stu-id="3698b-171">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="3698b-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-173"><strong>ResourceCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-173"><strong>ResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="3698b-174">Oggetto ADSI che rappresenta una raccolta di risorse.</span><span class="sxs-lookup"><span data-stu-id="3698b-174">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="3698b-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3698b-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-176"><strong>Schema</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-176"><strong>Schema</strong></span></span></td>
<td><span data-ttu-id="3698b-177">Oggetto ADSI che rappresenta il contenitore dello schema.</span><span class="sxs-lookup"><span data-stu-id="3698b-177">An ADSI object that represents the schema container.</span></span></td>
<td><dl> <span data-ttu-id="3698b-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>IADsContainer</strong> IADs</a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-179"><strong>Servizio</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-179"><strong>Service</strong></span></span></td>
<td><span data-ttu-id="3698b-180">Oggetto ADSI che rappresenta un servizio.</span><span class="sxs-lookup"><span data-stu-id="3698b-180">An ADSI object that represents a service.</span></span></td>
<td><dl> <span data-ttu-id="3698b-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-182"><strong>Sessione</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-182"><strong>Session</strong></span></span></td>
<td><span data-ttu-id="3698b-183">Oggetto ADSI che rappresenta una sessione.</span><span class="sxs-lookup"><span data-stu-id="3698b-183">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="3698b-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-185"><strong>SessionCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-185"><strong>SessionsCollection</strong></span></span></td>
<td><span data-ttu-id="3698b-186">Oggetto ADSI che rappresenta una raccolta di sessioni.</span><span class="sxs-lookup"><span data-stu-id="3698b-186">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="3698b-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3698b-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-188"><strong>Sintassi</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-188"><strong>Syntax</strong></span></span></td>
<td><span data-ttu-id="3698b-189">Oggetto ADSI che rappresenta la sintassi di un attributo.</span><span class="sxs-lookup"><span data-stu-id="3698b-189">An ADSI object that represents the syntax of an attribute.</span></span></td>
<td><dl> <span data-ttu-id="3698b-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong></strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>IADsSyntax</strong> IADs</a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"><strong>IADsSyntax</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3698b-191"><strong>Utente</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-191"><strong>User</strong></span></span></td>
<td><span data-ttu-id="3698b-192">Oggetto ADSI che rappresenta un account utente.</span><span class="sxs-lookup"><span data-stu-id="3698b-192">An ADSI object that represents a user account.</span></span></td>
<td><dl> <span data-ttu-id="3698b-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="3698b-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3698b-194"><strong>UserGroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3698b-194"><strong>UserGroupCollection</strong></span></span></td>
<td><span data-ttu-id="3698b-195">Oggetto ADSI che rappresenta una raccolta di gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="3698b-195">An ADSI object that represents a collection of user groups.</span></span></td>
<td><span data-ttu-id="3698b-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></span><span class="sxs-lookup"><span data-stu-id="3698b-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





