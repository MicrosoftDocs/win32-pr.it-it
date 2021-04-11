---
description: CIM \_ ProcessIndication è una superclasse astratta per le classi di indicazione specializzate, che affrontano modifiche e avvisi specifici pubblicati da provider e strumentazione.
ms.assetid: b321b5ec-4868-4149-99ad-4596fd49c39b
title: Classe CIM_ProcessIndication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessIndication
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5e0bd9539c43290e4972494d062e6983e64defb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233318"
---
# <a name="cim_processindication-class"></a><span data-ttu-id="16802-103">CIM \_ ProcessIndication (classe)</span><span class="sxs-lookup"><span data-stu-id="16802-103">CIM\_ProcessIndication class</span></span>

<span data-ttu-id="16802-104">**CIM \_ ProcessIndication** è una superclasse astratta per le classi di indicazione specializzate, che affrontano modifiche e avvisi specifici pubblicati da provider e strumentazione.</span><span class="sxs-lookup"><span data-stu-id="16802-104">**CIM\_ProcessIndication** is an abstract superclass for specialized indication classes, that address specific changes and alerts published by providers and instrumentation.</span></span>

## <a name="syntax"></a><span data-ttu-id="16802-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16802-105">Syntax</span></span>

``` syntax
[Indication, Version("2.6.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_ProcessIndication : CIM_Indication
{
};
```

## <a name="members"></a><span data-ttu-id="16802-106">Members</span><span class="sxs-lookup"><span data-stu-id="16802-106">Members</span></span>

<span data-ttu-id="16802-107">La classe **CIM \_ ProcessIndication** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="16802-107">The **CIM\_ProcessIndication** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="16802-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16802-108">Requirements</span></span>



| <span data-ttu-id="16802-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="16802-109">Requirement</span></span> | <span data-ttu-id="16802-110">Valore</span><span class="sxs-lookup"><span data-stu-id="16802-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16802-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16802-111">Minimum supported client</span></span><br/> | <span data-ttu-id="16802-112">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="16802-112">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="16802-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16802-113">Minimum supported server</span></span><br/> | <span data-ttu-id="16802-114">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="16802-114">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="16802-115">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="16802-115">Namespace</span></span><br/>                | <span data-ttu-id="16802-116">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="16802-116">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="16802-117">MOF</span><span class="sxs-lookup"><span data-stu-id="16802-117">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16802-118"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16802-118"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16802-119">DLL</span><span class="sxs-lookup"><span data-stu-id="16802-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16802-120"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16802-120"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="16802-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16802-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16802-122">**\_Indicazione CIM**</span><span class="sxs-lookup"><span data-stu-id="16802-122">**CIM\_Indication**</span></span>](cim-indication.md)
</dt> </dl>

 

 




