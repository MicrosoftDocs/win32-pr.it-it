---
title: DXCoreAdapterProperty
description: Definisce le costanti che specificano le proprietà dell'adapter DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 645f0a890aac9a50cdf2987c0736a85142a91aff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299997"
---
# <a name="dxcoreadapterproperty-enum"></a><span data-ttu-id="4cdfd-103">Enumerazione DXCoreAdapterProperty</span><span class="sxs-lookup"><span data-stu-id="4cdfd-103">DXCoreAdapterProperty enum</span></span>

<span data-ttu-id="4cdfd-104">Definisce le costanti che specificano le proprietà dell'adapter DXCore.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-104">Defines constants that specify DXCore adapter properties.</span></span> <span data-ttu-id="4cdfd-105">Passare una di queste costanti al metodo [IDXCoreAdapter:: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) per recuperare la dimensione del buffer necessaria per ricevere il valore della proprietà corrispondente; passare quindi la stessa costante al metodo [IDXCoreAdapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) per recuperare il valore della proprietà in un buffer allocato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-105">Pass one of these constants to the [IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) method to retrieve the buffer size necessary to receive the value of the corresponding property; then pass the same constant to the [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) method to retrieve the property's value in a buffer that you allocate.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cdfd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cdfd-106">Syntax</span></span>

```cpp
enum class DXCoreAdapterProperty : uint32_t
{
  InstanceLuid = 0,
  DriverVersion = 1,
  DriverDescription = 2,
  HardwareID = 3,
  KmdModelVersion = 4,
  ComputePreemptionGranularity = 5,
  GraphicsPreemptionGranularity = 6,
  DedicatedAdapterMemory = 7,
  DedicatedSystemMemory = 8,
  SharedSystemMemory = 9,
  AcgCompatible = 10,
  IsHardware = 11,
  IsIntegrated = 12,
  IsDetachable = 13
};
```

## <a name="constants"></a><span data-ttu-id="4cdfd-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="4cdfd-107">Constants</span></span>

### <a name="instanceluid"></a><span data-ttu-id="4cdfd-108">InstanceLuid</span><span class="sxs-lookup"><span data-stu-id="4cdfd-108">InstanceLuid</span></span>

<span data-ttu-id="4cdfd-109">Specifica la proprietà dell'adapter <em>InstanceLuid</em> , che contiene un identificatore univoco locale che rappresenta l'adapter.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-109">Specifies the <em>InstanceLuid</em> adapter property, which contains a locally unique identifier representing the adapter.</span></span> <span data-ttu-id="4cdfd-110">Questo valore rimane costante per la durata di questo adapter.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-110">This value remains constant for the lifetime of this adapter.</span></span> <span data-ttu-id="4cdfd-111">Il LUID di una scheda cambia al riavvio, all'aggiornamento del driver o alla disabilitazione o all'abilitazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-111">The LUID of an adapter changes on reboot, driver upgrade, or device disablement/enablement.</span></span>

<span data-ttu-id="4cdfd-112">Il tipo della proprietà dell'adattatore <em>InstanceLuid</em> è <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-112">The <em>InstanceLuid</em> adapter property has type <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.</span></span>

### <a name="driverversion"></a><span data-ttu-id="4cdfd-113">DriverVersion</span><span class="sxs-lookup"><span data-stu-id="4cdfd-113">DriverVersion</span></span>

<span data-ttu-id="4cdfd-114">Specifica la proprietà dell'adapter <em>DriverVersion</em> , che contiene la versione del driver, rappresentata in <b>WORD</b>s come <b>LARGE_INTEGER</b>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-114">Specifies the <em>DriverVersion</em> adapter property, which contains the driver version, represented in <b>WORD</b>s as a <b>LARGE_INTEGER</b>.</span></span>

<span data-ttu-id="4cdfd-115">La proprietà dell'adapter <em>DriverVersion</em> è di tipo <b>uint64_t</b>, che rappresenta un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-115">The <em>DriverVersion</em> adapter property has type <b>uint64_t</b>, representing a Boolean value.</span></span>

### <a name="driverdescription"></a><span data-ttu-id="4cdfd-116">DriverDescription</span><span class="sxs-lookup"><span data-stu-id="4cdfd-116">DriverDescription</span></span>

<span data-ttu-id="4cdfd-117">Specifica la proprietà dell'adattatore <em>DriverDescription</em> , che contiene una matrice con terminazione null di <b>char</b>s che descrive il driver, come specificato dal driver, nella codifica <a href="/windows/win32/intl/unicode">UTF-8</a> .</span><span class="sxs-lookup"><span data-stu-id="4cdfd-117">Specifies the <em>DriverDescription</em> adapter property, which contains a NULL-terminated array of <b>CHAR</b>s describing the driver, as specified by the driver, in <a href="/windows/win32/intl/unicode">UTF-8</a> encoding.</span></span>

<span data-ttu-id="4cdfd-118">La proprietà dell'adattatore <em>DriverDescription</em> è di tipo <b>char \*</b>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-118">The <em>DriverDescription</em> adapter property has type <b>char\*</b>.</span></span>

### <a name="hardwareid"></a><span data-ttu-id="4cdfd-119">HardwareID</span><span class="sxs-lookup"><span data-stu-id="4cdfd-119">HardwareID</span></span>

<span data-ttu-id="4cdfd-120">Specifica la proprietà dell'adattatore <em>HardwareID</em> , che rappresenta le parti dell'ID hardware PNP.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-120">Specifies the <em>HardwareID</em> adapter property, which represents the PnP hardware ID parts.</span></span>

<span data-ttu-id="4cdfd-121">Il tipo della proprietà dell'adattatore <em>HardwareID</em> è <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-121">The <em>HardwareID</em> adapter property has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.</span></span>

### <a name="kmdmodelversion"></a><span data-ttu-id="4cdfd-122">KmdModelVersion</span><span class="sxs-lookup"><span data-stu-id="4cdfd-122">KmdModelVersion</span></span>

<span data-ttu-id="4cdfd-123">Specifica la proprietà dell'adapter <em>KmdModelVersion</em> , che rappresenta il modello di driver.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-123">Specifies the <em>KmdModelVersion</em> adapter property, which represents the driver model.</span></span>

<span data-ttu-id="4cdfd-124">Il tipo della proprietà dell'adapter <em>KmdModelVersion</em> è <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-124">The <em>KmdModelVersion</em> adapter property has type <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.</span></span>

### <a name="computepreemptiongranularity"></a><span data-ttu-id="4cdfd-125">ComputePreemptionGranularity</span><span class="sxs-lookup"><span data-stu-id="4cdfd-125">ComputePreemptionGranularity</span></span>

<span data-ttu-id="4cdfd-126">Specifica la proprietà dell'adattatore <em>ComputePreemptionGranularity</em> , che rappresenta la granularità di precedenza di calcolo.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-126">Specifies the <em>ComputePreemptionGranularity</em> adapter property, which represents the compute preemption granularity.</span></span>

<span data-ttu-id="4cdfd-127">La proprietà dell'adapter <em>ComputePreemptionGranularity</em> è di tipo <b>uint16_t</b>, che rappresenta un valore <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> .</span><span class="sxs-lookup"><span data-stu-id="4cdfd-127">The <em>ComputePreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="graphicspreemptiongranularity"></a><span data-ttu-id="4cdfd-128">GraphicsPreemptionGranularity</span><span class="sxs-lookup"><span data-stu-id="4cdfd-128">GraphicsPreemptionGranularity</span></span>

<span data-ttu-id="4cdfd-129">Specifica la proprietà dell'adattatore <em>GraphicsPreemptionGranularity</em> , che rappresenta la granularità di precedenza della grafica.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-129">Specifies the <em>GraphicsPreemptionGranularity</em> adapter property, which represents the graphics preemption granularity.</span></span>

<span data-ttu-id="4cdfd-130">La proprietà dell'adapter <em>GraphicsPreemptionGranularity</em> è di tipo <b>uint16_t</b>, che rappresenta un valore <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> .</span><span class="sxs-lookup"><span data-stu-id="4cdfd-130">The <em>GraphicsPreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="dedicatedadaptermemory"></a><span data-ttu-id="4cdfd-131">DedicatedAdapterMemory</span><span class="sxs-lookup"><span data-stu-id="4cdfd-131">DedicatedAdapterMemory</span></span>

<span data-ttu-id="4cdfd-132">Specifica la proprietà dell'adapter <em>DedicatedAdapterMemory</em> , che rappresenta il numero di byte della memoria dell'adapter dedicato che non sono condivisi con la CPU.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-132">Specifies the <em>DedicatedAdapterMemory</em> adapter property, which represents the number of bytes of dedicated adapter memory that are not shared with the CPU.</span></span>

<span data-ttu-id="4cdfd-133">Il tipo della proprietà dell'adapter <em>DedicatedVideoMemory</em> è <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-133">The <em>DedicatedVideoMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="dedicatedsystemmemory"></a><span data-ttu-id="4cdfd-134">DedicatedSystemMemory</span><span class="sxs-lookup"><span data-stu-id="4cdfd-134">DedicatedSystemMemory</span></span>

<span data-ttu-id="4cdfd-135">Specifica la proprietà dell'adattatore <em>DedicatedSystemMemory</em> , che rappresenta il numero di byte di memoria di sistema dedicato che non sono condivisi con la CPU.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-135">Specifies the <em>DedicatedSystemMemory</em> adapter property, which represents the number of bytes of dedicated system memory that are not shared with the CPU.</span></span> <span data-ttu-id="4cdfd-136">Questa memoria viene allocata dalla memoria di sistema disponibile al momento dell'avvio.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-136">This memory is allocated from available system memory at boot time.</span></span>

<span data-ttu-id="4cdfd-137">Il tipo della proprietà dell'adapter <em>DedicatedSystemMemory</em> è <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-137">The <em>DedicatedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="sharedsystemmemory"></a><span data-ttu-id="4cdfd-138">SharedSystemMemory</span><span class="sxs-lookup"><span data-stu-id="4cdfd-138">SharedSystemMemory</span></span>

<span data-ttu-id="4cdfd-139">Specifica la proprietà dell'adapter <em>SharedSystemMemory</em> , che rappresenta il numero di byte della memoria di sistema condivisa.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-139">Specifies the <em>SharedSystemMemory</em> adapter property, which represents the number of bytes of shared system memory.</span></span> <span data-ttu-id="4cdfd-140">Questo è il valore massimo della memoria di sistema che può essere utilizzato dall'adapter durante l'operazione.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-140">This is the maximum value of system memory that may be consumed by the adapter during operation.</span></span> <span data-ttu-id="4cdfd-141">Eventuali memorie accidentali utilizzate dal driver durante la gestione e utilizzano la memoria video sono aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-141">Any incidental memory consumed by the driver as it manages and uses video memory is additional.</span></span>

<span data-ttu-id="4cdfd-142">Il tipo della proprietà dell'adapter <em>SharedSystemMemory</em> è <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-142">The <em>SharedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="acgcompatible"></a><span data-ttu-id="4cdfd-143">AcgCompatible</span><span class="sxs-lookup"><span data-stu-id="4cdfd-143">AcgCompatible</span></span>

<span data-ttu-id="4cdfd-144">Specifica la proprietà dell'adattatore <em>AcgCompatible</em> , che indica se l'adapter è compatibile con i processi che applicano la protezione del codice arbitraria.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-144">Specifies the <em>AcgCompatible</em> adapter property, which indicates whether the adapter is compatible with processes that enforce Arbitrary Code Guard.</span></span>

<span data-ttu-id="4cdfd-145">Il tipo della proprietà dell'adapter <em>AcgCompatible</em> è <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-145">The <em>AcgCompatible</em> adapter property has type <b>bool</b>.</span></span>

### <a name="ishardware"></a><span data-ttu-id="4cdfd-146">Hardware</span><span class="sxs-lookup"><span data-stu-id="4cdfd-146">IsHardware</span></span>

<span data-ttu-id="4cdfd-147">Specifica la proprietà dell'adattatore di <em>hardware</em> , che determina se si tratta di una scheda hardware.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-147">Specifies the <em>IsHardware</em> adapter property, which determines whether or not this is a hardware adapter.</span></span> <span data-ttu-id="4cdfd-148">Un adapter che non è una scheda hardware è un adattatore software.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-148">An adapter that's not a hardware adapter is a software adapter.</span></span>

<span data-ttu-id="4cdfd-149">Il tipo della proprietà dell'adattatore di <em>hardware</em> è <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-149">The <em>IsHardware</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isintegrated"></a><span data-ttu-id="4cdfd-150">Integrato</span><span class="sxs-lookup"><span data-stu-id="4cdfd-150">IsIntegrated</span></span>

<span data-ttu-id="4cdfd-151">Specifica la proprietà dell'adapter <em>integrato</em> , che determina se l'adapter viene segnalato come processore di grafica integrato (iGPU).</span><span class="sxs-lookup"><span data-stu-id="4cdfd-151">Specifies the <em>IsIntegrated</em> adapter property, which determines whether the adapter is reported to be an integrated graphics processor (iGPU).</span></span>

<span data-ttu-id="4cdfd-152">Il tipo della proprietà dell'adapter <em>disintegrato</em> è <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-152">The <em>IsIntegrated</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isdetachable"></a><span data-ttu-id="4cdfd-153">Dissociabile</span><span class="sxs-lookup"><span data-stu-id="4cdfd-153">IsDetachable</span></span>

<span data-ttu-id="4cdfd-154">Specifica la proprietà dell'adapter <em>dissociabile</em> , che determina se l'adapter è stato segnalato come scollegabile o rimovibile.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-154">Specifies the <em>IsDetachable</em> adapter property, which determines whether the adapter has been reported to be detachable, or removable.</span></span>

<span data-ttu-id="4cdfd-155">Il tipo della proprietà dell'adapter <em>dissociabile</em> è <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-155">The <em>IsDetachable</em> adapter property has type <b>bool</b>.</span></span>

<span data-ttu-id="4cdfd-156"><b>Nota</b>.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-156"><b>Note</b>.</span></span> <span data-ttu-id="4cdfd-157">Anche se <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter:: GetProperty</a> indica `false` per questa proprietà, l'adapter ha ancora la possibilità di essere segnalato come rimosso, ad esempio in caso di malfunzionamento o di aggiornamento del driver.</span><span class="sxs-lookup"><span data-stu-id="4cdfd-157">Even if <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter::GetProperty</a> indicates `false` for this property, the adapter still has the ability to be reported as removed, such as in the case of malfunction, or driver update.</span></span>

## <a name="see-also"></a><span data-ttu-id="4cdfd-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cdfd-158">See also</span></span>

<span data-ttu-id="4cdfd-159">[IDXCoreAdapter:: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="4cdfd-159">[IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>