---
title: Classe Win32_RDSHCollection
description: Gestisce una raccolta di Desktop remoto host sessione.
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDSHCollection Servizi Desktop remoto
- Classe Win32_RDSHCollection Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477080"
---
# <a name="win32_rdshcollection-class"></a><span data-ttu-id="5ecf9-105">Win32 \_ RDSHCollection (classe)</span><span class="sxs-lookup"><span data-stu-id="5ecf9-105">Win32\_RDSHCollection class</span></span>

<span data-ttu-id="5ecf9-106">Gestisce una raccolta di Desktop remoto host sessione.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-106">Manages a collection of Remote Desktop Session Hosts.</span></span>

<span data-ttu-id="5ecf9-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ecf9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ecf9-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="5ecf9-109">Members</span><span class="sxs-lookup"><span data-stu-id="5ecf9-109">Members</span></span>

<span data-ttu-id="5ecf9-110">La classe **Win32 \_ RDSHCollection** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5ecf9-110">The **Win32\_RDSHCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="5ecf9-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="5ecf9-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="5ecf9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ecf9-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5ecf9-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="5ecf9-113">Methods</span></span>

<span data-ttu-id="5ecf9-114">La classe **Win32 \_ RDSHCollection** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-114">The **Win32\_RDSHCollection** class has these methods.</span></span>



| <span data-ttu-id="5ecf9-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="5ecf9-115">Method</span></span>                                                                      | <span data-ttu-id="5ecf9-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ecf9-116">Description</span></span>                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ecf9-117">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-117">**GetInt32Property**</span></span>](getint32property-win32-rdshcollection.md)           | <span data-ttu-id="5ecf9-118">Recupera un valore di proprietà Integer di un oggetto **Win32 \_ RDSHCollection** .</span><span class="sxs-lookup"><span data-stu-id="5ecf9-118">Retrieves an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="5ecf9-119">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-119">**GetStringProperty**</span></span>](getstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="5ecf9-120">Recupera un valore della proprietà di stringa di un oggetto **Win32 \_ RDSHCollection** .</span><span class="sxs-lookup"><span data-stu-id="5ecf9-120">Retrieves a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="5ecf9-121">**KeyValueCompareAndSet**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-121">**KeyValueCompareAndSet**</span></span>](win32-rdshcollection-keyvaluecompareandset.md) | <span data-ttu-id="5ecf9-122">Confronta la chiave specificata nella raccolta con un comparand; Se corrispondono, la chiave viene impostata su un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-122">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="5ecf9-123">Se la chiave non esiste, il metodo inserirà la chiave nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-123">If the key does not exist, the method will insert the key into the collection.</span></span><br/> |
| [<span data-ttu-id="5ecf9-124">**KeyValueDelete**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-124">**KeyValueDelete**</span></span>](win32-rdshcollection-keyvaluedelete.md)               | <span data-ttu-id="5ecf9-125">Elimina dalla raccolta la chiave specificata e il valore associato.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-125">Deletes the specified key (and associated value) from the collection.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="5ecf9-126">**KeyValueGet**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-126">**KeyValueGet**</span></span>](win32-rdshcollection-keyvalueget.md)                     | <span data-ttu-id="5ecf9-127">Recupera il valore associato alla chiave specificata nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-127">Retrieves the value associated with the specified key in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="5ecf9-128">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-128">**SetInt32Property**</span></span>](setint32property-win32-rdshcollection.md)           | <span data-ttu-id="5ecf9-129">Aggiorna un valore della proprietà Integer di un oggetto **Win32 \_ RDSHCollection** .</span><span class="sxs-lookup"><span data-stu-id="5ecf9-129">Updates an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="5ecf9-130">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-130">**SetStringProperty**</span></span>](setstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="5ecf9-131">Aggiorna il valore di una proprietà di stringa di un oggetto **Win32 \_ RDSHCollection** .</span><span class="sxs-lookup"><span data-stu-id="5ecf9-131">Updates a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="5ecf9-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ecf9-132">Properties</span></span>

<span data-ttu-id="5ecf9-133">La classe **Win32 \_ RDSHCollection** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-133">The **Win32\_RDSHCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ecf9-134">**Alias**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-134">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecf9-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecf9-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ecf9-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ecf9-137">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5ecf9-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5ecf9-138">Ottiene e imposta l'alias della raccolta.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-138">Gets and sets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="5ecf9-139">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecf9-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecf9-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ecf9-141">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ecf9-142">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5ecf9-142">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5ecf9-143">Ottiene e imposta la descrizione della raccolta.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-143">Gets and sets the description of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="5ecf9-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecf9-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ecf9-146">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ecf9-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ecf9-147">Ottiene e imposta il nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-147">Gets and sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="5ecf9-148">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-148">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ecf9-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5ecf9-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ecf9-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ecf9-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ecf9-151">**Windows server 2012 R2 e Windows server 2012:** Questa proprietà non è disponibile prima di Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-151">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

<span data-ttu-id="5ecf9-152">Tipo della raccolta.</span><span class="sxs-lookup"><span data-stu-id="5ecf9-152">The type of collection.</span></span>

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="5ecf9-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Normale** (0)</span><span class="sxs-lookup"><span data-stu-id="5ecf9-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Regular** (0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ecf9-154">(2)</span><span class="sxs-lookup"><span data-stu-id="5ecf9-154">(2)</span></span>


</dt> <dd>

<span data-ttu-id="5ecf9-155">Riservato</span><span class="sxs-lookup"><span data-stu-id="5ecf9-155">Reserved</span></span>

</dd> <dt>



 <span data-ttu-id="5ecf9-156">(3)</span><span class="sxs-lookup"><span data-stu-id="5ecf9-156">(3)</span></span>


</dt> <dd>

<span data-ttu-id="5ecf9-157">Riservato</span><span class="sxs-lookup"><span data-stu-id="5ecf9-157">Reserved</span></span>

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span data-ttu-id="5ecf9-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)</span><span class="sxs-lookup"><span data-stu-id="5ecf9-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span data-ttu-id="5ecf9-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**Autopersonal** (5)</span><span class="sxs-lookup"><span data-stu-id="5ecf9-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**AutoPersonal** (5)</span></span>


<span data-ttu-id="5ecf9-160"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5ecf9-160"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5ecf9-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ecf9-161">Requirements</span></span>



| <span data-ttu-id="5ecf9-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ecf9-162">Requirement</span></span> | <span data-ttu-id="5ecf9-163">Valore</span><span class="sxs-lookup"><span data-stu-id="5ecf9-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ecf9-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ecf9-164">Minimum supported client</span></span><br/> | <span data-ttu-id="5ecf9-165">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5ecf9-165">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5ecf9-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ecf9-166">Minimum supported server</span></span><br/> | <span data-ttu-id="5ecf9-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ecf9-167">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5ecf9-168">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5ecf9-168">Namespace</span></span><br/>                | <span data-ttu-id="5ecf9-169">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="5ecf9-169">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5ecf9-170">MOF</span><span class="sxs-lookup"><span data-stu-id="5ecf9-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ecf9-171"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ecf9-171"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ecf9-172">DLL</span><span class="sxs-lookup"><span data-stu-id="5ecf9-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ecf9-173"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ecf9-173"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5ecf9-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ecf9-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ecf9-175">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="5ecf9-175">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

