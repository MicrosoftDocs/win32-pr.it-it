---
title: Classe Win32_RDMSDeploymentSettings
description: Gestisce le impostazioni di distribuzione per un insieme di desktop virtuali.
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517625"
---
# <a name="win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="53e62-105">Win32 \_ RDMSDeploymentSettings (classe)</span><span class="sxs-lookup"><span data-stu-id="53e62-105">Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="53e62-106">Gestisce le impostazioni di distribuzione per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-106">Manages deployment settings for a virtual desktop collection.</span></span>

<span data-ttu-id="53e62-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="53e62-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="53e62-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53e62-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a><span data-ttu-id="53e62-109">Members</span><span class="sxs-lookup"><span data-stu-id="53e62-109">Members</span></span>

<span data-ttu-id="53e62-110">La classe **Win32 \_ RDMSDeploymentSettings** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="53e62-110">The **Win32\_RDMSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="53e62-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="53e62-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="53e62-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="53e62-112">Methods</span></span>

<span data-ttu-id="53e62-113">La classe **Win32 \_ RDMSDeploymentSettings** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="53e62-113">The **Win32\_RDMSDeploymentSettings** class has these methods.</span></span>



| <span data-ttu-id="53e62-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="53e62-114">Method</span></span>                                                                                                  | <span data-ttu-id="53e62-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53e62-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53e62-116">**GetBaseVHDPath**</span><span class="sxs-lookup"><span data-stu-id="53e62-116">**GetBaseVHDPath**</span></span>](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="53e62-117">Recupera il percorso di base della directory in cui vengono distribuiti i VHD dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-117">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="53e62-118">**GetConnectionString**</span><span class="sxs-lookup"><span data-stu-id="53e62-118">**GetConnectionString**</span></span>](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | <span data-ttu-id="53e62-119">Recupera la stringa di connessione del database a livello di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="53e62-119">Retrieves the deployment-level database connection string.</span></span><br/>                                                             |
| [<span data-ttu-id="53e62-120">**GetDiffVHDPath**</span><span class="sxs-lookup"><span data-stu-id="53e62-120">**GetDiffVHDPath**</span></span>](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="53e62-121">Recupera il percorso della directory in cui vengono distribuiti i dischi differenze per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-121">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>            |
| [<span data-ttu-id="53e62-122">**GetExportPath**</span><span class="sxs-lookup"><span data-stu-id="53e62-122">**GetExportPath**</span></span>](getexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="53e62-123">Recupera il percorso della directory in cui vengono distribuite le macchine virtuali per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-123">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                  |
| [<span data-ttu-id="53e62-124">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="53e62-124">**GetInt32Property**</span></span>](getint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="53e62-125">Recupera una proprietà integer per le impostazioni di distribuzione di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-125">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                             |
| [<span data-ttu-id="53e62-126">**GetSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="53e62-126">**GetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | <span data-ttu-id="53e62-127">Recupera la stringa di connessione secondaria del database a livello di distribuzione, che può essere utilizzata per supportare la scadenza della password.</span><span class="sxs-lookup"><span data-stu-id="53e62-127">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span><br/> |
| [<span data-ttu-id="53e62-128">**GetSMBPath**</span><span class="sxs-lookup"><span data-stu-id="53e62-128">**GetSMBPath**</span></span>](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="53e62-129">Recupera il percorso UNC della condivisione SMB a cui vengono distribuite le macchine virtuali dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-129">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>      |
| [<span data-ttu-id="53e62-130">**GetStringArrayDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="53e62-130">**GetStringArrayDeploymentSetting**</span></span>](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="53e62-131">Recupera le impostazioni di distribuzione per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-131">Retrieves the deployment settings for a virtual desktop collection.</span></span><br/>                                                    |
| [<span data-ttu-id="53e62-132">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="53e62-132">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="53e62-133">Recupera una proprietà di stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-133">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="53e62-134">**RemoveDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="53e62-134">**RemoveDeploymentSetting**</span></span>](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | <span data-ttu-id="53e62-135">Elimina le impostazioni di distribuzione per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-135">Deletes the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="53e62-136">**SetBaseVHDPath**</span><span class="sxs-lookup"><span data-stu-id="53e62-136">**SetBaseVHDPath**</span></span>](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="53e62-137">Recupera il percorso di base della directory in cui vengono distribuiti i VHD dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-137">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="53e62-138">**SetConnectionString**</span><span class="sxs-lookup"><span data-stu-id="53e62-138">**SetConnectionString**</span></span>](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | <span data-ttu-id="53e62-139">Imposta la stringa di connessione del database a livello di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="53e62-139">Sets the deployment-level database connection string.</span></span><br/>                                                                  |
| [<span data-ttu-id="53e62-140">**SetDiffVHDPath**</span><span class="sxs-lookup"><span data-stu-id="53e62-140">**SetDiffVHDPath**</span></span>](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="53e62-141">Aggiorna il percorso della directory in cui vengono distribuiti i dischi differenze per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-141">Updates the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>              |
| [<span data-ttu-id="53e62-142">**SetExportPath**</span><span class="sxs-lookup"><span data-stu-id="53e62-142">**SetExportPath**</span></span>](setexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="53e62-143">Aggiorna il percorso della directory in cui vengono distribuite le macchine virtuali per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-143">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                    |
| [<span data-ttu-id="53e62-144">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="53e62-144">**SetInt32Property**</span></span>](setint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="53e62-145">Aggiorna una proprietà integer per le impostazioni di distribuzione di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-145">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="53e62-146">**SetSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="53e62-146">**SetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | <span data-ttu-id="53e62-147">Imposta la stringa di connessione secondaria del database a livello di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="53e62-147">Sets the deployment-level database secondary connection string.</span></span><br/>                                                        |
| [<span data-ttu-id="53e62-148">**SetSMBPath**</span><span class="sxs-lookup"><span data-stu-id="53e62-148">**SetSMBPath**</span></span>](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="53e62-149">Aggiorna il percorso UNC della condivisione SMB a cui vengono distribuite le macchine virtuali dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-149">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>        |
| [<span data-ttu-id="53e62-150">**SetStringArrayDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="53e62-150">**SetStringArrayDeploymentSetting**</span></span>](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="53e62-151">Aggiorna le impostazioni di distribuzione per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-151">Updates the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="53e62-152">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="53e62-152">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="53e62-153">Aggiorna una proprietà di stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="53e62-153">Updates a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="53e62-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53e62-154">Requirements</span></span>



| <span data-ttu-id="53e62-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="53e62-155">Requirement</span></span> | <span data-ttu-id="53e62-156">Valore</span><span class="sxs-lookup"><span data-stu-id="53e62-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="53e62-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53e62-157">Minimum supported client</span></span><br/> | <span data-ttu-id="53e62-158">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="53e62-158">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="53e62-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53e62-159">Minimum supported server</span></span><br/> | <span data-ttu-id="53e62-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53e62-160">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="53e62-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="53e62-161">Namespace</span></span><br/>                | <span data-ttu-id="53e62-162">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="53e62-162">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="53e62-163">MOF</span><span class="sxs-lookup"><span data-stu-id="53e62-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53e62-164"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53e62-164"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="53e62-165">DLL</span><span class="sxs-lookup"><span data-stu-id="53e62-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53e62-166"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53e62-166"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="53e62-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53e62-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e62-168">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="53e62-168">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





