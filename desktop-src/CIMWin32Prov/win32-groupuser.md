---
description: La \_ classe WMI dell'associazione GroupUser Win32 mette in correlazione un gruppo e un account membro di tale gruppo.
ms.assetid: 46dd65f0-b729-4b23-8a00-bc33d1a4868b
ms.tgt_platform: multiple
title: Classe Win32_GroupUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_GroupUser
- Win32_GroupUser.GroupComponent
- Win32_GroupUser.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 79035ff3c56331a240704cf6605fdf72efa4e81c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483700"
---
# <a name="win32_groupuser-class"></a><span data-ttu-id="17f64-103">Win32 \_ GroupUser (classe)</span><span class="sxs-lookup"><span data-stu-id="17f64-103">Win32\_GroupUser class</span></span>

<span data-ttu-id="17f64-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ GroupUser Win32** mette in correlazione un gruppo e un account membro di tale gruppo.</span><span class="sxs-lookup"><span data-stu-id="17f64-104">The **Win32\_GroupUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a group and an account that is a member of that group.</span></span>

<span data-ttu-id="17f64-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="17f64-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="17f64-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="17f64-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17f64-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17f64-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C508-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_GroupUser : CIM_Component
{
  Win32_Group   REF GroupComponent;
  Win32_Account REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="17f64-108">Members</span><span class="sxs-lookup"><span data-stu-id="17f64-108">Members</span></span>

<span data-ttu-id="17f64-109">La classe **Win32 \_ GroupUser** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="17f64-109">The **Win32\_GroupUser** class has these types of members:</span></span>

-   [<span data-ttu-id="17f64-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="17f64-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17f64-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="17f64-111">Properties</span></span>

<span data-ttu-id="17f64-112">La classe **Win32 \_ GroupUser** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="17f64-112">The **Win32\_GroupUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17f64-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="17f64-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f64-114">Tipo di dati **: \_ gruppo Win32**</span><span class="sxs-lookup"><span data-stu-id="17f64-114">Data type: **Win32\_Group**</span></span>
</dt> <dt>

<span data-ttu-id="17f64-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="17f64-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17f64-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| gruppo WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="17f64-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Group")</span></span>
</dt> </dl>

<span data-ttu-id="17f64-117">Riferimento all'istanza di che rappresenta il gruppo di cui l'account è membro.</span><span class="sxs-lookup"><span data-stu-id="17f64-117">Reference to the instance representing the group of which the account is a member.</span></span>

</dd> <dt>

<span data-ttu-id="17f64-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="17f64-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f64-119">Tipo di dati **: \_ account Win32**</span><span class="sxs-lookup"><span data-stu-id="17f64-119">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="17f64-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="17f64-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17f64-121">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| account Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="17f64-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Account")</span></span>
</dt> </dl>

<span data-ttu-id="17f64-122">Riferimento all'istanza di che rappresenta l'account utente o di sistema che fa parte di un gruppo di account.</span><span class="sxs-lookup"><span data-stu-id="17f64-122">Reference to the instance representing the user or system account that is a part of a group of accounts.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17f64-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="17f64-123">Remarks</span></span>

<span data-ttu-id="17f64-124">La classe **Win32 \_ GroupUser** è derivata dal [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="17f64-124">The **Win32\_GroupUser** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="examples"></a><span data-ttu-id="17f64-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="17f64-125">Examples</span></span>

<span data-ttu-id="17f64-126">Per un esempio di PowerShell sull'uso di Win32 \_ GroupUser per recuperare un elenco di membri del gruppo locale, vedere l' [elenco dei membri del gruppo locale in un computer remoto tramite WMI e PowerShell di esempio](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) nella raccolta TechNet.</span><span class="sxs-lookup"><span data-stu-id="17f64-126">For a PowerShell example of using Win32\_GroupUser to retrieve a list of local group members, see the [List local group members on a remote computer using WMI and PowerShell sample](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) on TechNet Gallery.</span></span>

<span data-ttu-id="17f64-127">Nell'esempio di codice VBScript [Information Retriever WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) della raccolta TechNet viene utilizzata la classe **Win32 \_ GroupUser** per recuperare le informazioni utente da un numero di computer remoti.</span><span class="sxs-lookup"><span data-stu-id="17f64-127">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_GroupUser** class to retrieve user information from a number of remote computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="17f64-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17f64-128">Requirements</span></span>



| <span data-ttu-id="17f64-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="17f64-129">Requirement</span></span> | <span data-ttu-id="17f64-130">Valore</span><span class="sxs-lookup"><span data-stu-id="17f64-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17f64-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17f64-131">Minimum supported client</span></span><br/> | <span data-ttu-id="17f64-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17f64-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17f64-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17f64-133">Minimum supported server</span></span><br/> | <span data-ttu-id="17f64-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17f64-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17f64-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17f64-135">Namespace</span></span><br/>                | <span data-ttu-id="17f64-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="17f64-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17f64-137">MOF</span><span class="sxs-lookup"><span data-stu-id="17f64-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17f64-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17f64-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17f64-139">DLL</span><span class="sxs-lookup"><span data-stu-id="17f64-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17f64-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17f64-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17f64-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17f64-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f64-142">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="17f64-142">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="17f64-143">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17f64-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

