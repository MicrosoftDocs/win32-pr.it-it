---
description: La \_ classe di prodotto CIM è una classe concreta che rappresenta una raccolta di elementi fisici, funzionalità software e altri prodotti, acquisiti come unità.
ms.assetid: beb20f61-de39-4221-8d29-4727104518d5
ms.tgt_platform: multiple
title: Classe CIM_Product
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Product
- CIM_Product.Caption
- CIM_Product.Description
- CIM_Product.IdentifyingNumber
- CIM_Product.Name
- CIM_Product.SKUNumber
- CIM_Product.Vendor
- CIM_Product.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16c8541a18185d721bbdcbf23acaeb67adf508c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748007"
---
# <a name="cim_product-class"></a><span data-ttu-id="a165c-103">\_Classe prodotto CIM</span><span class="sxs-lookup"><span data-stu-id="a165c-103">CIM\_Product class</span></span>

<span data-ttu-id="a165c-104">La classe di **\_ prodotto CIM** è una classe concreta che rappresenta una raccolta di elementi fisici, funzionalità software e altri prodotti, acquisiti come unità.</span><span class="sxs-lookup"><span data-stu-id="a165c-104">The **CIM\_Product** class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="a165c-105">L'acquisizione implica un accordo tra il fornitore e il consumer, che può avere implicazioni sulla licenza, il supporto e la garanzia di prodotti.</span><span class="sxs-lookup"><span data-stu-id="a165c-105">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a165c-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a165c-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a165c-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a165c-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a165c-108">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a165c-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a165c-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a165c-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a165c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a165c-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B63-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="a165c-111">Members</span><span class="sxs-lookup"><span data-stu-id="a165c-111">Members</span></span>

<span data-ttu-id="a165c-112">La classe di **\_ prodotto CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a165c-112">The **CIM\_Product** class has these types of members:</span></span>

-   [<span data-ttu-id="a165c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a165c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a165c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a165c-114">Properties</span></span>

<span data-ttu-id="a165c-115">La **classe \_ Product CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a165c-115">The **CIM\_Product** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a165c-116">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a165c-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a165c-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a165c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a165c-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a165c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a165c-119">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a165c-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a165c-120">Breve descrizione testuale del prodotto.</span><span class="sxs-lookup"><span data-stu-id="a165c-120">Short textual description for the product.</span></span>

</dd> <dt>

<span data-ttu-id="a165c-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a165c-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a165c-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a165c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a165c-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a165c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a165c-124">Descrizione testuale del prodotto.</span><span class="sxs-lookup"><span data-stu-id="a165c-124">Textual description of the product.</span></span>

</dd> <dt>

<span data-ttu-id="a165c-125">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="a165c-125">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a165c-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a165c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a165c-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a165c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a165c-128">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="a165c-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="a165c-129">Identificazione del prodotto, ad esempio un numero di serie sul software, un numero di dado su un chip hardware o (per prodotti non commerciali) un numero di progetto.</span><span class="sxs-lookup"><span data-stu-id="a165c-129">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

</dd> <dt>

<span data-ttu-id="a165c-130">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a165c-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a165c-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a165c-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a165c-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a165c-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a165c-133">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="a165c-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="a165c-134">Nome del prodotto comunemente usato.</span><span class="sxs-lookup"><span data-stu-id="a165c-134">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="a165c-135">**SKUNumber**</span><span class="sxs-lookup"><span data-stu-id="a165c-135">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a165c-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a165c-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a165c-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a165c-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a165c-138">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a165c-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a165c-139">Informazioni sulle unità di supporto (SKU) del prodotto.</span><span class="sxs-lookup"><span data-stu-id="a165c-139">Product's stock-keeping unit (SKU) information.</span></span>

</dd> <dt>

<span data-ttu-id="a165c-140">**Fornitore**</span><span class="sxs-lookup"><span data-stu-id="a165c-140">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a165c-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a165c-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a165c-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a165c-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a165c-143">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="a165c-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="a165c-144">Nome del fornitore del prodotto o dell'entità che vende il prodotto (produttore, rivenditore, OEM e così via).</span><span class="sxs-lookup"><span data-stu-id="a165c-144">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="a165c-145">**Versione**</span><span class="sxs-lookup"><span data-stu-id="a165c-145">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a165c-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a165c-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a165c-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a165c-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a165c-148">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="a165c-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a165c-149">Informazioni sulla versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="a165c-149">Product version information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a165c-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="a165c-150">Remarks</span></span>

<span data-ttu-id="a165c-151">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a165c-151">WMI does not implement this class.</span></span> <span data-ttu-id="a165c-152">Per le classi WMI derivate **dal \_ prodotto CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a165c-152">For WMI classes that are derived from **CIM\_Product**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a165c-153">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a165c-153">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a165c-154">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a165c-154">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a165c-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a165c-155">Requirements</span></span>



| <span data-ttu-id="a165c-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="a165c-156">Requirement</span></span> | <span data-ttu-id="a165c-157">Valore</span><span class="sxs-lookup"><span data-stu-id="a165c-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a165c-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a165c-158">Minimum supported client</span></span><br/> | <span data-ttu-id="a165c-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a165c-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a165c-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a165c-160">Minimum supported server</span></span><br/> | <span data-ttu-id="a165c-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a165c-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a165c-162">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a165c-162">Namespace</span></span><br/>                | <span data-ttu-id="a165c-163">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a165c-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a165c-164">MOF</span><span class="sxs-lookup"><span data-stu-id="a165c-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a165c-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a165c-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a165c-166">DLL</span><span class="sxs-lookup"><span data-stu-id="a165c-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a165c-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a165c-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

