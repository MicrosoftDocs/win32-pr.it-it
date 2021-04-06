---
title: Classe MDM_DeviceStatus_Firewall01
description: La \_ classe MDM DeviceStatus \_ Firewall01 viene usata dall'azienda per eseguire query sullo stato della conformità del firewall dei dispositivi con i criteri aziendali.
ms.assetid: 0f62350c-8c7b-44fb-b163-dedaf4669895
keywords:
- Classe MDM_DeviceStatus_Firewall01
- Classe MDM_DeviceStatus_Firewall01, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Firewall01
- MDM_DeviceStatus_Firewall01.InstanceID
- MDM_DeviceStatus_Firewall01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67166a076b9e6db01d8642d7b1d21e72b8732c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742626"
---
# <a name="mdm_devicestatus_firewall01-class"></a><span data-ttu-id="fcd27-105">\_Classe MDM DeviceStatus \_ Firewall01</span><span class="sxs-lookup"><span data-stu-id="fcd27-105">MDM\_DeviceStatus\_Firewall01 class</span></span>

<span data-ttu-id="fcd27-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="fcd27-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fcd27-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="fcd27-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fcd27-108">La classe **MDM \_ DeviceStatus \_ Firewall01** viene usata dall'azienda per eseguire query sullo stato della conformità del firewall dei dispositivi con i criteri aziendali.</span><span class="sxs-lookup"><span data-stu-id="fcd27-108">The **MDM\_DeviceStatus\_Firewall01** class is used by the enterprise to query the state of firewall compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="fcd27-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fcd27-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcd27-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fcd27-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Firewall01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="fcd27-111">Members</span><span class="sxs-lookup"><span data-stu-id="fcd27-111">Members</span></span>

<span data-ttu-id="fcd27-112">La classe **MDM \_ DeviceStatus \_ Firewall01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fcd27-112">The **MDM\_DeviceStatus\_Firewall01** class has these types of members:</span></span>

-   [<span data-ttu-id="fcd27-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fcd27-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fcd27-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fcd27-114">Properties</span></span>

<span data-ttu-id="fcd27-115">La classe **MDM \_ DeviceStatus \_ Firewall01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fcd27-115">The **MDM\_DeviceStatus\_Firewall01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fcd27-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fcd27-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd27-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fcd27-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcd27-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fcd27-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcd27-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fcd27-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fcd27-120">Nodo per la query del firewall.</span><span class="sxs-lookup"><span data-stu-id="fcd27-120">Node for the firewall query.</span></span>

</dd> <dt>

<span data-ttu-id="fcd27-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fcd27-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd27-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fcd27-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcd27-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fcd27-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcd27-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fcd27-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fcd27-125">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="fcd27-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="fcd27-126">Per questa classe la stringa è "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="fcd27-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="fcd27-127">Status</span><span class="sxs-lookup"><span data-stu-id="fcd27-127">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd27-128">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fcd27-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcd27-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fcd27-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fcd27-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fcd27-130">Requirements</span></span>



| <span data-ttu-id="fcd27-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcd27-131">Requirement</span></span> | <span data-ttu-id="fcd27-132">Valore</span><span class="sxs-lookup"><span data-stu-id="fcd27-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd27-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcd27-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fcd27-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fcd27-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fcd27-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcd27-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fcd27-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fcd27-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fcd27-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fcd27-137">Namespace</span></span><br/>                | <span data-ttu-id="fcd27-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="fcd27-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="fcd27-139">MOF</span><span class="sxs-lookup"><span data-stu-id="fcd27-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcd27-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fcd27-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fcd27-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fcd27-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcd27-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcd27-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

