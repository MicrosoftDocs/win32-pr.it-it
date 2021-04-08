---
description: Descrive i dati dell'impostazione per una porta seriale virtuale.
ms.assetid: 8b257bbf-495a-4eef-86a1-70e31e4a85a5
title: Classe Msvm_SerialPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortSettingData
- Msvm_SerialPortSettingData.DebuggerMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 21a1ab58608c5631a328795272d6a04aa56aedf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882157"
---
# <a name="msvm_serialportsettingdata-class"></a><span data-ttu-id="b6aa0-103">\_Classe MSVM SerialPortSettingData</span><span class="sxs-lookup"><span data-stu-id="b6aa0-103">Msvm\_SerialPortSettingData class</span></span>

<span data-ttu-id="b6aa0-104">Descrive i dati dell'impostazione per una porta seriale virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6aa0-104">Describes the setting data for a virtual serial port.</span></span>

<span data-ttu-id="b6aa0-105">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b6aa0-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6aa0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6aa0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortSettingData : CIM_ResourceAllocationSettingData
{
  boolean DebuggerMode;
};
```

## <a name="members"></a><span data-ttu-id="b6aa0-107">Members</span><span class="sxs-lookup"><span data-stu-id="b6aa0-107">Members</span></span>

<span data-ttu-id="b6aa0-108">La **classe \_ SerialPortSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b6aa0-108">The **Msvm\_SerialPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b6aa0-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b6aa0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6aa0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b6aa0-110">Properties</span></span>

<span data-ttu-id="b6aa0-111">La **classe \_ SerialPortSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b6aa0-111">The **Msvm\_SerialPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6aa0-112">**DebuggerMode**</span><span class="sxs-lookup"><span data-stu-id="b6aa0-112">**DebuggerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6aa0-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b6aa0-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6aa0-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b6aa0-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b6aa0-115">**true** se la modalità del debugger è abilitata su una porta seriale virtuale; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b6aa0-115">**true** if the debugger mode is enabled on a virtual serial port; otherwise, **false**.</span></span> <span data-ttu-id="b6aa0-116">La modalità debugger consente di migliorare l'utilizzo di un debugger del kernel di Microsoft Windows su una porta seriale virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6aa0-116">The debugger mode enhances the use of a Microsoft Windows kernel debugger over a virtual serial port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6aa0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6aa0-117">Requirements</span></span>



| <span data-ttu-id="b6aa0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6aa0-118">Requirement</span></span> | <span data-ttu-id="b6aa0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b6aa0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6aa0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6aa0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6aa0-121">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b6aa0-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b6aa0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6aa0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6aa0-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b6aa0-123">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b6aa0-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b6aa0-124">Namespace</span></span><br/>                | <span data-ttu-id="b6aa0-125">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b6aa0-125">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b6aa0-126">MOF</span><span class="sxs-lookup"><span data-stu-id="b6aa0-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6aa0-127"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6aa0-127"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6aa0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b6aa0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6aa0-129"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b6aa0-129"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b6aa0-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6aa0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6aa0-131">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="b6aa0-131">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




