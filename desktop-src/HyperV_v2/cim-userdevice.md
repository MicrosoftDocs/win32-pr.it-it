---
description: Rappresenta un dispositivo logico che consente a un utente di immettere, visualizzare o ascoltare i dati nel computer.
ms.assetid: 95f88a63-3a2a-4b8c-9849-564dac254933
title: Classe CIM_UserDevice (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.IsLocked
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8776c0b5e9ddf1653747b82e94040197e4c56f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880754"
---
# <a name="cim_userdevice-class-hyper-v-management"></a><span data-ttu-id="a2f02-103">Classe CIM_UserDevice (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="a2f02-103">CIM_UserDevice class (Hyper-V management)</span></span>

<span data-ttu-id="a2f02-104">Rappresenta un dispositivo logico che consente a un utente di immettere, visualizzare o ascoltare i dati nel computer.</span><span class="sxs-lookup"><span data-stu-id="a2f02-104">Represents a logical device that allows a user to input, view or hear data on the computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2f02-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2f02-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
{
  boolean IsLocked;
};
```

## <a name="members"></a><span data-ttu-id="a2f02-106">Members</span><span class="sxs-lookup"><span data-stu-id="a2f02-106">Members</span></span>

<span data-ttu-id="a2f02-107">La classe **CIM \_ UserDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a2f02-107">The **CIM\_UserDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="a2f02-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a2f02-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2f02-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a2f02-109">Properties</span></span>

<span data-ttu-id="a2f02-110">La classe **CIM \_ UserDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a2f02-110">The **CIM\_UserDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2f02-111">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="a2f02-111">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2f02-112">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a2f02-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2f02-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a2f02-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2f02-114">**true** se il dispositivo è bloccato, impedendo l'input o l'output dell'utente; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a2f02-114">**true** if the device is locked, preventing user input or output; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2f02-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2f02-115">Requirements</span></span>



| <span data-ttu-id="a2f02-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2f02-116">Requirement</span></span> | <span data-ttu-id="a2f02-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a2f02-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f02-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2f02-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a2f02-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a2f02-119">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a2f02-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2f02-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a2f02-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2f02-121">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a2f02-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a2f02-122">Namespace</span></span><br/>                | <span data-ttu-id="a2f02-123">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a2f02-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a2f02-124">MOF</span><span class="sxs-lookup"><span data-stu-id="a2f02-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2f02-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2f02-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2f02-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a2f02-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2f02-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2f02-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2f02-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2f02-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2f02-129">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a2f02-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




