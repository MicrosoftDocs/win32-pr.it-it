---
title: Classe Win32_RDMSPublishedApplication
description: Gestisce un'applicazione pubblicata.
ms.assetid: 7a529f1d-1aaf-42fb-8469-92d38a7b0ffc
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSPublishedApplication Servizi Desktop remoto
- Classe Win32_RDMSPublishedApplication Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSPublishedApplication
- Win32_RDMSPublishedApplication.AppAlias
- Win32_RDMSPublishedApplication.PoolName
- Win32_RDMSPublishedApplication.DisplayName
- Win32_RDMSPublishedApplication.ShowInPortal
- Win32_RDMSPublishedApplication.SecurityDescriptor
- Win32_RDMSPublishedApplication.AppPath
- Win32_RDMSPublishedApplication.VirtualPath
- Win32_RDMSPublishedApplication.CommandLineSetting
- Win32_RDMSPublishedApplication.RequiredCommandLine
- Win32_RDMSPublishedApplication.Folder
- Win32_RDMSPublishedApplication.IconPath
- Win32_RDMSPublishedApplication.IconIndex
- Win32_RDMSPublishedApplication.IconContents
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb003faf5e51c9da1f46f23c5f8d6b5ae977987c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341123"
---
# <a name="win32_rdmspublishedapplication-class"></a><span data-ttu-id="eed3a-105">Win32 \_ RDMSPublishedApplication (classe)</span><span class="sxs-lookup"><span data-stu-id="eed3a-105">Win32\_RDMSPublishedApplication class</span></span>

<span data-ttu-id="eed3a-106">Gestisce un'applicazione pubblicata.</span><span class="sxs-lookup"><span data-stu-id="eed3a-106">Manages a published application.</span></span>

<span data-ttu-id="eed3a-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="eed3a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed3a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eed3a-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSPublishedApplication
{
  string  AppAlias;
  string  PoolName;
  string  DisplayName;
  boolean ShowInPortal;
  string  SecurityDescriptor;
  string  AppPath;
  string  VirtualPath;
  uint32  CommandLineSetting;
  string  RequiredCommandLine;
  string  Folder;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
};
```

## <a name="members"></a><span data-ttu-id="eed3a-109">Members</span><span class="sxs-lookup"><span data-stu-id="eed3a-109">Members</span></span>

<span data-ttu-id="eed3a-110">La classe **Win32 \_ RDMSPublishedApplication** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="eed3a-110">The **Win32\_RDMSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="eed3a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eed3a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eed3a-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eed3a-112">Properties</span></span>

<span data-ttu-id="eed3a-113">La classe **Win32 \_ RDMSPublishedApplication** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="eed3a-113">The **Win32\_RDMSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eed3a-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="eed3a-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eed3a-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-117">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eed3a-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-118">Ottiene e imposta l'alias dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eed3a-118">Gets and sets the alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="eed3a-119">**AppPath**</span><span class="sxs-lookup"><span data-stu-id="eed3a-119">**AppPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eed3a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-122">Ottiene e imposta il percorso dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eed3a-122">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="eed3a-123">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="eed3a-123">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eed3a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-126">Ottiene e imposta l'impostazione della riga di comando per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eed3a-126">Gets and sets the command line setting for the application.</span></span>

<span data-ttu-id="eed3a-127">Questa proprietà può essere impostata su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="eed3a-127">This property can be set to one of the following values:</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="eed3a-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span><span class="sxs-lookup"><span data-stu-id="eed3a-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="eed3a-129">Non consentire argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="eed3a-129">Do not allow command line arguments.</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="eed3a-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Consenti** (1)</span><span class="sxs-lookup"><span data-stu-id="eed3a-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eed3a-131">Consente argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="eed3a-131">Allow command line arguments.</span></span>

</dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="eed3a-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Richiedi** (2)</span><span class="sxs-lookup"><span data-stu-id="eed3a-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eed3a-133">Richiedere argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="eed3a-133">Require command line arguments.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eed3a-134">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="eed3a-134">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eed3a-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-137">Ottiene e imposta il nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eed3a-137">Gets and sets the display name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="eed3a-138">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="eed3a-138">**Folder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eed3a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-141">Ottiene e imposta il percorso dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eed3a-141">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="eed3a-142">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="eed3a-142">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-143">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="eed3a-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-145">Ottiene e imposta una matrice che contiene l'icona dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eed3a-145">Gets and sets an array that contains the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="eed3a-146">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="eed3a-146">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eed3a-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-149">Ottiene e imposta l'indice per l'icona dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eed3a-149">Gets and sets the index for the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="eed3a-150">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="eed3a-150">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eed3a-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-153">Ottiene e imposta il percorso dell'icona per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eed3a-153">Gets and sets the path to the icon for this application.</span></span>

</dd> <dt>

<span data-ttu-id="eed3a-154">**PoolName**</span><span class="sxs-lookup"><span data-stu-id="eed3a-154">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eed3a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-156">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-157">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eed3a-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-158">Ottiene e imposta il nome del pool di applicazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eed3a-158">Gets and sets the name of the application pool of the application.</span></span>

</dd> <dt>

<span data-ttu-id="eed3a-159">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="eed3a-159">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eed3a-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-161">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-161">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-162">Ottiene e imposta gli argomenti della riga di comando necessari per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eed3a-162">Gets and sets the command line arguments that are required for the application</span></span>

</dd> <dt>

<span data-ttu-id="eed3a-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="eed3a-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eed3a-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-166">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eed3a-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-167">Ottiene e imposta il descrittore di sicurezza che controlla l'accesso all'applicazione nel formato SDDL (Security Descriptor Definition Language).</span><span class="sxs-lookup"><span data-stu-id="eed3a-167">Gets and sets the security descriptor that controls access to the application, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="eed3a-168">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="eed3a-168">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-169">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="eed3a-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-170">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-171">Indica se visualizzare l'applicazione in Servizi terminal Accesso Web (Accesso Web TS).</span><span class="sxs-lookup"><span data-stu-id="eed3a-171">Indicates whether to display the application in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="eed3a-172">**True** per visualizzare l'applicazione in accesso Web di Servizi terminal; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="eed3a-172">**TRUE** to display the application in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eed3a-173">**VirtualPath**</span><span class="sxs-lookup"><span data-stu-id="eed3a-173">**VirtualPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eed3a-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eed3a-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eed3a-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="eed3a-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eed3a-176">Ottiene e imposta il percorso virtuale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eed3a-176">Gets and sets the virtual path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eed3a-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eed3a-177">Requirements</span></span>



| <span data-ttu-id="eed3a-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="eed3a-178">Requirement</span></span> | <span data-ttu-id="eed3a-179">Valore</span><span class="sxs-lookup"><span data-stu-id="eed3a-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eed3a-180">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eed3a-180">Minimum supported client</span></span><br/> | <span data-ttu-id="eed3a-181">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="eed3a-181">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="eed3a-182">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eed3a-182">Minimum supported server</span></span><br/> | <span data-ttu-id="eed3a-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eed3a-183">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="eed3a-184">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eed3a-184">Namespace</span></span><br/>                | <span data-ttu-id="eed3a-185">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="eed3a-185">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="eed3a-186">MOF</span><span class="sxs-lookup"><span data-stu-id="eed3a-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eed3a-187"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eed3a-187"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="eed3a-188">DLL</span><span class="sxs-lookup"><span data-stu-id="eed3a-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eed3a-189"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eed3a-189"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="eed3a-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eed3a-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed3a-191">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="eed3a-191">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

