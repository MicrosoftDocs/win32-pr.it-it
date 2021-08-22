---
title: DXCoreAdapterProperty
description: Definisce le costanti che specificano le proprietà dell'adattatore DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: aca9093eb85971621cf232b4713d811535619b59c3d07e0b8b490d063b9d7ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042929"
---
# <a name="dxcoreadapterproperty-enum"></a>Enumerazione DXCoreAdapterProperty

Definisce le costanti che specificano le proprietà dell'adattatore DXCore. Passare una di queste costanti al metodo [IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) per recuperare le dimensioni del buffer necessarie per ricevere il valore della proprietà corrispondente. passare quindi la stessa costante al [metodo IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) per recuperare il valore della proprietà in un buffer allocato.

## <a name="syntax"></a>Sintassi

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

## <a name="constants"></a>Costanti

### <a name="instanceluid"></a>InstanceLuid

Specifica la proprietà <em>dell'adapter InstanceLuid,</em> che contiene un identificatore univoco locale che rappresenta l'adattatore. Questo valore rimane costante per la durata di questo adattatore. Il LUID di una scheda cambia al riavvio, all'aggiornamento del driver o alla disabilitazione/abilitazione del dispositivo.

La <em>proprietà dell'adapter InstanceLuid</em> è di <a href="/windows/win32/api/winnt/ns-winnt-luid">tipo LUID.</a>

### <a name="driverversion"></a>DriverVersion

Specifica la proprietà <em>dell'adattatore DriverVersion,</em> che contiene la versione del driver, rappresentata in <b>WORD</b>come <b>LARGE_INTEGER</b>.

La <em>proprietà dell'adattatore DriverVersion</em> <b>ha uint64_t</b>, che rappresenta un valore booleano.

### <a name="driverdescription"></a>DriverDescription

Specifica la <em>proprietà dell'adattatore DriverDescription,</em> che contiene una matrice con terminazione NULL di <b>CHAR</b>che descrive il driver, come specificato dal driver, nella <a href="/windows/win32/intl/unicode">codifica UTF-8.</a>

La <em>proprietà dell'adapter DriverDescription</em> è di <b>tipo char*.</b>

### <a name="hardwareid"></a>HardwareID

Specifica la proprietà <em>dell'adattatore HardwareID,</em> che rappresenta le parti dell'ID hardware PnP.

La proprietà della scheda <em>HardwareID</em> è di <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">tipo DXCoreHardwareID</a>.

### <a name="kmdmodelversion"></a>KmdModelVersion

Specifica la proprietà <em>dell'adattatore KmdModelVersion,</em> che rappresenta il modello di driver.

La <em>proprietà dell'adapter KmdModelVersion</em> è di <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.

### <a name="computepreemptiongranularity"></a>ComputePreemptionGranularity

Specifica la proprietà <em>dell'adattatore ComputePreemptionGranularity,</em> che rappresenta la granularità della preemption di calcolo.

La <em>proprietà dell'adattatore ComputePreemptionGranularity</em> ha uint16_t <b>,</b>che rappresenta un <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> predefinito.

### <a name="graphicspreemptiongranularity"></a>GraphicsPreemptionGranularity

Specifica la <em>proprietà dell'adattatore GraphicsPreemptionGranularity,</em> che rappresenta la granularità della preemption grafica.

La <em>proprietà dell'adattatore GraphicsPreemptionGranularity</em> ha uint16_t <b>,</b>che rappresenta <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> valore.

### <a name="dedicatedadaptermemory"></a>DedicatedAdapterMemory

Specifica la proprietà <em>dell'adapter DedicatedAdapterMemory,</em> che rappresenta il numero di byte di memoria della scheda dedicata non condivisi con la CPU.

La <em>proprietà dell'adapter DedicatedVideoMemory</em> è <b>di uint64_t</b>.

### <a name="dedicatedsystemmemory"></a>DedicatedSystemMemory

Specifica la proprietà <em>dell'adapter DedicatedSystemMemory,</em> che rappresenta il numero di byte di memoria di sistema dedicata non condivisi con la CPU. Questa memoria viene allocata dalla memoria di sistema disponibile in fase di avvio.

La <em>proprietà dell'adapter DedicatedSystemMemory</em> è di <b>uint64_t</b>.

### <a name="sharedsystemmemory"></a>SharedSystemMemory

Specifica la proprietà <em>dell'adapter SharedSystemMemory,</em> che rappresenta il numero di byte di memoria di sistema condivisa. Si tratta del valore massimo della memoria di sistema che può essere utilizzato dall'adattatore durante l'operazione. Qualsiasi memoria incidentale utilizzata dal driver durante la gestione e l'uso della memoria video è aggiuntiva.

La <em>proprietà dell'adapter SharedSystemMemory</em> è di <b>uint64_t</b>.

### <a name="acgcompatible"></a>AcgCompatible

Specifica la <em>proprietà dell'adapter AcgCompatible,</em> che indica se l'adapter è compatibile con i processi che applicano Arbitrary Code Guard.

La <em>proprietà dell'adapter AcgCompatible</em> è di <b>tipo bool</b>.

### <a name="ishardware"></a>IsHardware

Specifica la proprietà <em>dell'adattatore IsHardware,</em> che determina se si tratta o meno di una scheda hardware. Una scheda che non è una scheda hardware è una scheda software.

La <em>proprietà dell'adapter IsHardware</em> è di <b>tipo bool</b>.

### <a name="isintegrated"></a>IsIntegrated

Specifica la proprietà <em>isIntegrated</em> dell'adapter, che determina se l'adattatore viene segnalato come processore di grafica integrato (iGPU).

La <em>proprietà dell'adapter IsIntegrated</em> è di <b>tipo bool</b>.

### <a name="isdetachable"></a>IsDetachable

Specifica la proprietà <em>dell'adattatore IsDetachable,</em> che determina se l'adattatore è stato segnalato come rimovibile o rimovibile.

La <em>proprietà dell'adattatore IsDetachable</em> è di <b>tipo bool</b>.

<b>Si noti</b>. Anche se <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter::GetProperty</a> indica per questa proprietà, l'adapter può comunque essere segnalato come rimosso, ad esempio in caso di malfunzionamento o aggiornamento `false` del driver.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)