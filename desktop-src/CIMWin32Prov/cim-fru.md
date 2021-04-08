---
description: La \_ classe CIM FRU rappresenta una raccolta definita dal fornitore di prodotti ed elementi fisici associati a un'unità sostituibile sul campo (FRU) per supportare, gestire o aggiornare un prodotto nella posizione del cliente.
ms.assetid: 4464ec3a-5509-4e15-9020-4abb2edd2570
ms.tgt_platform: multiple
title: Classe CIM_FRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRU
- CIM_FRU.Caption
- CIM_FRU.Description
- CIM_FRU.FRUNumber
- CIM_FRU.IdentifyingNumber
- CIM_FRU.Name
- CIM_FRU.RevisionLevel
- CIM_FRU.Vendor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d163c3c223159ad8e09aa6e36d63187ff0aa97f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748466"
---
# <a name="cim_fru-class"></a><span data-ttu-id="1f67e-103">\_Classe di FRU CIM</span><span class="sxs-lookup"><span data-stu-id="1f67e-103">CIM\_FRU class</span></span>

<span data-ttu-id="1f67e-104">La classe **CIM \_ FRU** rappresenta una raccolta definita dal fornitore di prodotti ed elementi fisici associati a un'unità sostituibile sul campo (FRU) per supportare, gestire o aggiornare un prodotto nella posizione del cliente.</span><span class="sxs-lookup"><span data-stu-id="1f67e-104">The **CIM\_FRU** class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f67e-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="1f67e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1f67e-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1f67e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1f67e-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1f67e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1f67e-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="1f67e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f67e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f67e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{778C74EE-DB2A-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FRU
{
  string Caption;
  string Description;
  string FRUNumber;
  string IdentifyingNumber;
  string Name;
  string RevisionLevel;
  string Vendor;
};
```

## <a name="members"></a><span data-ttu-id="1f67e-110">Members</span><span class="sxs-lookup"><span data-stu-id="1f67e-110">Members</span></span>

<span data-ttu-id="1f67e-111">La classe **CIM \_ FRU** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1f67e-111">The **CIM\_FRU** class has these types of members:</span></span>

-   [<span data-ttu-id="1f67e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1f67e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f67e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1f67e-113">Properties</span></span>

<span data-ttu-id="1f67e-114">La classe **CIM \_ FRU** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1f67e-114">The **CIM\_FRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f67e-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="1f67e-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f67e-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1f67e-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1f67e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1f67e-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1f67e-119">Breve descrizione testuale per la FRU.</span><span class="sxs-lookup"><span data-stu-id="1f67e-119">Short textual description for the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="1f67e-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1f67e-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f67e-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1f67e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1f67e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-123">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 002,3 ")</span><span class="sxs-lookup"><span data-stu-id="1f67e-123">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.3")</span></span>
</dt> </dl>

<span data-ttu-id="1f67e-124">Descrizione della FRU.</span><span class="sxs-lookup"><span data-stu-id="1f67e-124">Description of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="1f67e-125">**FRUNumber**</span><span class="sxs-lookup"><span data-stu-id="1f67e-125">**FRUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f67e-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1f67e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1f67e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-128">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 002,6 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1f67e-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.6"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1f67e-129">Informazioni sugli ordini di FRU.</span><span class="sxs-lookup"><span data-stu-id="1f67e-129">FRU ordering information.</span></span>

</dd> <dt>

<span data-ttu-id="1f67e-130">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="1f67e-130">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f67e-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1f67e-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1f67e-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-133">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 002,7 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1f67e-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.7"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1f67e-134">Identificazione del software, ad esempio un numero di serie o un numero di dado su un chip hardware.</span><span class="sxs-lookup"><span data-stu-id="1f67e-134">Identification on software, such as a serial number, or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="1f67e-135">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1f67e-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f67e-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1f67e-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1f67e-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-138">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1f67e-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1f67e-139">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="1f67e-139">Label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="1f67e-140">**RevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="1f67e-140">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f67e-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1f67e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1f67e-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-143">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 002,8 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1f67e-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.8"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1f67e-144">Livello di revisione della FRU.</span><span class="sxs-lookup"><span data-stu-id="1f67e-144">Revision level of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="1f67e-145">**Fornitore**</span><span class="sxs-lookup"><span data-stu-id="1f67e-145">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f67e-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1f67e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1f67e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f67e-148">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 002,4 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1f67e-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.4"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1f67e-149">Nome del fornitore.</span><span class="sxs-lookup"><span data-stu-id="1f67e-149">Name of the supplier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f67e-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f67e-150">Remarks</span></span>

<span data-ttu-id="1f67e-151">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="1f67e-151">WMI does not implement this class.</span></span>

<span data-ttu-id="1f67e-152">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="1f67e-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1f67e-153">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="1f67e-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f67e-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f67e-154">Requirements</span></span>



| <span data-ttu-id="1f67e-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f67e-155">Requirement</span></span> | <span data-ttu-id="1f67e-156">Valore</span><span class="sxs-lookup"><span data-stu-id="1f67e-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f67e-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f67e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="1f67e-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f67e-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f67e-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f67e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="1f67e-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f67e-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f67e-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1f67e-161">Namespace</span></span><br/>                | <span data-ttu-id="1f67e-162">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1f67e-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1f67e-163">MOF</span><span class="sxs-lookup"><span data-stu-id="1f67e-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f67e-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f67e-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f67e-165">DLL</span><span class="sxs-lookup"><span data-stu-id="1f67e-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f67e-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f67e-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

