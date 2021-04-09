---
description: La \_ classe WMI Association Protocol associazione di Win32 mette in correlazione un driver a livello di sistema, un protocollo di rete e una scheda di rete.
ms.assetid: 09b84bb2-9999-4e80-a330-88ed6b2bd5e9
ms.tgt_platform: multiple
title: Classe Win32_ProtocolBinding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProtocolBinding
- Win32_ProtocolBinding.Antecedent
- Win32_ProtocolBinding.Dependent
- Win32_ProtocolBinding.Device
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91e735a599a1dda2536fe26bcd654dcdf4b119dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877337"
---
# <a name="win32_protocolbinding-class"></a><span data-ttu-id="3e4f9-103">\_Classe di protocollo Win32</span><span class="sxs-lookup"><span data-stu-id="3e4f9-103">Win32\_ProtocolBinding class</span></span>

<span data-ttu-id="3e4f9-104">La [classe WMI](../wmisdk/retrieving-a-class.md) Association **\_ Protocol** associazione di Win32 mette in correlazione un driver a livello di sistema, un protocollo di rete e una scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="3e4f9-104">The **Win32\_ProtocolBinding** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system-level driver, network protocol, and network adapter.</span></span>

<span data-ttu-id="3e4f9-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3e4f9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3e4f9-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3e4f9-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e4f9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e4f9-107">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("CIMWin32"), UUID("{8502C509-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProtocolBinding
{
  Win32_NetworkProtocol REF Antecedent;
  Win32_SystemDriver    REF Dependent;
  Win32_NetworkAdapter  REF Device;
};
```

## <a name="members"></a><span data-ttu-id="3e4f9-108">Members</span><span class="sxs-lookup"><span data-stu-id="3e4f9-108">Members</span></span>

<span data-ttu-id="3e4f9-109">La classe di **\_ protocollo Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3e4f9-109">The **Win32\_ProtocolBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="3e4f9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3e4f9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e4f9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3e4f9-111">Properties</span></span>

<span data-ttu-id="3e4f9-112">La classe di **\_ protocollo Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3e4f9-112">The **Win32\_ProtocolBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e4f9-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3e4f9-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e4f9-114">Tipo di dati: **Win32 \_ NetworkProtocol**</span><span class="sxs-lookup"><span data-stu-id="3e4f9-114">Data type: **Win32\_NetworkProtocol**</span></span>
</dt> <dt>

<span data-ttu-id="3e4f9-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e4f9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e4f9-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkProtocol")</span><span class="sxs-lookup"><span data-stu-id="3e4f9-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="3e4f9-117">Riferimento all'istanza di che rappresenta il protocollo utilizzato con il driver di sistema e nella scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="3e4f9-117">Reference to the instance representing the protocol that is used with the system driver and on the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3e4f9-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="3e4f9-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e4f9-119">Tipo di dati: **Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="3e4f9-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="3e4f9-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e4f9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e4f9-121">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="3e4f9-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="3e4f9-122">Riferimento all'istanza di che rappresenta il driver di sistema che utilizza la scheda di rete tramite il protocollo di rete di questa classe.</span><span class="sxs-lookup"><span data-stu-id="3e4f9-122">Reference to the instance representing the system driver that uses the network adapter through the network protocol of this class.</span></span>

</dd> <dt>

<span data-ttu-id="3e4f9-123">**Dispositivo**</span><span class="sxs-lookup"><span data-stu-id="3e4f9-123">**Device**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e4f9-124">Tipo di dati: **Win32 \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="3e4f9-124">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="3e4f9-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e4f9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e4f9-126">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapter")</span><span class="sxs-lookup"><span data-stu-id="3e4f9-126">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="3e4f9-127">Proprietà della scheda di rete utilizzata nel computer.</span><span class="sxs-lookup"><span data-stu-id="3e4f9-127">Properties of the network adapter being used on the computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e4f9-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e4f9-128">Requirements</span></span>



| <span data-ttu-id="3e4f9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e4f9-129">Requirement</span></span> | <span data-ttu-id="3e4f9-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3e4f9-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e4f9-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e4f9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3e4f9-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e4f9-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e4f9-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e4f9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3e4f9-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e4f9-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e4f9-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3e4f9-135">Namespace</span></span><br/>                | <span data-ttu-id="3e4f9-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3e4f9-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e4f9-137">MOF</span><span class="sxs-lookup"><span data-stu-id="3e4f9-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e4f9-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e4f9-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e4f9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3e4f9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e4f9-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e4f9-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e4f9-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e4f9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e4f9-142">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3e4f9-142">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
