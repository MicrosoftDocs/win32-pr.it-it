---
title: Classe Win32_RDMSFileTypeAssociation
description: Gestisce un'associazione del tipo di file per un'applicazione pubblicata.
ms.assetid: 22c945cb-4c47-431a-bc9b-d33ba15c8ab3
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSFileTypeAssociation Servizi Desktop remoto
- Classe Win32_RDMSFileTypeAssociation Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSFileTypeAssociation
- Win32_RDMSFileTypeAssociation.AppAlias
- Win32_RDMSFileTypeAssociation.PoolName
- Win32_RDMSFileTypeAssociation.ExtName
- Win32_RDMSFileTypeAssociation.ProgIdHint
- Win32_RDMSFileTypeAssociation.IconPath
- Win32_RDMSFileTypeAssociation.IconIndex
- Win32_RDMSFileTypeAssociation.IconContents
- Win32_RDMSFileTypeAssociation.IsPrimaryHandler
- Win32_RDMSFileTypeAssociation.IsPublished
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2e569077bf47a2b0eba63db39ae1e86c39feb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400277"
---
# <a name="win32_rdmsfiletypeassociation-class"></a><span data-ttu-id="6ec84-105">Win32 \_ RDMSFileTypeAssociation (classe)</span><span class="sxs-lookup"><span data-stu-id="6ec84-105">Win32\_RDMSFileTypeAssociation class</span></span>

<span data-ttu-id="6ec84-106">Gestisce un'associazione del tipo di file per un'applicazione pubblicata.</span><span class="sxs-lookup"><span data-stu-id="6ec84-106">Manages a file type association for a published application.</span></span>

<span data-ttu-id="6ec84-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6ec84-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec84-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ec84-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSFileTypeAssociation
{
  string  AppAlias;
  string  PoolName;
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean IsPrimaryHandler;
  boolean IsPublished;
};
```

## <a name="members"></a><span data-ttu-id="6ec84-109">Members</span><span class="sxs-lookup"><span data-stu-id="6ec84-109">Members</span></span>

<span data-ttu-id="6ec84-110">La classe **Win32 \_ RDMSFileTypeAssociation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6ec84-110">The **Win32\_RDMSFileTypeAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="6ec84-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6ec84-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ec84-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6ec84-112">Properties</span></span>

<span data-ttu-id="6ec84-113">La classe **Win32 \_ RDMSFileTypeAssociation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6ec84-113">The **Win32\_RDMSFileTypeAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ec84-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="6ec84-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec84-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6ec84-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ec84-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6ec84-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6ec84-117">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6ec84-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6ec84-118">Ottiene e imposta l'alias dell'applicazione associata al tipo di file.</span><span class="sxs-lookup"><span data-stu-id="6ec84-118">Gets and sets the alias of the application that is associated with the file type.</span></span>

</dd> <dt>

<span data-ttu-id="6ec84-119">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="6ec84-119">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec84-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6ec84-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ec84-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6ec84-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ec84-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6ec84-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6ec84-123">Ottiene il nome dell'estensione di file.</span><span class="sxs-lookup"><span data-stu-id="6ec84-123">Gets the name of the file extension.</span></span>

</dd> <dt>

<span data-ttu-id="6ec84-124">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="6ec84-124">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec84-125">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6ec84-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6ec84-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6ec84-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6ec84-127">Ottiene e imposta il contenuto dell'icona per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="6ec84-127">Gets and sets the content of the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="6ec84-128">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="6ec84-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec84-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6ec84-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ec84-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6ec84-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6ec84-131">Ottiene e imposta l'indice dell'icona per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="6ec84-131">Gets and sets the index to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="6ec84-132">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="6ec84-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec84-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6ec84-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ec84-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6ec84-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6ec84-135">Ottiene e imposta il percorso dell'icona per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="6ec84-135">Gets and sets the path to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="6ec84-136">**IsPrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="6ec84-136">**IsPrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec84-137">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6ec84-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ec84-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6ec84-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6ec84-139">Ottiene e imposta un valore che indica se l'associazione del tipo di file è per il gestore primario.</span><span class="sxs-lookup"><span data-stu-id="6ec84-139">Gets and sets a value that indicates whether the file type association is for the primary handler.</span></span> <span data-ttu-id="6ec84-140">**True** se l'associazione del tipo di file è per il gestore primario. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6ec84-140">**TRUE** if the file type association is for the primary handler; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6ec84-141">**IsPublished**</span><span class="sxs-lookup"><span data-stu-id="6ec84-141">**IsPublished**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec84-142">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6ec84-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ec84-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6ec84-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6ec84-144">Indica se questo FTA è pubblicato.</span><span class="sxs-lookup"><span data-stu-id="6ec84-144">Whether this FTA is published.</span></span>

<span data-ttu-id="6ec84-145">Ottiene e imposta un valore che indica se l'associazione del tipo di file è pubblicata.</span><span class="sxs-lookup"><span data-stu-id="6ec84-145">Gets and sets a value that indicates whether the file type association is published.</span></span> <span data-ttu-id="6ec84-146">**True** se l'associazione del tipo di file è pubblicata; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6ec84-146">**TRUE** if the file type association is published; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6ec84-147">**PoolName**</span><span class="sxs-lookup"><span data-stu-id="6ec84-147">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec84-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6ec84-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ec84-149">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6ec84-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6ec84-150">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6ec84-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6ec84-151">Ottiene e imposta il nome del pool di applicazioni per l'associazione del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="6ec84-151">Gets and sets the name of the application pool for the file type association.</span></span>

</dd> <dt>

<span data-ttu-id="6ec84-152">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="6ec84-152">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec84-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6ec84-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ec84-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6ec84-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ec84-155">Ottiene un hint che consente agli utenti di aprire l'estensione di file.</span><span class="sxs-lookup"><span data-stu-id="6ec84-155">Gets a hint to help users open the file extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ec84-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ec84-156">Requirements</span></span>



| <span data-ttu-id="6ec84-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec84-157">Requirement</span></span> | <span data-ttu-id="6ec84-158">Valore</span><span class="sxs-lookup"><span data-stu-id="6ec84-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec84-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ec84-159">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec84-160">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6ec84-160">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6ec84-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ec84-161">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec84-162">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ec84-162">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6ec84-163">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6ec84-163">Namespace</span></span><br/>                | <span data-ttu-id="6ec84-164">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="6ec84-164">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6ec84-165">MOF</span><span class="sxs-lookup"><span data-stu-id="6ec84-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ec84-166"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ec84-166"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ec84-167">DLL</span><span class="sxs-lookup"><span data-stu-id="6ec84-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ec84-168"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ec84-168"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6ec84-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ec84-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec84-170">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="6ec84-170">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

