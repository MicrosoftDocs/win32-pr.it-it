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
# <a name="dxcoreadapterproperty-enum"></a>Enumerazione DXCoreAdapterProperty

Definisce le costanti che specificano le proprietà dell'adapter DXCore. Passare una di queste costanti al metodo [IDXCoreAdapter:: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) per recuperare la dimensione del buffer necessaria per ricevere il valore della proprietà corrispondente; passare quindi la stessa costante al metodo [IDXCoreAdapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) per recuperare il valore della proprietà in un buffer allocato dall'utente.

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

Specifica la proprietà dell'adapter <em>InstanceLuid</em> , che contiene un identificatore univoco locale che rappresenta l'adapter. Questo valore rimane costante per la durata di questo adapter. Il LUID di una scheda cambia al riavvio, all'aggiornamento del driver o alla disabilitazione o all'abilitazione del dispositivo.

Il tipo della proprietà dell'adattatore <em>InstanceLuid</em> è <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.

### <a name="driverversion"></a>DriverVersion

Specifica la proprietà dell'adapter <em>DriverVersion</em> , che contiene la versione del driver, rappresentata in <b>WORD</b>s come <b>LARGE_INTEGER</b>.

La proprietà dell'adapter <em>DriverVersion</em> è di tipo <b>uint64_t</b>, che rappresenta un valore booleano.

### <a name="driverdescription"></a>DriverDescription

Specifica la proprietà dell'adattatore <em>DriverDescription</em> , che contiene una matrice con terminazione null di <b>char</b>s che descrive il driver, come specificato dal driver, nella codifica <a href="/windows/win32/intl/unicode">UTF-8</a> .

La proprietà dell'adattatore <em>DriverDescription</em> è di tipo <b>char *</b>.

### <a name="hardwareid"></a>HardwareID

Specifica la proprietà dell'adattatore <em>HardwareID</em> , che rappresenta le parti dell'ID hardware PNP.

Il tipo della proprietà dell'adattatore <em>HardwareID</em> è <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.

### <a name="kmdmodelversion"></a>KmdModelVersion

Specifica la proprietà dell'adapter <em>KmdModelVersion</em> , che rappresenta il modello di driver.

Il tipo della proprietà dell'adapter <em>KmdModelVersion</em> è <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.

### <a name="computepreemptiongranularity"></a>ComputePreemptionGranularity

Specifica la proprietà dell'adattatore <em>ComputePreemptionGranularity</em> , che rappresenta la granularità di precedenza di calcolo.

La proprietà dell'adapter <em>ComputePreemptionGranularity</em> è di tipo <b>uint16_t</b>, che rappresenta un valore <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> .

### <a name="graphicspreemptiongranularity"></a>GraphicsPreemptionGranularity

Specifica la proprietà dell'adattatore <em>GraphicsPreemptionGranularity</em> , che rappresenta la granularità di precedenza della grafica.

La proprietà dell'adapter <em>GraphicsPreemptionGranularity</em> è di tipo <b>uint16_t</b>, che rappresenta un valore <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> .

### <a name="dedicatedadaptermemory"></a>DedicatedAdapterMemory

Specifica la proprietà dell'adapter <em>DedicatedAdapterMemory</em> , che rappresenta il numero di byte della memoria dell'adapter dedicato che non sono condivisi con la CPU.

Il tipo della proprietà dell'adapter <em>DedicatedVideoMemory</em> è <b>uint64_t</b>.

### <a name="dedicatedsystemmemory"></a>DedicatedSystemMemory

Specifica la proprietà dell'adattatore <em>DedicatedSystemMemory</em> , che rappresenta il numero di byte di memoria di sistema dedicato che non sono condivisi con la CPU. Questa memoria viene allocata dalla memoria di sistema disponibile al momento dell'avvio.

Il tipo della proprietà dell'adapter <em>DedicatedSystemMemory</em> è <b>uint64_t</b>.

### <a name="sharedsystemmemory"></a>SharedSystemMemory

Specifica la proprietà dell'adapter <em>SharedSystemMemory</em> , che rappresenta il numero di byte della memoria di sistema condivisa. Questo è il valore massimo della memoria di sistema che può essere utilizzato dall'adapter durante l'operazione. Eventuali memorie accidentali utilizzate dal driver durante la gestione e utilizzano la memoria video sono aggiuntive.

Il tipo della proprietà dell'adapter <em>SharedSystemMemory</em> è <b>uint64_t</b>.

### <a name="acgcompatible"></a>AcgCompatible

Specifica la proprietà dell'adattatore <em>AcgCompatible</em> , che indica se l'adapter è compatibile con i processi che applicano la protezione del codice arbitraria.

Il tipo della proprietà dell'adapter <em>AcgCompatible</em> è <b>bool</b>.

### <a name="ishardware"></a>Hardware

Specifica la proprietà dell'adattatore di <em>hardware</em> , che determina se si tratta di una scheda hardware. Un adapter che non è una scheda hardware è un adattatore software.

Il tipo della proprietà dell'adattatore di <em>hardware</em> è <b>bool</b>.

### <a name="isintegrated"></a>Integrato

Specifica la proprietà dell'adapter <em>integrato</em> , che determina se l'adapter viene segnalato come processore di grafica integrato (iGPU).

Il tipo della proprietà dell'adapter <em>disintegrato</em> è <b>bool</b>.

### <a name="isdetachable"></a>Dissociabile

Specifica la proprietà dell'adapter <em>dissociabile</em> , che determina se l'adapter è stato segnalato come scollegabile o rimovibile.

Il tipo della proprietà dell'adapter <em>dissociabile</em> è <b>bool</b>.

<b>Nota</b>. Anche se <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter:: GetProperty</a> indica `false` per questa proprietà, l'adapter ha ancora la possibilità di essere segnalato come rimosso, ad esempio in caso di malfunzionamento o di aggiornamento del driver.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter:: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)