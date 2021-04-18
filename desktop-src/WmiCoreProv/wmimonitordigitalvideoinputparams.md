---
description: Rappresenta i parametri di input per i video digitali.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: Classe WmiMonitorDigitalVideoInputParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a08e38a38bb5f5e8d539fabdf69c429c42f4b1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315741"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a><span data-ttu-id="b5831-103">Classe WmiMonitorDigitalVideoInputParams</span><span class="sxs-lookup"><span data-stu-id="b5831-103">WmiMonitorDigitalVideoInputParams class</span></span>

<span data-ttu-id="b5831-104">**WmiMonitorDigitalVideoInputParams** rappresenta i parametri di input per i video digitali.</span><span class="sxs-lookup"><span data-stu-id="b5831-104">The **WmiMonitorDigitalVideoInputParams** represents input parameters for digital video.</span></span> <span data-ttu-id="b5831-105">I dati in questa classe corrispondono ai dati nella definizione del video di input di video Electronics Standard Association (VESA) Enhanced Extended Display Data (E-EDID) standard.</span><span class="sxs-lookup"><span data-stu-id="b5831-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="b5831-106">Un'istanza di questa classe è disponibile solo se il valore della proprietà **VideoInputType** della classe [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) è "Digital".</span><span class="sxs-lookup"><span data-stu-id="b5831-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Digital".</span></span>

## <a name="syntax"></a><span data-ttu-id="b5831-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5831-107">Syntax</span></span>

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a><span data-ttu-id="b5831-108">Members</span><span class="sxs-lookup"><span data-stu-id="b5831-108">Members</span></span>

<span data-ttu-id="b5831-109">La classe **WmiMonitorDigitalVideoInputParams** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b5831-109">The **WmiMonitorDigitalVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="b5831-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b5831-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5831-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b5831-111">Properties</span></span>

<span data-ttu-id="b5831-112">La classe **WmiMonitorDigitalVideoInputParams** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b5831-112">The **WmiMonitorDigitalVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5831-113">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="b5831-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5831-114">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b5831-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5831-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5831-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5831-116">Indica il monitoraggio attivo.</span><span class="sxs-lookup"><span data-stu-id="b5831-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b5831-117">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="b5831-117">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5831-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5831-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5831-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5831-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5831-120">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="b5831-120">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b5831-121">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="b5831-121">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="b5831-122">**IsDFP1xCompatible**</span><span class="sxs-lookup"><span data-stu-id="b5831-122">**IsDFP1xCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5831-123">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b5831-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5831-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5831-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5831-125">VESA DFP 1. x o compatibile.</span><span class="sxs-lookup"><span data-stu-id="b5831-125">VESA DFP 1.x or compatible.</span></span> <span data-ttu-id="b5831-126">Se impostato, l'interfaccia è compatibile con i segnali con VESA Digital Flat Panel (DFP) 1. x transizione ridotta a icona (TMDS) CRGB, 1 pixel/clock, fino a 8 bit/colore più significativo (MSB) allineato, DE Active High.</span><span class="sxs-lookup"><span data-stu-id="b5831-126">If set, interface is signal compatible with VESA Digital Flat Panel (DFP) 1.x Transition Minimized Differential Signaling (TMDS) CRGB, 1 pixel/clock, up to 8 bits/color most significant bit (MSB) aligned, DE active high.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5831-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5831-127">Requirements</span></span>



| <span data-ttu-id="b5831-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5831-128">Requirement</span></span> | <span data-ttu-id="b5831-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b5831-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5831-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5831-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b5831-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5831-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b5831-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5831-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b5831-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5831-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b5831-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b5831-134">Namespace</span></span><br/>                | <span data-ttu-id="b5831-135">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="b5831-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b5831-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b5831-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5831-137"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5831-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5831-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b5831-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5831-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5831-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5831-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5831-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5831-141">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="b5831-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




