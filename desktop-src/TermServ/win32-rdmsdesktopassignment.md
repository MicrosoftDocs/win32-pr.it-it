---
title: Classe Win32_RDMSDesktopAssignment
description: Descrive l'assegnazione del desktop utente della raccolta desktop remoto.
ms.assetid: d3370cf2-65db-4e01-9ea3-9a71340bf71b
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSDesktopAssignment Servizi Desktop remoto
- Classe Win32_RDMSDesktopAssignment Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment.CollectionAlias
- Win32_RDMSDesktopAssignment.DesktopName
- Win32_RDMSDesktopAssignment.UserName
- Win32_RDMSDesktopAssignment.UserDomain
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72bb252bd2efb71e3192ebd16160cecf18196cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340653"
---
# <a name="win32_rdmsdesktopassignment-class"></a><span data-ttu-id="0e8a1-105">Win32 \_ RDMSDesktopAssignment (classe)</span><span class="sxs-lookup"><span data-stu-id="0e8a1-105">Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="0e8a1-106">Descrive l'assegnazione del desktop utente della raccolta desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0e8a1-106">Describes the RD collection User Desktop assignment.</span></span>

<span data-ttu-id="0e8a1-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0e8a1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e8a1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e8a1-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDesktopAssignment
{
  string CollectionAlias;
  string DesktopName;
  string UserName;
  string UserDomain;
};
```

## <a name="members"></a><span data-ttu-id="0e8a1-109">Members</span><span class="sxs-lookup"><span data-stu-id="0e8a1-109">Members</span></span>

<span data-ttu-id="0e8a1-110">La classe **Win32 \_ RDMSDesktopAssignment** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0e8a1-110">The **Win32\_RDMSDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="0e8a1-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="0e8a1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="0e8a1-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e8a1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0e8a1-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="0e8a1-113">Methods</span></span>

<span data-ttu-id="0e8a1-114">La classe **Win32 \_ RDMSDesktopAssignment** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0e8a1-114">The **Win32\_RDMSDesktopAssignment** class has these methods.</span></span>



| <span data-ttu-id="0e8a1-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="0e8a1-115">Method</span></span>                                                                                 | <span data-ttu-id="0e8a1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e8a1-116">Description</span></span>                              |
|:---------------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="0e8a1-117">**AddDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="0e8a1-117">**AddDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-adddesktopassignment.md)       | <span data-ttu-id="0e8a1-118">Aggiunge un'assegnazione desktop.</span><span class="sxs-lookup"><span data-stu-id="0e8a1-118">Adds a desktop assignment.</span></span><br/>    |
| [<span data-ttu-id="0e8a1-119">**RemoveDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="0e8a1-119">**RemoveDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-removedesktopassignment.md) | <span data-ttu-id="0e8a1-120">Rimuove un'assegnazione desktop.</span><span class="sxs-lookup"><span data-stu-id="0e8a1-120">Removes a desktop assignment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0e8a1-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e8a1-121">Properties</span></span>

<span data-ttu-id="0e8a1-122">La classe **Win32 \_ RDMSDesktopAssignment** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0e8a1-122">The **Win32\_RDMSDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e8a1-123">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="0e8a1-123">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e8a1-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e8a1-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e8a1-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0e8a1-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0e8a1-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0e8a1-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0e8a1-127">Alias della raccolta.</span><span class="sxs-lookup"><span data-stu-id="0e8a1-127">Alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="0e8a1-128">**Desktopname**</span><span class="sxs-lookup"><span data-stu-id="0e8a1-128">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e8a1-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e8a1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e8a1-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0e8a1-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0e8a1-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0e8a1-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0e8a1-132">Nome del desktop.</span><span class="sxs-lookup"><span data-stu-id="0e8a1-132">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="0e8a1-133">**UserDomain**</span><span class="sxs-lookup"><span data-stu-id="0e8a1-133">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e8a1-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e8a1-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e8a1-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0e8a1-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0e8a1-136">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0e8a1-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0e8a1-137">Nome di dominio dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="0e8a1-137">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="0e8a1-138">**UserName**</span><span class="sxs-lookup"><span data-stu-id="0e8a1-138">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e8a1-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e8a1-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e8a1-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0e8a1-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0e8a1-141">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0e8a1-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0e8a1-142">Nome dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="0e8a1-142">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e8a1-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e8a1-143">Requirements</span></span>



| <span data-ttu-id="0e8a1-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e8a1-144">Requirement</span></span> | <span data-ttu-id="0e8a1-145">Valore</span><span class="sxs-lookup"><span data-stu-id="0e8a1-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e8a1-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e8a1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0e8a1-147">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0e8a1-147">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0e8a1-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e8a1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0e8a1-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0e8a1-149">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="0e8a1-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0e8a1-150">Namespace</span></span><br/>                | <span data-ttu-id="0e8a1-151">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="0e8a1-151">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0e8a1-152">MOF</span><span class="sxs-lookup"><span data-stu-id="0e8a1-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e8a1-153"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e8a1-153"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e8a1-154">DLL</span><span class="sxs-lookup"><span data-stu-id="0e8a1-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e8a1-155"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e8a1-155"><dt>RDMS.dll</dt></span></span> </dl>         |



 

