---
description: La \_ classe CIM LogicalIdentity è un'associazione astratta e generica che indica che due elementi logici rappresentano aspetti diversi della stessa entità sottostante.
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: Classe CIM_LogicalIdentity (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965999"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a><span data-ttu-id="17ff3-103">Classe CIM_LogicalIdentity (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="17ff3-103">CIM_LogicalIdentity class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="17ff3-104">La classe **CIM \_ LogicalIdentity** è un'associazione astratta e generica che indica che due elementi logici rappresentano aspetti diversi della stessa entità sottostante.</span><span class="sxs-lookup"><span data-stu-id="17ff3-104">The **CIM\_LogicalIdentity** class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="17ff3-105">L'associazione trasmette ciò che può essere definito con ereditarietà multipla ed è limitato agli aspetti logici di un elemento di sistema gestito.</span><span class="sxs-lookup"><span data-stu-id="17ff3-105">The association conveys what can be defined with multiple inheritance and is restricted to the logical aspects of a managed system element.</span></span> <span data-ttu-id="17ff3-106">Nella maggior parte degli scenari la relazione di identità è determinata dall'equivalenza delle chiavi o da altre proprietà di identificazione degli elementi correlati.</span><span class="sxs-lookup"><span data-stu-id="17ff3-106">In most scenarios, the identity relationship is determined by the equivalence of keys, or some other identifying properties of the related elements.</span></span>

<span data-ttu-id="17ff3-107">L'associazione deve essere utilizzata solo in scenari ben noti, consentendo una definizione e un chiarimento più concreti nelle sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="17ff3-107">The association should only be used in scenarios that are well understood, allowing more concrete definition and clarification in subclasses.</span></span> <span data-ttu-id="17ff3-108">Uno scenario in cui la relazione è ragionevole, ad esempio, rappresenta un dispositivo che è sia un'entità bus che un'entità funzionale, in cui il dispositivo è un'entità USB (bus) e una tastiera (funzionale).</span><span class="sxs-lookup"><span data-stu-id="17ff3-108">A scenario where the relationship is reasonable, for example, represents a device that is both a bus entity and a functional entity where the device is a USB (bus) and keyboard (functional) entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17ff3-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="17ff3-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="17ff3-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="17ff3-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="17ff3-111">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="17ff3-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="17ff3-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="17ff3-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17ff3-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17ff3-113">Syntax</span></span>

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="17ff3-114">Members</span><span class="sxs-lookup"><span data-stu-id="17ff3-114">Members</span></span>

<span data-ttu-id="17ff3-115">La classe **CIM \_ LogicalIdentity** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="17ff3-115">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="17ff3-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="17ff3-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17ff3-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="17ff3-117">Properties</span></span>

<span data-ttu-id="17ff3-118">La classe **CIM \_ LogicalIdentity** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="17ff3-118">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17ff3-119">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="17ff3-119">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17ff3-120">Tipo di dati **: \_ LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="17ff3-120">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="17ff3-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="17ff3-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17ff3-122">Riferimento a un aspetto alternativo dell'entità di sistema.</span><span class="sxs-lookup"><span data-stu-id="17ff3-122">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="17ff3-123">**SystemElement**</span><span class="sxs-lookup"><span data-stu-id="17ff3-123">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17ff3-124">Tipo di dati **: \_ LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="17ff3-124">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="17ff3-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="17ff3-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17ff3-126">Riferimento a un aspetto dell'elemento logico.</span><span class="sxs-lookup"><span data-stu-id="17ff3-126">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17ff3-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="17ff3-127">Remarks</span></span>

<span data-ttu-id="17ff3-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="17ff3-128">WMI does not implement this class.</span></span> <span data-ttu-id="17ff3-129">Per le classi derivate da **CIM \_ LogicalIdentity**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="17ff3-129">For classes derived from **CIM\_LogicalIdentity**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="17ff3-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="17ff3-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="17ff3-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="17ff3-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="17ff3-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17ff3-132">Requirements</span></span>



| <span data-ttu-id="17ff3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="17ff3-133">Requirement</span></span> | <span data-ttu-id="17ff3-134">Valore</span><span class="sxs-lookup"><span data-stu-id="17ff3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17ff3-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17ff3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="17ff3-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17ff3-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17ff3-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17ff3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="17ff3-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17ff3-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17ff3-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17ff3-139">Namespace</span></span><br/>                | <span data-ttu-id="17ff3-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="17ff3-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17ff3-141">MOF</span><span class="sxs-lookup"><span data-stu-id="17ff3-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17ff3-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17ff3-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17ff3-143">DLL</span><span class="sxs-lookup"><span data-stu-id="17ff3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17ff3-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17ff3-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




