---
description: Rappresenta un set di componenti che funzionano come una singola entità di alto livello.
ms.assetid: 784cee32-e0ae-4632-8dac-e5110513f5c9
title: Classe CIM_System (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerName
- CIM_System.PrimaryOwnerContact
- CIM_System.Roles
- CIM_System.OtherIdentifyingInfo
- CIM_System.IdentifyingDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a51e56ad3e8f91200fbe5bc7e09ac2f14c4ee232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310580"
---
# <a name="cim_system-class-hyper-v-management"></a><span data-ttu-id="c2aa2-103">Classe CIM_System (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="c2aa2-103">CIM_System class (Hyper-V management)</span></span>

<span data-ttu-id="c2aa2-104">Rappresenta un set di componenti che funzionano come una singola entità di alto livello.</span><span class="sxs-lookup"><span data-stu-id="c2aa2-104">Represents a set of components that function as a single high-level entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2aa2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2aa2-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_System : CIM_EnabledLogicalElement
{
  string CreationClassName;
  string Name;
  string NameFormat;
  string PrimaryOwnerName;
  string PrimaryOwnerContact;
  string Roles[];
  string OtherIdentifyingInfo[];
  string IdentifyingDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="c2aa2-106">Members</span><span class="sxs-lookup"><span data-stu-id="c2aa2-106">Members</span></span>

<span data-ttu-id="c2aa2-107">La classe di **\_ sistema CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c2aa2-107">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="c2aa2-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c2aa2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2aa2-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c2aa2-109">Properties</span></span>

<span data-ttu-id="c2aa2-110">La classe di **\_ sistema CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c2aa2-110">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2aa2-111">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2aa2-112">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2aa2-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-114">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c2aa2-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c2aa2-115">Nome della classe utilizzato per creare un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="c2aa2-115">The class name used to create an instance of this class.</span></span> <span data-ttu-id="c2aa2-116">**CreationClassName** è combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="c2aa2-116">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="c2aa2-117">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-117">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2aa2-118">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2aa2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-120">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ System**.**OtherIdentifyingInfo**")</span><span class="sxs-lookup"><span data-stu-id="c2aa2-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="c2aa2-121">Matrice che contiene le descrizioni dei valori nella proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="c2aa2-121">An array that contains descriptions of the values in the **OtherIdentifyingInfo** property.</span></span> <span data-ttu-id="c2aa2-122">Gli elementi della matrice in **IdentifyingDescriptions** corrispondono agli elementi della proprietà **IdentifyingDescriptions** .</span><span class="sxs-lookup"><span data-stu-id="c2aa2-122">The array items in **IdentifyingDescriptions** correspond to the items in the **IdentifyingDescriptions** property.</span></span>

</dd> <dt>

<span data-ttu-id="c2aa2-123">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-123">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2aa2-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2aa2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-126">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c2aa2-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c2aa2-127">Chiave di questa istanza in un ambiente aziendale.</span><span class="sxs-lookup"><span data-stu-id="c2aa2-127">The key of this instance in an enterprise environment.</span></span>

</dd> <dt>

<span data-ttu-id="c2aa2-128">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-128">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2aa2-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2aa2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-131">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c2aa2-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c2aa2-132">Convenzione di denominazione utilizzata dalla proprietà Name per assicurarsi che i valori dei **nomi** siano univoci.</span><span class="sxs-lookup"><span data-stu-id="c2aa2-132">The naming convention used by the Name property to ensure that **Name** values are unique.</span></span>

</dd> <dt>

<span data-ttu-id="c2aa2-133">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-133">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2aa2-134">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-134">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c2aa2-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-136">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ sistema CIM**.**IdentifyingDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="c2aa2-136">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="c2aa2-137">Matrice che contiene un set di dati aggiuntivi, oltre alle informazioni sul nome del sistema, che possono essere utilizzati per identificare un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="c2aa2-137">An array that contains a set of additional data, beyond system name information, that could be used to identify a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="c2aa2-138">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-138">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2aa2-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c2aa2-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-141">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni generali \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="c2aa2-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="c2aa2-142">Stringa che fornisce informazioni sul modo in cui il proprietario del sistema primario può essere raggiunto, ad esempio numero di telefono, indirizzo di posta elettronica e così via.</span><span class="sxs-lookup"><span data-stu-id="c2aa2-142">A string that provides information on how the primary system owner can be reached (for example, phone number, e-mail address, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="c2aa2-143">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-143">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2aa2-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c2aa2-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-146">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni generali \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="c2aa2-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="c2aa2-147">Nome dell'utente primario del sistema.</span><span class="sxs-lookup"><span data-stu-id="c2aa2-147">The name of the primary user of the system.</span></span>

</dd> <dt>

<span data-ttu-id="c2aa2-148">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-148">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2aa2-149">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c2aa2-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c2aa2-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c2aa2-151">Matrice che contiene i ruoli eseguiti dal sistema in un ambiente aziendale.</span><span class="sxs-lookup"><span data-stu-id="c2aa2-151">An array that contains the roles carried out by the system in an enterprise environment.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2aa2-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2aa2-152">Requirements</span></span>



| <span data-ttu-id="c2aa2-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2aa2-153">Requirement</span></span> | <span data-ttu-id="c2aa2-154">Valore</span><span class="sxs-lookup"><span data-stu-id="c2aa2-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2aa2-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2aa2-155">Minimum supported client</span></span><br/> | <span data-ttu-id="c2aa2-156">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c2aa2-156">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c2aa2-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2aa2-157">Minimum supported server</span></span><br/> | <span data-ttu-id="c2aa2-158">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2aa2-158">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c2aa2-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c2aa2-159">Namespace</span></span><br/>                | <span data-ttu-id="c2aa2-160">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c2aa2-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c2aa2-161">MOF</span><span class="sxs-lookup"><span data-stu-id="c2aa2-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2aa2-162"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2aa2-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2aa2-163">DLL</span><span class="sxs-lookup"><span data-stu-id="c2aa2-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2aa2-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c2aa2-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c2aa2-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2aa2-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2aa2-166">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="c2aa2-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

