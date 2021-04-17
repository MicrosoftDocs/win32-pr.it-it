---
description: La \_ classe Win32 LogonSessionMappedDisk rappresenta un'associazione tra una sessione di accesso e i dischi logici mappati definiti all'interno della sessione.
ms.assetid: 013ae55e-6dd1-42fb-bcba-74d6afa1b905
ms.tgt_platform: multiple
title: Classe Win32_LogonSessionMappedDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSessionMappedDisk
- Win32_LogonSessionMappedDisk.Antecedent
- Win32_LogonSessionMappedDisk.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 203c9dd783dece52fa19905d51ece3bc26584dc6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524266"
---
# <a name="win32_logonsessionmappeddisk-class"></a><span data-ttu-id="8575e-103">Win32 \_ LogonSessionMappedDisk (classe)</span><span class="sxs-lookup"><span data-stu-id="8575e-103">Win32\_LogonSessionMappedDisk class</span></span>

<span data-ttu-id="8575e-104">La \_ classe Win32 LogonSessionMappedDisk rappresenta un'associazione tra una sessione di accesso e i dischi logici mappati definiti all'interno della sessione.</span><span class="sxs-lookup"><span data-stu-id="8575e-104">The Win32\_LogonSessionMappedDisk class represents an association between a logon session and the mapped logical disks defined within the session.</span></span>

<span data-ttu-id="8575e-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8575e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8575e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8575e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_LogonSessionMappedDisk : CIM_Dependency
{
  Win32_LogonSession      REF Antecedent;
  Win32_MappedLogicalDisk REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="8575e-107">Members</span><span class="sxs-lookup"><span data-stu-id="8575e-107">Members</span></span>

<span data-ttu-id="8575e-108">La classe **Win32 \_ LogonSessionMappedDisk** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8575e-108">The **Win32\_LogonSessionMappedDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="8575e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8575e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8575e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8575e-110">Properties</span></span>

<span data-ttu-id="8575e-111">La classe **Win32 \_ LogonSessionMappedDisk** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8575e-111">The **Win32\_LogonSessionMappedDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8575e-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="8575e-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8575e-113">Tipo di dati: **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="8575e-113">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="8575e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8575e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8575e-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8575e-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8575e-116">La proprietà precedente fa riferimento a una sessione di accesso.</span><span class="sxs-lookup"><span data-stu-id="8575e-116">The Antecedent property references a logon session.</span></span>

</dd> <dt>

<span data-ttu-id="8575e-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="8575e-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8575e-118">Tipo di dati: **Win32 \_ MappedLogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="8575e-118">Data type: **Win32\_MappedLogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="8575e-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8575e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8575e-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8575e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8575e-121">La proprietà dipendente fa riferimento a un disco logico mappato definito all'interno della sessione a cui fa riferimento la proprietà precedente.</span><span class="sxs-lookup"><span data-stu-id="8575e-121">The Dependent property references a mapped logical disk defined within the session referenced by the Antecedent property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8575e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8575e-122">Requirements</span></span>



| <span data-ttu-id="8575e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8575e-123">Requirement</span></span> | <span data-ttu-id="8575e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8575e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8575e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8575e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8575e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8575e-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8575e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8575e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8575e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8575e-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8575e-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8575e-129">Namespace</span></span><br/>                | <span data-ttu-id="8575e-130">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8575e-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8575e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8575e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8575e-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8575e-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8575e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8575e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8575e-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8575e-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8575e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8575e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8575e-136">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="8575e-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

