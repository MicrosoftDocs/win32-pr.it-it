---
description: L' \_ associazione Win32 SessionResource rappresenta la relazione tra una sessione e le risorse a cui la sessione fornisce l'accesso.
ms.assetid: 39c195cf-e70b-4e93-b46b-61ed4f08f57e
ms.tgt_platform: multiple
title: Classe Win32_SessionResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionResource
- Win32_SessionResource.Antecedent
- Win32_SessionResource.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 3962c8523863bb97710bf21be38906d3897beea3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748786"
---
# <a name="win32_sessionresource-class"></a><span data-ttu-id="5105e-103">Win32 \_ SessionResource (classe)</span><span class="sxs-lookup"><span data-stu-id="5105e-103">Win32\_SessionResource class</span></span>

<span data-ttu-id="5105e-104">L' \_ associazione Win32 SessionResource rappresenta la relazione tra una sessione e le risorse a cui la sessione fornisce l'accesso.</span><span class="sxs-lookup"><span data-stu-id="5105e-104">The Win32\_SessionResource association represents the relationship between a session and the resources that the session provides access to.</span></span>

<span data-ttu-id="5105e-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5105e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5105e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5105e-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SessionResource : CIM_Dependency
{
  Win32_LogicalElement REF Antecedent;
  Win32_Session        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5105e-107">Members</span><span class="sxs-lookup"><span data-stu-id="5105e-107">Members</span></span>

<span data-ttu-id="5105e-108">La classe **Win32 \_ SessionResource** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5105e-108">The **Win32\_SessionResource** class has these types of members:</span></span>

-   [<span data-ttu-id="5105e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5105e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5105e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5105e-110">Properties</span></span>

<span data-ttu-id="5105e-111">La classe **Win32 \_ SessionResource** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5105e-111">The **Win32\_SessionResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5105e-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5105e-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5105e-113">Tipo di dati **: \_ LogicalElement Win32**</span><span class="sxs-lookup"><span data-stu-id="5105e-113">Data type: **Win32\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="5105e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5105e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5105e-115">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="5105e-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5105e-116">Il riferimento precedente rappresenta le risorse usate da questa sessione.</span><span class="sxs-lookup"><span data-stu-id="5105e-116">The Antecedent reference represents resources used by this session.</span></span>

</dd> <dt>

<span data-ttu-id="5105e-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="5105e-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5105e-118">Tipo di dati **: \_ sessione Win32**</span><span class="sxs-lookup"><span data-stu-id="5105e-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="5105e-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5105e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5105e-120">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="5105e-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5105e-121">Il riferimento dipendente rappresenta la sessione usando la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5105e-121">The Dependent reference represents the session using the resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5105e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5105e-122">Requirements</span></span>



| <span data-ttu-id="5105e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5105e-123">Requirement</span></span> | <span data-ttu-id="5105e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5105e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5105e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5105e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5105e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5105e-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5105e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5105e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5105e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5105e-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5105e-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5105e-129">Namespace</span></span><br/>                | <span data-ttu-id="5105e-130">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5105e-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5105e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5105e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5105e-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5105e-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5105e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5105e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5105e-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5105e-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5105e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5105e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5105e-136">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="5105e-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
