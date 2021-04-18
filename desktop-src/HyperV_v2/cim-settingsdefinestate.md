---
description: Associa i dati delle impostazioni a un elemento gestito.
ms.assetid: 3fdf111b-3ec1-4559-94ce-27d6a8cd0080
title: Classe CIM_SettingsDefineState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineState
- CIM_SettingsDefineState.ManagedElement
- CIM_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1931b365108bb7b3df4269ae6acbb78292a0401d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314837"
---
# <a name="cim_settingsdefinestate-class"></a><span data-ttu-id="dfd7b-103">CIM \_ SettingsDefineState (classe)</span><span class="sxs-lookup"><span data-stu-id="dfd7b-103">CIM\_SettingsDefineState class</span></span>

<span data-ttu-id="dfd7b-104">Associa i dati delle impostazioni a un elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="dfd7b-104">Associates settings data with a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd7b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfd7b-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Settings")]
class CIM_SettingsDefineState
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="dfd7b-106">Members</span><span class="sxs-lookup"><span data-stu-id="dfd7b-106">Members</span></span>

<span data-ttu-id="dfd7b-107">La classe **CIM \_ SettingsDefineState** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dfd7b-107">The **CIM\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="dfd7b-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dfd7b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dfd7b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dfd7b-109">Properties</span></span>

<span data-ttu-id="dfd7b-110">La classe **CIM \_ SettingsDefineState** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dfd7b-110">The **CIM\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dfd7b-111">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="dfd7b-111">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfd7b-112">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="dfd7b-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="dfd7b-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dfd7b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfd7b-114">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dfd7b-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dfd7b-115">Elemento gestito nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="dfd7b-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="dfd7b-116">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="dfd7b-116">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfd7b-117">Tipo di dati: **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="dfd7b-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="dfd7b-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dfd7b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfd7b-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dfd7b-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dfd7b-120">Dati delle impostazioni nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="dfd7b-120">The settings data in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dfd7b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfd7b-121">Requirements</span></span>



| <span data-ttu-id="dfd7b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfd7b-122">Requirement</span></span> | <span data-ttu-id="dfd7b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="dfd7b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd7b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfd7b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dfd7b-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dfd7b-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="dfd7b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfd7b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dfd7b-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dfd7b-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="dfd7b-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dfd7b-128">Namespace</span></span><br/>                | <span data-ttu-id="dfd7b-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="dfd7b-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dfd7b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="dfd7b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfd7b-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfd7b-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfd7b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dfd7b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfd7b-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dfd7b-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

