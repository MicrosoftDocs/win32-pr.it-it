---
title: Metodi di proprietà IADsComputer (IADs. h)
description: I metodi dell'interfaccia IADsComputer leggono e scrivono le proprietà descritte in questo argomento. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: c990b6bb-6256-4216-9435-c85c67db4d13
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsComputer ADSI
topic_type:
- apiref
api_name:
- IADsComputer Property Methods
- IADsComputer.ComputerID
- IADsComputer.get_ComputerID
- IADsComputer.Department
- IADsComputer.get_Department
- IADsComputer.put_Department
- IADsComputer.Description
- IADsComputer.get_Description
- IADsComputer.put_Description
- IADsComputer.Division
- IADsComputer.get_Division
- IADsComputer.put_Division
- IADsComputer.Location
- IADsComputer.get_Location
- IADsComputer.put_Location
- IADsComputer.MemorySize
- IADsComputer.get_MemorySize
- IADsComputer.put_MemorySize
- IADsComputer.Model
- IADsComputer.get_Model
- IADsComputer.put_Model
- IADsComputer.NetAddresses
- IADsComputer.get_NetAddresses
- IADsComputer.put_NetAddresses
- IADsComputer.OperatingSystem
- IADsComputer.get_OperatingSystem
- IADsComputer.put_OperatingSystem
- IADsComputer.OperatingSystemVersion
- IADsComputer.get_OperatingSystemVersion
- IADsComputer.put_OperatingSystemVersion
- IADsComputer.Owner
- IADsComputer.get_Owner
- IADsComputer.put_Owner
- IADsComputer.PrimaryUser
- IADsComputer.get_PrimaryUser
- IADsComputer.put_PrimaryUser
- IADsComputer.Processor
- IADsComputer.get_Processor
- IADsComputer.put_Processor
- IADsComputer.ProcessorCount
- IADsComputer.get_ProcessorCount
- IADsComputer.put_ProcessorCount
- IADsComputer.Role
- IADsComputer.get_Role
- IADsComputer.put_Role
- IADsComputer.Site
- IADsComputer.get_Site
- IADsComputer.StorageCapacity
- IADsComputer.get_StorageCapacity
- IADsComputer.put_StorageCapacity
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f3c455e2e43436627b62d142781bb6a605bef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874245"
---
# <a name="iadscomputer-property-methods"></a><span data-ttu-id="cfac9-105">Metodi di proprietà IADsComputer</span><span class="sxs-lookup"><span data-stu-id="cfac9-105">IADsComputer Property Methods</span></span>

<span data-ttu-id="cfac9-106">I metodi dell'interfaccia [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) leggono e scrivono le proprietà descritte in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="cfac9-106">The [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="cfac9-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="cfac9-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="cfac9-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cfac9-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="cfac9-109">**Con informatizzazione**</span><span class="sxs-lookup"><span data-stu-id="cfac9-109">**ComputerID**</span></span>
<span data-ttu-id="cfac9-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-111">Identificatore univoco globale assegnato a ogni computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-111">The globally unique identifier assigned to each computer.</span></span>

<dt>

<span data-ttu-id="cfac9-112">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cfac9-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-113">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerID(
  [out] BSTR* pbstrComputerID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-114">**Reparto**</span><span class="sxs-lookup"><span data-stu-id="cfac9-114">**Department**</span></span>
<span data-ttu-id="cfac9-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-116">Unità organizzativa (OU), ad esempio Department, a cui appartiene il computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-116">The organizational unit (OU), such as department, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="cfac9-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Department(
  [out] BSTR* pbstrDepartment
);
HRESULT put_Department(
  [in] BSTR bstrDepartment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-119">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="cfac9-119">**Description**</span></span>
<span data-ttu-id="cfac9-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-121">Descrizione del computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-121">The description of this computer.</span></span>

<dt>

<span data-ttu-id="cfac9-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-123">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-124">**Divisione**</span><span class="sxs-lookup"><span data-stu-id="cfac9-124">**Division**</span></span>
<span data-ttu-id="cfac9-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-126">Divisione, all'interno di un'organizzazione, a cui appartiene il computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-126">The division, within an organization, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="cfac9-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-128">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Division(
  [out] BSTR* pbstrDivision
);
HRESULT put_Division(
  [in] BSTR bstrDivision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-129">**Posizione**</span><span class="sxs-lookup"><span data-stu-id="cfac9-129">**Location**</span></span>
<span data-ttu-id="cfac9-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-131">Percorso fisico assegnato del computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-131">The assigned physical location of this computer.</span></span>

<dt>

<span data-ttu-id="cfac9-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-133">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-134">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="cfac9-134">**MemorySize**</span></span>
<span data-ttu-id="cfac9-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-136">Dimensioni, in megabyte, della memoria ad accesso casuale per questo computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-136">The size, in megabytes, of random access memory for this computer.</span></span>

<dt>

<span data-ttu-id="cfac9-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-138">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MemorySize(
  [out] BSTR* pbstrMemorySize
);
HRESULT put_MemorySize(
  [in] BSTR bstrMemorySize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-139">**Modello**</span><span class="sxs-lookup"><span data-stu-id="cfac9-139">**Model**</span></span>
<span data-ttu-id="cfac9-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-141">Marca e modello del computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-141">The make and model of this computer.</span></span>

<dt>

<span data-ttu-id="cfac9-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-143">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-144">**NetAddresses**</span><span class="sxs-lookup"><span data-stu-id="cfac9-144">**NetAddresses**</span></span>
<span data-ttu-id="cfac9-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-146">Matrice di campi NetAddress che rappresentano gli indirizzi in base ai quali è possibile raggiungere il computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-146">An array of NetAddress fields that represent the addresses by which this computer can be reached.</span></span> <span data-ttu-id="cfac9-147">NetAddress è un **BSTR** specifico del provider composto da due sottostringhe separate da due punti (:).</span><span class="sxs-lookup"><span data-stu-id="cfac9-147">NetAddress is a provider-specific **BSTR** composed of two substrings separated by a colon (:).</span></span> <span data-ttu-id="cfac9-148">La sottostringa sinistra indica il tipo di indirizzo e la sottostringa destra è una rappresentazione di stringa di un indirizzo di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="cfac9-148">The left substring indicates the address type, and the right substring is a string representation of an address of that type.</span></span> <span data-ttu-id="cfac9-149">Ad esempio, gli indirizzi TCP/IP hanno il formato: IP: 100.201.301.45.</span><span class="sxs-lookup"><span data-stu-id="cfac9-149">For example, TCP/IP addresses are of the form: IP:100.201.301.45.</span></span> <span data-ttu-id="cfac9-150">Il formato degli indirizzi di tipo IPX è IPX: 10.123456.80.</span><span class="sxs-lookup"><span data-stu-id="cfac9-150">IPX type addresses are of the form: IPX:10.123456.80.</span></span>

<dt>

<span data-ttu-id="cfac9-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-152">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="cfac9-152">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NetAddresses(
  [out] VARIANT* pvNetAddresses
);
HRESULT put_NetAddresses(
  [in] VARIANT vNetAddresses
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-153">**OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="cfac9-153">**OperatingSystem**</span></span>
<span data-ttu-id="cfac9-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-155">Sistema operativo utilizzato nel computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-155">The operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="cfac9-156">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-157">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-157">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystem(
  [out] BSTR* pbstrOperatingSystem
);
HRESULT put_OperatingSystem(
  [in] BSTR bstrOperatingSystem
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-158">**OperatingSystemVersion**</span><span class="sxs-lookup"><span data-stu-id="cfac9-158">**OperatingSystemVersion**</span></span>
<span data-ttu-id="cfac9-159"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-159"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-160">Versione del sistema operativo utilizzato nel computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-160">The version of the operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="cfac9-161">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-162">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-162">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystemVersion(
  [out] BSTR* pbstrOperatingSystemVersion
);
HRESULT put_OperatingSystemVersion(
  [in] BSTR bstrOperatingSystemVersion
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-163">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="cfac9-163">**Owner**</span></span>
<span data-ttu-id="cfac9-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-165">Persona a cui viene assegnato il computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-165">The person to whom this computer is assigned.</span></span> <span data-ttu-id="cfac9-166">L'utente deve inoltre disporre di una licenza per eseguire il software installato.</span><span class="sxs-lookup"><span data-stu-id="cfac9-166">This person should also have a license to run the installed software.</span></span>

<dt>

<span data-ttu-id="cfac9-167">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-168">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwner
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-169">**PrimaryUser**</span><span class="sxs-lookup"><span data-stu-id="cfac9-169">**PrimaryUser**</span></span>
<span data-ttu-id="cfac9-170"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-170"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-171">Nome dell'utente del contatto, ad esempio un amministratore, per questo computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-171">The name of the contact person, such as an administrator, for this computer.</span></span>

<dt>

<span data-ttu-id="cfac9-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-173">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-173">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryUser(
  [out] BSTR* pbstrPrimaryUser
);
HRESULT put_PrimaryUser(
  [in] BSTR bstrPrimaryUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-174">**Processore**</span><span class="sxs-lookup"><span data-stu-id="cfac9-174">**Processor**</span></span>
<span data-ttu-id="cfac9-175"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-175"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-176">Tipo di processore.</span><span class="sxs-lookup"><span data-stu-id="cfac9-176">The processor type.</span></span>

<dt>

<span data-ttu-id="cfac9-177">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-177">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-178">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-178">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Processor(
  [out] BSTR* pbstrProcessor
);
HRESULT put_Processor(
  [in] BSTR bstrProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-179">**ProcessorCount**</span><span class="sxs-lookup"><span data-stu-id="cfac9-179">**ProcessorCount**</span></span>
<span data-ttu-id="cfac9-180"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-180"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-181">Numero di processori installati.</span><span class="sxs-lookup"><span data-stu-id="cfac9-181">The number of installed processors.</span></span>

<dt>

<span data-ttu-id="cfac9-182">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-183">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-183">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProcessorCount(
  [out] BSTR* pbstrProcessorCount
);
HRESULT put_ProcessorCount(
  [in] BSTR bstrProcessorCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-184">**Ruolo**</span><span class="sxs-lookup"><span data-stu-id="cfac9-184">**Role**</span></span>
<span data-ttu-id="cfac9-185"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-185"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-186">Ruolo del computer, ad esempio workstation, server o controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="cfac9-186">The role of this computer, for example, workstation, server, or domain controller.</span></span>

<dt>

<span data-ttu-id="cfac9-187">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-187">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-188">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-188">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Role(
  [out] BSTR* pbstrRole
);
HRESULT put_Role(
  [in] BSTR bstrRole
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-189">**Sito**</span><span class="sxs-lookup"><span data-stu-id="cfac9-189">**Site**</span></span>
<span data-ttu-id="cfac9-190"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-190"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-191">Identificatore univoco globale che identifica il sito in cui è stato installato il computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-191">The globally unique identifier that identifies the site that this computer was installed in.</span></span> <span data-ttu-id="cfac9-192">Un sito è un'area fisica di una connettività efficace in una rete.</span><span class="sxs-lookup"><span data-stu-id="cfac9-192">A site is a physical region of good connectivity in a network.</span></span>

<dt>

<span data-ttu-id="cfac9-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cfac9-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-194">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-194">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Site(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cfac9-195">**StorageCapacity**</span><span class="sxs-lookup"><span data-stu-id="cfac9-195">**StorageCapacity**</span></span>
<span data-ttu-id="cfac9-196"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cfac9-196"></dt> <dd> <dl></span></span>

<span data-ttu-id="cfac9-197">Dimensione, in megabyte, del disco.</span><span class="sxs-lookup"><span data-stu-id="cfac9-197">The size, in megabytes, of the disk.</span></span>

<dt>

<span data-ttu-id="cfac9-198">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cfac9-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cfac9-199">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfac9-199">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StorageCapacity(
  [out] BSTR* pbstrStorageCapacity
);
HRESULT put_StorageCapacity(
  [in] BSTR bstrStorageCapacity
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="cfac9-200">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfac9-200">Remarks</span></span>

<span data-ttu-id="cfac9-201">Provider diversi possono scegliere di esporre proprietà diverse di un oggetto computer.</span><span class="sxs-lookup"><span data-stu-id="cfac9-201">Different providers may choose to expose different properties of a computer object.</span></span> <span data-ttu-id="cfac9-202">Per ulteriori informazioni, vedere [provider di sistema ADSI](adsi-system-providers.md).</span><span class="sxs-lookup"><span data-stu-id="cfac9-202">For more information, see [ADSI System Providers](adsi-system-providers.md).</span></span>

<span data-ttu-id="cfac9-203">È possibile individuare le proprietà supportate controllando le proprietà obbligatorie e facoltative tramite la relativa classe dello schema.</span><span class="sxs-lookup"><span data-stu-id="cfac9-203">You can discover what properties are supported by inspecting the mandatory and optional properties through its schema class.</span></span> <span data-ttu-id="cfac9-204">Per ulteriori informazioni, vedere l'interfaccia [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) .</span><span class="sxs-lookup"><span data-stu-id="cfac9-204">For more information, see the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface.</span></span>

<span data-ttu-id="cfac9-205">Per esaminare lo stato di un computer o per eseguire l'operazione di arresto attraverso la rete, è necessario usare l'interfaccia [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) .</span><span class="sxs-lookup"><span data-stu-id="cfac9-205">To examine the status of a computer or to perform the shutdown operation across the network, you must use the [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="cfac9-206">Esempio</span><span class="sxs-lookup"><span data-stu-id="cfac9-206">Examples</span></span>

<span data-ttu-id="cfac9-207">Nell'esempio di codice Visual Basic riportato di seguito vengono esaminate le proprietà del computer supportate dal provider ADSI WinNT.</span><span class="sxs-lookup"><span data-stu-id="cfac9-207">The following Visual Basic code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```VB
Dim obj As IADs
On Error Resume Next

Set obj = GetObject("WinNT://myMachine,computer")
If (obj.Class = "Computer") Then
    MsgBox "Computer owner: " & obj.owner
    MsgBox "Computer division: " & obj.Division
    MsgBox "Computer operatingSystem: " & obj.OperatingSystem
    MsgBox "Computer operating System Version: " & obj.OperatingSystemVersion
    MsgBox "Computer processor: " & obj.Processor
    MsgBox "Computer processor Count: " & obj.ProcessorCount
End If
```



<span data-ttu-id="cfac9-208">Nell'esempio di codice C++ riportato di seguito vengono esaminate le proprietà del computer supportate dal provider ADSI WinNT.</span><span class="sxs-lookup"><span data-stu-id="cfac9-208">The following C++ code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```C++
IADsComputer *pComp = NULL;
LPWSTR adspath = L"WinNT://jeffsmith1,computer";
HRESULT hr = S_OK;
BSTR bstr = NULL;

hr = ADsGetObject(adspath,IID_IADsComputer,(void**)&pComp);
if(FAILED(hr)) {goto Cleanup;}

hr = pComp->get_Owner(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Computer owner: %S\n",bstr);
SysFreeString(bstr);

hr = pComp->get_OperatingSystem(&bstr);
if(FAILED(hr)) {goto Cleanup;}
printf("Operating System: %S\n",bstr);
SysFreeString(bstr);

Cleanup:
    if(pComp) pComp->Release();
    if(bstr) SysFreeString(bstr);
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="cfac9-209">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfac9-209">Requirements</span></span>



| <span data-ttu-id="cfac9-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfac9-210">Requirement</span></span> | <span data-ttu-id="cfac9-211">Valore</span><span class="sxs-lookup"><span data-stu-id="cfac9-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfac9-212">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfac9-212">Minimum supported client</span></span><br/> | <span data-ttu-id="cfac9-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cfac9-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cfac9-214">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfac9-214">Minimum supported server</span></span><br/> | <span data-ttu-id="cfac9-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfac9-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cfac9-216">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfac9-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfac9-217"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfac9-217"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="cfac9-218">DLL</span><span class="sxs-lookup"><span data-stu-id="cfac9-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfac9-219"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfac9-219"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="cfac9-220">IID</span><span class="sxs-lookup"><span data-stu-id="cfac9-220">IID</span></span><br/>                      | <span data-ttu-id="cfac9-221">IID \_ IADsComputer è definito come EFE3CC70-1D9F-11CF-B1F3-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="cfac9-221">IID\_IADsComputer is defined as EFE3CC70-1D9F-11CF-B1F3-02608C9E7553</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="cfac9-222">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfac9-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfac9-223">**IADsComputer**</span><span class="sxs-lookup"><span data-stu-id="cfac9-223">**IADsComputer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputer)
</dt> <dt>

[<span data-ttu-id="cfac9-224">Provider di sistema ADSI</span><span class="sxs-lookup"><span data-stu-id="cfac9-224">ADSI System Providers</span></span>](adsi-system-providers.md)
</dt> <dt>

[<span data-ttu-id="cfac9-225">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="cfac9-225">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="cfac9-226">**IADsComputerOperations**</span><span class="sxs-lookup"><span data-stu-id="cfac9-226">**IADsComputerOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)
</dt> <dt>

[<span data-ttu-id="cfac9-227">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="cfac9-227">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





