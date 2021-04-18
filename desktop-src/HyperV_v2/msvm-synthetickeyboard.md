---
description: Rappresenta un dispositivo di tastiera sintetico.
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Classe Msvm_SyntheticKeyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64ac153a2c20815891d8a39fd10f58562ed8d81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306028"
---
# <a name="msvm_synthetickeyboard-class"></a><span data-ttu-id="c8663-103">\_Classe MSVM SyntheticKeyboard</span><span class="sxs-lookup"><span data-stu-id="c8663-103">Msvm\_SyntheticKeyboard class</span></span>

<span data-ttu-id="c8663-104">Rappresenta un dispositivo di tastiera sintetico.</span><span class="sxs-lookup"><span data-stu-id="c8663-104">Represents a synthetic keyboard device.</span></span>

<span data-ttu-id="c8663-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c8663-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8663-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8663-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a><span data-ttu-id="c8663-107">Members</span><span class="sxs-lookup"><span data-stu-id="c8663-107">Members</span></span>

<span data-ttu-id="c8663-108">La **classe \_ SyntheticKeyboard di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c8663-108">The **Msvm\_SyntheticKeyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="c8663-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="c8663-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c8663-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="c8663-110">Methods</span></span>

<span data-ttu-id="c8663-111">La **classe \_ SyntheticKeyboard di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c8663-111">The **Msvm\_SyntheticKeyboard** class has these methods.</span></span>



| <span data-ttu-id="c8663-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="c8663-112">Method</span></span>                                                                  | <span data-ttu-id="c8663-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8663-113">Description</span></span>                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="c8663-114">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c8663-114">**RequestStateChange**</span></span>](msvm-synthetickeyboard-requeststatechange.md) | <span data-ttu-id="c8663-115">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="c8663-115">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="c8663-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="c8663-116">**Reset**</span></span>](msvm-synthetickeyboard-reset.md)                           | <span data-ttu-id="c8663-117">Reimposta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8663-117">resets the device.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="c8663-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8663-118">Requirements</span></span>



| <span data-ttu-id="c8663-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8663-119">Requirement</span></span> | <span data-ttu-id="c8663-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c8663-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8663-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8663-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c8663-122">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c8663-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c8663-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8663-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c8663-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c8663-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c8663-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c8663-125">Namespace</span></span><br/>                | <span data-ttu-id="c8663-126">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c8663-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c8663-127">MOF</span><span class="sxs-lookup"><span data-stu-id="c8663-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8663-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8663-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8663-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c8663-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8663-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c8663-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c8663-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8663-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8663-132">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c8663-132">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

 




