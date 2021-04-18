---
description: Rappresenta la registrazione di un servizio nella piattaforma Microsoft Hyper-V.
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Classe Msvm_VirtualizationComponentRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e9704dcade0474a10ca60383280941ec2e3591b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306017"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a><span data-ttu-id="c3a2a-103">\_Classe MSVM VirtualizationComponentRegistration</span><span class="sxs-lookup"><span data-stu-id="c3a2a-103">Msvm\_VirtualizationComponentRegistration class</span></span>

<span data-ttu-id="c3a2a-104">Rappresenta la registrazione di un servizio nella piattaforma Microsoft Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="c3a2a-104">Represents the registration of a service in the Microsoft Hyper-V platform.</span></span>

<span data-ttu-id="c3a2a-105">La sintassi seguente è semplificata Managed Object Format codice (MOF).</span><span class="sxs-lookup"><span data-stu-id="c3a2a-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a2a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3a2a-106">Syntax</span></span>

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a><span data-ttu-id="c3a2a-107">Members</span><span class="sxs-lookup"><span data-stu-id="c3a2a-107">Members</span></span>

<span data-ttu-id="c3a2a-108">La **classe \_ VirtualizationComponentRegistration di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c3a2a-108">The **Msvm\_VirtualizationComponentRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="c3a2a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c3a2a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3a2a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c3a2a-110">Properties</span></span>

<span data-ttu-id="c3a2a-111">La **classe \_ VirtualizationComponentRegistration di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c3a2a-111">The **Msvm\_VirtualizationComponentRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3a2a-112">**Componente**</span><span class="sxs-lookup"><span data-stu-id="c3a2a-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a2a-113">Tipo di dati: **[ **MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="c3a2a-113">Data type: **[**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c3a2a-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c3a2a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3a2a-115">Riferimento a un'istanza di che descrive l'oggetto COM che implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="c3a2a-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="c3a2a-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="c3a2a-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a2a-117">Tipo di dati: **[ **MSVM \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="c3a2a-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c3a2a-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c3a2a-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3a2a-119">Riferimento a un'istanza di che descrive un tipo di risorsa supportato dal servizio.</span><span class="sxs-lookup"><span data-stu-id="c3a2a-119">A reference to an instance that describes a resource type supported by the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3a2a-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3a2a-120">Remarks</span></span>

<span data-ttu-id="c3a2a-121">L'accesso alla **classe \_ VirtualizationComponentRegistration di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="c3a2a-121">Access to the **Msvm\_VirtualizationComponentRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c3a2a-122">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c3a2a-122">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a2a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3a2a-123">Requirements</span></span>



| <span data-ttu-id="c3a2a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3a2a-124">Requirement</span></span> | <span data-ttu-id="c3a2a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c3a2a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a2a-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3a2a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a2a-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c3a2a-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c3a2a-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3a2a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a2a-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c3a2a-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3a2a-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c3a2a-130">End of client support</span></span><br/>    | <span data-ttu-id="c3a2a-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c3a2a-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c3a2a-132">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="c3a2a-132">End of server support</span></span><br/>    | <span data-ttu-id="c3a2a-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c3a2a-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c3a2a-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c3a2a-134">Namespace</span></span><br/>                | <span data-ttu-id="c3a2a-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c3a2a-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c3a2a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c3a2a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3a2a-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3a2a-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3a2a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c3a2a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3a2a-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3a2a-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

