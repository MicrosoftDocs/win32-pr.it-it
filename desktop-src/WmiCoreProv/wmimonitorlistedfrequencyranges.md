---
description: Elenca gli intervalli di frequenza supportati dal monitoraggio.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: Classe WmiMonitorListedFrequencyRanges
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e13828f6d5e844147fc0b041617c8452c503ceef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314100"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a><span data-ttu-id="1eb58-103">Classe WmiMonitorListedFrequencyRanges</span><span class="sxs-lookup"><span data-stu-id="1eb58-103">WmiMonitorListedFrequencyRanges class</span></span>

<span data-ttu-id="1eb58-104">La classe WMI **WmiMonitorListedFrequencyRanges** elenca gli intervalli di frequenza supportati dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="1eb58-104">The **WmiMonitorListedFrequencyRanges** WMI class lists the frequency ranges supported by the monitor.</span></span> <span data-ttu-id="1eb58-105">Questi intervalli si trovano nella definizione del video di input del blocco EDID (video Electronics Standard Association) Enhanced Extended Display Identification Data (E-) o nel file INF di Windows che contiene i dati del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1eb58-105">These ranges are found in Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) block or in the Windows INF file that contains device driver data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb58-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1eb58-106">Syntax</span></span>

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a><span data-ttu-id="1eb58-107">Members</span><span class="sxs-lookup"><span data-stu-id="1eb58-107">Members</span></span>

<span data-ttu-id="1eb58-108">La classe **WmiMonitorListedFrequencyRanges** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1eb58-108">The **WmiMonitorListedFrequencyRanges** class has these types of members:</span></span>

-   [<span data-ttu-id="1eb58-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1eb58-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1eb58-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1eb58-110">Properties</span></span>

<span data-ttu-id="1eb58-111">La classe **WmiMonitorListedFrequencyRanges** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1eb58-111">The **WmiMonitorListedFrequencyRanges** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1eb58-112">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="1eb58-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb58-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1eb58-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1eb58-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1eb58-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb58-115">Indica il monitoraggio attivo.</span><span class="sxs-lookup"><span data-stu-id="1eb58-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="1eb58-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="1eb58-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb58-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1eb58-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb58-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1eb58-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb58-119">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="1eb58-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1eb58-120">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="1eb58-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="1eb58-121">**MonitorFreqRanges**</span><span class="sxs-lookup"><span data-stu-id="1eb58-121">**MonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb58-122">Tipo di dati: matrice **FrequencyRangeDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1eb58-122">Data type: **FrequencyRangeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="1eb58-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1eb58-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb58-124">Elenco di intervalli di frequenza di monitoraggio rappresentati da istanze della classe [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="1eb58-124">List of monitor frequency ranges represented by instances of the [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1eb58-125">**NumOfMonitorFreqRanges**</span><span class="sxs-lookup"><span data-stu-id="1eb58-125">**NumOfMonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb58-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1eb58-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1eb58-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1eb58-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb58-128">Numero di intervalli di frequenza di monitoraggio supportati elencati.</span><span class="sxs-lookup"><span data-stu-id="1eb58-128">Number of listed supported monitor frequency ranges.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1eb58-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1eb58-129">Requirements</span></span>



| <span data-ttu-id="1eb58-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1eb58-130">Requirement</span></span> | <span data-ttu-id="1eb58-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1eb58-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb58-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1eb58-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1eb58-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1eb58-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1eb58-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1eb58-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1eb58-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1eb58-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1eb58-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1eb58-136">Namespace</span></span><br/>                | <span data-ttu-id="1eb58-137">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="1eb58-137">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1eb58-138">MOF</span><span class="sxs-lookup"><span data-stu-id="1eb58-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1eb58-139"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1eb58-139"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1eb58-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1eb58-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eb58-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1eb58-141"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eb58-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1eb58-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb58-143">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="1eb58-143">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




