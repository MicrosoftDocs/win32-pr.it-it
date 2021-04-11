---
description: Contiene il tipo di connessione del monitoraggio.
ms.assetid: f5658246-fbb8-4530-8dfb-f1ca792fe9d5
title: Classe WmiMonitorConnectionParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorConnectionParams
- WmiMonitorConnectionParams.Active
- WmiMonitorConnectionParams.InstanceName
- WmiMonitorConnectionParams.VideoOutputTechnology
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 64212c523459696ced37e42689f6a4be0edb056b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232409"
---
# <a name="wmimonitorconnectionparams-class"></a><span data-ttu-id="77e0e-103">Classe WmiMonitorConnectionParams</span><span class="sxs-lookup"><span data-stu-id="77e0e-103">WmiMonitorConnectionParams class</span></span>

<span data-ttu-id="77e0e-104">La classe WMI WmiMonitorConnectionParams contiene il tipo di connessione del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="77e0e-104">The WmiMonitorConnectionParams WMI class contains the connection type of the monitor.</span></span>

<span data-ttu-id="77e0e-105">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="77e0e-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="77e0e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77e0e-106">Syntax</span></span>

``` syntax
class WmiMonitorConnectionParams
{
  boolean Active;
  string  InstanceName;
  uint32  VideoOutputTechnology;
};
```

## <a name="members"></a><span data-ttu-id="77e0e-107">Members</span><span class="sxs-lookup"><span data-stu-id="77e0e-107">Members</span></span>

<span data-ttu-id="77e0e-108">La classe **WmiMonitorConnectionParams** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="77e0e-108">The **WmiMonitorConnectionParams** class has these types of members:</span></span>

-   [<span data-ttu-id="77e0e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="77e0e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77e0e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="77e0e-110">Properties</span></span>

<span data-ttu-id="77e0e-111">La classe **WmiMonitorConnectionParams** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="77e0e-111">The **WmiMonitorConnectionParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77e0e-112">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="77e0e-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77e0e-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="77e0e-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77e0e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="77e0e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77e0e-115">Indica il monitoraggio attivo.</span><span class="sxs-lookup"><span data-stu-id="77e0e-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="77e0e-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="77e0e-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77e0e-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="77e0e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77e0e-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="77e0e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77e0e-119">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="77e0e-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="77e0e-120">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="77e0e-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="77e0e-121">**VideoOutputTechnology**</span><span class="sxs-lookup"><span data-stu-id="77e0e-121">**VideoOutputTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77e0e-122">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77e0e-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77e0e-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="77e0e-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77e0e-124">Tipo di connessione della tecnologia di output video.</span><span class="sxs-lookup"><span data-stu-id="77e0e-124">Video output technology connection type.</span></span> <span data-ttu-id="77e0e-125">I valori validi sono documentati nell'enumerazione [D3DKMDT \_ video \_ output \_ Technology](https://msdn.microsoft.com/library/ms794498.aspx) .</span><span class="sxs-lookup"><span data-stu-id="77e0e-125">Valid values are documented in the [D3DKMDT\_VIDEO\_OUTPUT\_TECHNOLOGY](https://msdn.microsoft.com/library/ms794498.aspx) enumeration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77e0e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77e0e-126">Requirements</span></span>



| <span data-ttu-id="77e0e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="77e0e-127">Requirement</span></span> | <span data-ttu-id="77e0e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="77e0e-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77e0e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77e0e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="77e0e-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77e0e-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="77e0e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77e0e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="77e0e-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77e0e-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="77e0e-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="77e0e-133">Namespace</span></span><br/>                | <span data-ttu-id="77e0e-134">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="77e0e-134">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="77e0e-135">MOF</span><span class="sxs-lookup"><span data-stu-id="77e0e-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77e0e-136"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77e0e-136"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="77e0e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="77e0e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77e0e-138"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77e0e-138"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77e0e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77e0e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e0e-140">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="77e0e-140">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




