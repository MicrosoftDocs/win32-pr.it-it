---
description: Associa una testa video al controller video che lo include.
ms.assetid: D072DF7C-D55B-4203-9FE5-B395D1EC1632
title: Classe Msvm_VideoHeadOnController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHeadOnController
- Msvm_VideoHeadOnController.Antecedent
- Msvm_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11065c7b7a9e23b786697c3d4f0dbd63e67d6b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131519"
---
# <a name="msvm_videoheadoncontroller-class"></a><span data-ttu-id="b671e-103">\_Classe MSVM VideoHeadOnController</span><span class="sxs-lookup"><span data-stu-id="b671e-103">Msvm\_VideoHeadOnController class</span></span>

<span data-ttu-id="b671e-104">Associa una testa video al controller video che lo include.</span><span class="sxs-lookup"><span data-stu-id="b671e-104">Associates a video head with the video controller that includes it.</span></span>

<span data-ttu-id="b671e-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b671e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b671e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b671e-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHeadOnController : CIM_VideoHeadOnController
{
  CIM_DisplayController REF Antecedent;
  Msvm_VideoHead        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b671e-107">Members</span><span class="sxs-lookup"><span data-stu-id="b671e-107">Members</span></span>

<span data-ttu-id="b671e-108">La **classe \_ VideoHeadOnController di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b671e-108">The **Msvm\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="b671e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b671e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b671e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b671e-110">Properties</span></span>

<span data-ttu-id="b671e-111">La **classe \_ VideoHeadOnController di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b671e-111">The **Msvm\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b671e-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b671e-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b671e-113">Tipo di dati: **[ **CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b671e-113">Data type: **[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="b671e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b671e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b671e-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="b671e-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b671e-116">Controller video che include l'intestazione.</span><span class="sxs-lookup"><span data-stu-id="b671e-116">The video controller that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="b671e-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="b671e-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b671e-118">Tipo di dati: **[ **MSVM \_ VideoHead**](msvm-videohead.md)**</span><span class="sxs-lookup"><span data-stu-id="b671e-118">Data type: **[**Msvm\_VideoHead**](msvm-videohead.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b671e-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b671e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b671e-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="b671e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b671e-121">L'intestazione del dispositivo video.</span><span class="sxs-lookup"><span data-stu-id="b671e-121">The head on the video device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b671e-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="b671e-122">Remarks</span></span>

<span data-ttu-id="b671e-123">L'accesso alla **classe \_ VideoHeadOnController di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="b671e-123">Access to the **Msvm\_VideoHeadOnController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b671e-124">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b671e-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b671e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b671e-125">Requirements</span></span>



| <span data-ttu-id="b671e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b671e-126">Requirement</span></span> | <span data-ttu-id="b671e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b671e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b671e-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b671e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b671e-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b671e-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b671e-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b671e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b671e-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b671e-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b671e-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b671e-132">Namespace</span></span><br/>                | <span data-ttu-id="b671e-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b671e-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b671e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b671e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b671e-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b671e-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b671e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b671e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b671e-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b671e-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b671e-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b671e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b671e-139">**\_VIDEOHEADONCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="b671e-139">**CIM\_VideoHeadOnController**</span></span>](cim-videoheadoncontroller.md)
</dt> <dt>

<span data-ttu-id="b671e-140">[**\_VIDEOHEADONCONTROLLER CIM**](/previous-versions//cc136950(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b671e-140">[**CIM\_VideoHeadOnController**](/previous-versions//cc136950(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b671e-141">Classi video</span><span class="sxs-lookup"><span data-stu-id="b671e-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

