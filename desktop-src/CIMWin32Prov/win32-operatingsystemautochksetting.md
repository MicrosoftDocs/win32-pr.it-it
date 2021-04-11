---
description: Questa classe rappresenta l'associazione tra un sistema operativo e le impostazioni di Autochk che si applicano ai dischi nel computer. Si noti che l'impostazione è associata al sistema operativo anziché al sistema del computer perché nel computer possono essere installati uno o più sistemi operativi, ognuno con le proprie impostazioni Autochk.
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystemAutochkSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 905ffc92273b46bb36b7b3e2909afea32e6baeff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127466"
---
# <a name="win32_operatingsystemautochksetting-class"></a><span data-ttu-id="cdaaa-103">Win32 \_ OperatingSystemAutochkSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="cdaaa-103">Win32\_OperatingSystemAutochkSetting class</span></span>

<span data-ttu-id="cdaaa-104">Questa classe rappresenta l'associazione tra un sistema operativo e le impostazioni di Autochk che si applicano ai dischi nel computer. Si noti che l'impostazione è associata al sistema operativo anziché al sistema del computer perché nel computer possono essere installati uno o più sistemi operativi, ognuno con le proprie impostazioni Autochk.</span><span class="sxs-lookup"><span data-stu-id="cdaaa-104">This class represents the association between an operating system and the autochk settings that apply to the disks on the machine.Note that the setting is associated to operating system rather than computer system since there can be one or more operating systems installed on the machine, each with its own autochk settings.</span></span>

<span data-ttu-id="cdaaa-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cdaaa-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdaaa-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdaaa-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="cdaaa-107">Members</span><span class="sxs-lookup"><span data-stu-id="cdaaa-107">Members</span></span>

<span data-ttu-id="cdaaa-108">La classe **Win32 \_ OperatingSystemAutochkSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cdaaa-108">The **Win32\_OperatingSystemAutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="cdaaa-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cdaaa-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdaaa-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cdaaa-110">Properties</span></span>

<span data-ttu-id="cdaaa-111">La classe **Win32 \_ OperatingSystemAutochkSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cdaaa-111">The **Win32\_OperatingSystemAutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cdaaa-112">**elemento**</span><span class="sxs-lookup"><span data-stu-id="cdaaa-112">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdaaa-113">Tipo di dati: **Win32 \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="cdaaa-113">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="cdaaa-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdaaa-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdaaa-115">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**Key**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="cdaaa-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="cdaaa-116">TBD</span><span class="sxs-lookup"><span data-stu-id="cdaaa-116">TBD</span></span>

</dd> <dt>

<span data-ttu-id="cdaaa-117">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="cdaaa-117">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdaaa-118">Tipo di dati: **Win32 \_ AutochkSetting**</span><span class="sxs-lookup"><span data-stu-id="cdaaa-118">Data type: **Win32\_AutochkSetting**</span></span>
</dt> <dt>

<span data-ttu-id="cdaaa-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdaaa-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdaaa-120">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("impostazione"), [**chiave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="cdaaa-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="cdaaa-121">TBD</span><span class="sxs-lookup"><span data-stu-id="cdaaa-121">TBD</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cdaaa-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdaaa-122">Requirements</span></span>



| <span data-ttu-id="cdaaa-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdaaa-123">Requirement</span></span> | <span data-ttu-id="cdaaa-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cdaaa-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdaaa-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdaaa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cdaaa-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cdaaa-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cdaaa-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdaaa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cdaaa-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdaaa-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cdaaa-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cdaaa-129">Namespace</span></span><br/>                | <span data-ttu-id="cdaaa-130">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="cdaaa-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cdaaa-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cdaaa-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdaaa-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdaaa-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdaaa-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cdaaa-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdaaa-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdaaa-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdaaa-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdaaa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdaaa-136">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="cdaaa-136">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

 
