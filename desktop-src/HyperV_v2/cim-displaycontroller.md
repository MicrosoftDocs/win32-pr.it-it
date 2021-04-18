---
description: Rappresenta un controller di visualizzazione.
ms.assetid: 14598ae6-58e2-46ca-8653-b57e5833a224
title: Classe CIM_DisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DisplayController
- CIM_DisplayController.Description
- CIM_DisplayController.VideoProcessor
- CIM_DisplayController.VideoMemoryType
- CIM_DisplayController.OtherVideoMemoryType
- CIM_DisplayController.NumberOfVideoPages
- CIM_DisplayController.MaxMemorySupported
- CIM_DisplayController.AcceleratorCapabilities
- CIM_DisplayController.CapabilityDescriptions
- CIM_DisplayController.OtherVideoArchitecture
- CIM_DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59db37a89ce1f57e01a6a9a27fb9c24177221b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308352"
---
# <a name="cim_displaycontroller-class"></a>CIM \_ DisplayController (classe)

Rappresenta un controller di visualizzazione.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_DisplayController : CIM_Controller
{
  string Description;
  string VideoProcessor;
  uint16 VideoMemoryType;
  string OtherVideoMemoryType;
  uint32 NumberOfVideoPages;
  uint32 MaxMemorySupported;
  uint16 AcceleratorCapabilities[];
  string CapabilityDescriptions[];
  string OtherVideoArchitecture;
  uint16 VideoArchitecture;
};
```

## <a name="members"></a>Members

La classe **CIM \_ DisplayController** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ DisplayController** dispone di queste proprietà.

<dl> <dt>

**AcceleratorCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**CapabilityDescriptions**")
</dt> </dl>

Funzionalità grafiche e 3D del controller di visualizzazione.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

**Acceleratore grafico** (2)


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

**acceleratore 3D** (3)


</dt> <dd></dd> <dt>

<span id="PCI_Fast_Write"></span><span id="pci_fast_write"></span><span id="PCI_FAST_WRITE"></span>

**Scrittura veloce PCI** (4)


</dt> <dd></dd> <dt>

<span id="MultiMonitor_Support"></span><span id="multimonitor_support"></span><span id="MULTIMONITOR_SUPPORT"></span>

**Supporto di multimonitor** (5)


</dt> <dd></dd> <dt>

<span id="PCI_Mastering"></span><span id="pci_mastering"></span><span id="PCI_MASTERING"></span>

**Master PCI** (6)


</dt> <dd></dd> <dt>

<span id="Second_Monochrome_Adapter_Support"></span><span id="second_monochrome_adapter_support"></span><span id="SECOND_MONOCHROME_ADAPTER_SUPPORT"></span>

**Supporto per la seconda scheda monocromatica** (7)


</dt> <dd></dd> <dt>

<span id="Large_Memory_Address_Support"></span><span id="large_memory_address_support"></span><span id="LARGE_MEMORY_ADDRESS_SUPPORT"></span>

**Supporto per indirizzi di memoria di grandi dimensioni** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**AcceleratorCapabilities**")
</dt> </dl>

Spiegazione dettagliata delle funzionalità dell'acceleratore video della matrice **AcceleratorCapabilities** . Gli elementi in questa matrice corrispondono agli elementi della matrice in **AcceleratorCapabilities**.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 004,18 ")
</dt> </dl>

Descrizione testuale dell'oggetto.

</dd> <dt>

**MaxMemorySupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")
</dt> </dl>

Quantità massima di memoria, in byte, supportata.

</dd> <dt>

**NumberOfVideoPages**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero di pagine video supportate in base alle risoluzioni correnti e alla memoria disponibile.

</dd> <dt>

**OtherVideoArchitecture**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**VideoArchitecture**")
</dt> </dl>

Descrizione del tipo di architettura video quando la proprietà **VideoArchitecture** contiene "1" (other).

</dd> <dt>

**OtherVideoMemoryType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**VideoMemoryType**")
</dt> </dl>

Tipo di memoria video quando la proprietà **VideoMemoryType** è "1" (other).

</dd> <dt>

**VideoArchitecture**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

L'architettura video dei controller di visualizzazione usata per generare il segnale video. In genere, un processore video dedicato genera il segnale video in conformità con l'architettura specificata. L'architettura indica la capacità massima di risoluzione del controller di visualizzazione.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

**CGA** (2)


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

**EGA** (3)


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

**VGA** (4)


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

**SVGA** (5)


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

**MDA** (6)


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

**HGC** (7)


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

**MCGA** (8)


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

**8514a** (9)


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

**XGA** (10)


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

**Buffer frame lineare** (11)


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

**PC-98** (160)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (0x8000..)


</dt> <dd></dd> </dl>

</dd> <dt>

**VideoMemoryType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,6 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**OtherVideoMemoryType**")
</dt> </dl>

Tipo di memoria video.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

**VRAM** (2)


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

**DRAM** (3)


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

**SRAM** (4)


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

**WRAM** (5)


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

**RAM EDO** (6)


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

**DRAM sincrona a impulsi** (7)


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

**SRAM** (8)


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

**CDRAM** (9)


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

**3DRAM** (10)


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

**SDRAM** (11)


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

**SGRAM** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**VideoProcessor**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale del processore/controller video.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Controller CIM**](cim-controller.md)
</dt> </dl>

 

