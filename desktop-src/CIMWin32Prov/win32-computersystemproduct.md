---
description: Rappresenta un prodotto. Sono inclusi software e hardware usati in questo sistema di computer.
ms.assetid: 6241e703-4ce9-435f-bf36-4388e38a3ea5
ms.tgt_platform: multiple
title: Classe Win32_ComputerSystemProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProduct
- Win32_ComputerSystemProduct.Caption
- Win32_ComputerSystemProduct.Description
- Win32_ComputerSystemProduct.IdentifyingNumber
- Win32_ComputerSystemProduct.Name
- Win32_ComputerSystemProduct.SKUNumber
- Win32_ComputerSystemProduct.Vendor
- Win32_ComputerSystemProduct.Version
- Win32_ComputerSystemProduct.UUID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cab3dc8679c606076eca2f5cf704867aa9833c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126261"
---
# <a name="win32_computersystemproduct-class"></a><span data-ttu-id="06bcf-104">Win32 \_ ComputerSystemProduct (classe)</span><span class="sxs-lookup"><span data-stu-id="06bcf-104">Win32\_ComputerSystemProduct class</span></span>

<span data-ttu-id="06bcf-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ComputerSystemProduct Win32** rappresenta un prodotto.</span><span class="sxs-lookup"><span data-stu-id="06bcf-105">The **Win32\_ComputerSystemProduct** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a product.</span></span> <span data-ttu-id="06bcf-106">Sono inclusi software e hardware usati in questo sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="06bcf-106">This includes software and hardware used on this computer system.</span></span>

<span data-ttu-id="06bcf-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="06bcf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="06bcf-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="06bcf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="06bcf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06bcf-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B96-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystemProduct : CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
  string UUID;
};
```

## <a name="members"></a><span data-ttu-id="06bcf-110">Members</span><span class="sxs-lookup"><span data-stu-id="06bcf-110">Members</span></span>

<span data-ttu-id="06bcf-111">La classe **Win32 \_ ComputerSystemProduct** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="06bcf-111">The **Win32\_ComputerSystemProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="06bcf-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06bcf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06bcf-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06bcf-113">Properties</span></span>

<span data-ttu-id="06bcf-114">La classe **Win32 \_ ComputerSystemProduct** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="06bcf-114">The **Win32\_ComputerSystemProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06bcf-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="06bcf-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06bcf-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06bcf-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06bcf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="06bcf-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="06bcf-119">Breve descrizione testuale del prodotto.</span><span class="sxs-lookup"><span data-stu-id="06bcf-119">Short textual description for the product.</span></span>

<span data-ttu-id="06bcf-120">Questa proprietà viene ereditata [**dal \_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="06bcf-120">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="06bcf-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="06bcf-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06bcf-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06bcf-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06bcf-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06bcf-124">Descrizione testuale del prodotto.</span><span class="sxs-lookup"><span data-stu-id="06bcf-124">Textual description of the product.</span></span>

<span data-ttu-id="06bcf-125">Questa proprietà viene ereditata [**dal \_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="06bcf-125">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="06bcf-126">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="06bcf-126">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06bcf-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06bcf-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06bcf-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-129">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="06bcf-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="06bcf-130">Identificazione del prodotto, ad esempio un numero di serie sul software, un numero di dado su un chip hardware o (per prodotti non commerciali) un numero di progetto.</span><span class="sxs-lookup"><span data-stu-id="06bcf-130">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

<span data-ttu-id="06bcf-131">Questa proprietà viene ereditata [**dal \_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="06bcf-131">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="06bcf-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="06bcf-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06bcf-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06bcf-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06bcf-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-135">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="06bcf-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="06bcf-136">Nome del prodotto comunemente usato.</span><span class="sxs-lookup"><span data-stu-id="06bcf-136">Commonly used product name.</span></span>

<span data-ttu-id="06bcf-137">Questa proprietà viene ereditata [**dal \_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="06bcf-137">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="06bcf-138">**SKUNumber**</span><span class="sxs-lookup"><span data-stu-id="06bcf-138">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06bcf-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06bcf-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06bcf-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-141">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="06bcf-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="06bcf-142">Informazioni sulle unità di supporto (SKU) del prodotto.</span><span class="sxs-lookup"><span data-stu-id="06bcf-142">Product's stock-keeping unit (SKU) information.</span></span>

<span data-ttu-id="06bcf-143">Questa proprietà viene ereditata [**dal \_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="06bcf-143">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="06bcf-144">**UUID**</span><span class="sxs-lookup"><span data-stu-id="06bcf-144">**UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06bcf-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06bcf-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06bcf-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-147">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 1 \| UUID")</span><span class="sxs-lookup"><span data-stu-id="06bcf-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|UUID")</span></span>
</dt> </dl>

<span data-ttu-id="06bcf-148">Identificatore univoco universale (UUID) per questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="06bcf-148">Universally unique identifier (UUID) for this product.</span></span> <span data-ttu-id="06bcf-149">Un UUID è un identificatore a 128 bit che è sicuramente diverso da quello degli altri UUID generati.</span><span class="sxs-lookup"><span data-stu-id="06bcf-149">A UUID is a 128-bit identifier that is guaranteed to be different from other generated UUIDs.</span></span> <span data-ttu-id="06bcf-150">Se non è disponibile alcun UUID, viene usato un UUID di tutti gli zeri.</span><span class="sxs-lookup"><span data-stu-id="06bcf-150">If a UUID is not available, a UUID of all zeros is used.</span></span>

<span data-ttu-id="06bcf-151">Questo valore deriva dal membro **UUID** della struttura delle **informazioni di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="06bcf-151">This value comes from the **UUID** member of the **System Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="06bcf-152">**Fornitore**</span><span class="sxs-lookup"><span data-stu-id="06bcf-152">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06bcf-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06bcf-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06bcf-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-155">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="06bcf-155">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="06bcf-156">Nome del fornitore del prodotto o dell'entità che vende il prodotto (produttore, rivenditore, OEM e così via).</span><span class="sxs-lookup"><span data-stu-id="06bcf-156">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

<span data-ttu-id="06bcf-157">Questa proprietà viene ereditata [**dal \_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="06bcf-157">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="06bcf-158">**Versione**</span><span class="sxs-lookup"><span data-stu-id="06bcf-158">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06bcf-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06bcf-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06bcf-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06bcf-161">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="06bcf-161">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="06bcf-162">Informazioni sulla versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="06bcf-162">Product version information.</span></span>

<span data-ttu-id="06bcf-163">Questa proprietà viene ereditata [**dal \_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="06bcf-163">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06bcf-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="06bcf-164">Remarks</span></span>

<span data-ttu-id="06bcf-165">La classe **Win32 \_ ComputerSystemProduct** è derivata dal [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="06bcf-165">The **Win32\_ComputerSystemProduct** class is derived from [**CIM\_Product**](cim-product.md).</span></span>

## <a name="examples"></a><span data-ttu-id="06bcf-166">Esempio</span><span class="sxs-lookup"><span data-stu-id="06bcf-166">Examples</span></span>

<span data-ttu-id="06bcf-167">Nell'esempio [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell della raccolta TechNet viene usato **per \_ ComputerSystemProduct Win32** per recuperare un elenco di hardware non funzionante con WMI.</span><span class="sxs-lookup"><span data-stu-id="06bcf-167">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_ComputerSystemProduct** to retrieve a list of non-working hardware using WMI.</span></span>

## <a name="requirements"></a><span data-ttu-id="06bcf-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06bcf-168">Requirements</span></span>



| <span data-ttu-id="06bcf-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="06bcf-169">Requirement</span></span> | <span data-ttu-id="06bcf-170">Valore</span><span class="sxs-lookup"><span data-stu-id="06bcf-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06bcf-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06bcf-171">Minimum supported client</span></span><br/> | <span data-ttu-id="06bcf-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06bcf-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06bcf-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06bcf-173">Minimum supported server</span></span><br/> | <span data-ttu-id="06bcf-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06bcf-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06bcf-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06bcf-175">Namespace</span></span><br/>                | <span data-ttu-id="06bcf-176">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="06bcf-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06bcf-177">MOF</span><span class="sxs-lookup"><span data-stu-id="06bcf-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06bcf-178"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06bcf-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06bcf-179">DLL</span><span class="sxs-lookup"><span data-stu-id="06bcf-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06bcf-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06bcf-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06bcf-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06bcf-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06bcf-182">**\_Prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="06bcf-182">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dt>

<span data-ttu-id="06bcf-183">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="06bcf-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

