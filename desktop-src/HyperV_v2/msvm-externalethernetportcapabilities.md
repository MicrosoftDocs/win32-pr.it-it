---
description: Descrive le funzionalità del ExternalEthernetPort MSVM associato \_ .
ms.assetid: 63731b62-b1c7-4dd9-b906-03225bbc3154
title: Classe Msvm_ExternalEthernetPortCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPortCapabilities
- Msvm_ExternalEthernetPortCapabilities.InstanceID
- Msvm_ExternalEthernetPortCapabilities.Caption
- Msvm_ExternalEthernetPortCapabilities.Description
- Msvm_ExternalEthernetPortCapabilities.ElementName
- Msvm_ExternalEthernetPortCapabilities.IOVSupport
- Msvm_ExternalEthernetPortCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 748b207151fb1d11b013af7c736de52bbe5bec8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879589"
---
# <a name="msvm_externalethernetportcapabilities-class"></a><span data-ttu-id="da308-103">\_Classe MSVM ExternalEthernetPortCapabilities</span><span class="sxs-lookup"><span data-stu-id="da308-103">Msvm\_ExternalEthernetPortCapabilities class</span></span>

<span data-ttu-id="da308-104">Descrive le funzionalità del [**\_ ExternalEthernetPort MSVM**](msvm-externalethernetport.md)associato.</span><span class="sxs-lookup"><span data-stu-id="da308-104">Describes the capabilities of the associated [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md).</span></span>

<span data-ttu-id="da308-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="da308-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="da308-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da308-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPortCapabilities : CIM_Capabilities
{
  string  InstanceID;
  string  Caption = "Ethernet Port Capabilities";
  string  Description = "Describes the capabilities of the Microsoft External Ethernet Port";
  string  ElementName = "Ethernet Port Capabilities";
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="da308-107">Members</span><span class="sxs-lookup"><span data-stu-id="da308-107">Members</span></span>

<span data-ttu-id="da308-108">La **classe \_ ExternalEthernetPortCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="da308-108">The **Msvm\_ExternalEthernetPortCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="da308-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da308-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da308-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da308-110">Properties</span></span>

<span data-ttu-id="da308-111">La **classe \_ ExternalEthernetPortCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="da308-111">The **Msvm\_ExternalEthernetPortCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da308-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="da308-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da308-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da308-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da308-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da308-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da308-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="da308-115">A short description of the object.</span></span> <span data-ttu-id="da308-116">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Port Capabilities".</span><span class="sxs-lookup"><span data-stu-id="da308-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="da308-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="da308-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da308-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da308-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da308-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da308-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da308-120">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="da308-120">A description of the object.</span></span> <span data-ttu-id="da308-121">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "descrive le funzionalità della porta Ethernet esterna Microsoft".</span><span class="sxs-lookup"><span data-stu-id="da308-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the capabilities of the Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="da308-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="da308-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da308-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da308-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da308-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da308-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da308-125">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="da308-125">A display name for the object.</span></span> <span data-ttu-id="da308-126">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Port Capabilities".</span><span class="sxs-lookup"><span data-stu-id="da308-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="da308-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="da308-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da308-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da308-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da308-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da308-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da308-130">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="da308-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="da308-131">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="da308-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="da308-132">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="da308-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="da308-133">**IOVSupport**</span><span class="sxs-lookup"><span data-stu-id="da308-133">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da308-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="da308-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da308-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da308-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da308-136">Valore booleano che indica se la virtualizzazione I/O (IOV) è supportata dalla scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="da308-136">A boolean value that indicates whether I/O virtualization (IOV) is supported by the network adapter.</span></span> <span data-ttu-id="da308-137">Se il valore è **true**, IOV è supportato dalla scheda di rete e la proprietà **IOVSupportReasons** sarà vuota.</span><span class="sxs-lookup"><span data-stu-id="da308-137">If the value is **True**, then IOV is supported by the network adapter and the **IOVSupportReasons** property will be empty.</span></span> <span data-ttu-id="da308-138">In caso contrario, la proprietà **IOVSupportReasons** avrà i motivi per cui non è possibile supportare IOV.</span><span class="sxs-lookup"><span data-stu-id="da308-138">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="da308-139">**IOVSupportReasons**</span><span class="sxs-lookup"><span data-stu-id="da308-139">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da308-140">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="da308-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="da308-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da308-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da308-142">Matrice di stringhe che indica i possibili motivi per cui IOV non è supportato.</span><span class="sxs-lookup"><span data-stu-id="da308-142">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="da308-143">Se il valore di **IOVSupport** è **true**, questa matrice sarà vuota.</span><span class="sxs-lookup"><span data-stu-id="da308-143">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da308-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da308-144">Requirements</span></span>



| <span data-ttu-id="da308-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="da308-145">Requirement</span></span> | <span data-ttu-id="da308-146">Valore</span><span class="sxs-lookup"><span data-stu-id="da308-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da308-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da308-147">Minimum supported client</span></span><br/> | <span data-ttu-id="da308-148">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="da308-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="da308-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da308-149">Minimum supported server</span></span><br/> | <span data-ttu-id="da308-150">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="da308-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da308-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="da308-151">Namespace</span></span><br/>                | <span data-ttu-id="da308-152">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="da308-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="da308-153">MOF</span><span class="sxs-lookup"><span data-stu-id="da308-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da308-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da308-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="da308-155">DLL</span><span class="sxs-lookup"><span data-stu-id="da308-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da308-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="da308-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

