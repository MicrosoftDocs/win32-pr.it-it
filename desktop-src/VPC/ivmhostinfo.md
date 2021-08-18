---
title: Interfaccia IVMHostInfo (VPCCOMInterfaces.h)
description: Recupera informazioni sul computer host. Un oggetto IVMHostInfo viene restituito dalla proprietà IVMVirtualPC HostInfo.
ms.assetid: f30fa377-2067-4e03-bc6e-2ada62fc56b4
keywords:
- Interfaccia IVMHostInfo Virtual PC
- Interfaccia IVMHostInfo Virtual PC , descritto
topic_type:
- apiref
api_name:
- IVMHostInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da45459379c468839b0bf48ae134db1885ea25acce5ac3befa289ae15ee6fe8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974261"
---
# <a name="ivmhostinfo-interface"></a>Interfaccia IVMHostInfo

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera informazioni sul computer host. Un **oggetto IVMHostInfo** viene restituito dalla [**proprietà IVMVirtualPC::HostInfo.**](ivmvirtualpc-hostinfo.md)

## <a name="members"></a>Membri

**L'interfaccia IVMHostInfo** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMHostInfo** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia IVMHostInfo** ha queste proprietà.



| Proprietà                                                                                  | Tipo di accesso          | Descrizione                                                                                        |
|:------------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**DVDDrives**](ivmhostinfo-dvddrives.md)<br/>                                     | Sola lettura<br/> | Lettere di unità associate ai dispositivi CD e DVD host.<br/>                              |
| [**FloppyDrives**](ivmhostinfo-floppydrives.md)<br/>                               | Sola lettura<br/> | Lettere di unità associate alle unità floppy host.<br/>                                   |
| [**LogicalProcessorCount**](ivmhostinfo-logicalprocessorcount.md)<br/>             | Sola lettura<br/> | Numero di processori logici nel computer host.<br/>                                   |
| [**Memoria**](ivmhostinfo-memory.md)<br/>                                           | Sola lettura<br/> | Quantità totale di memoria fisica nel computer host, in megabyte.<br/>                  |
| [**MemoryAvail**](ivmhostinfo-memoryavail.md)<br/>                                 | Sola lettura<br/> | Quantità di memoria fisica disponibile nel computer host, in megabyte.<br/>              |
| [**MemoryAvailString**](ivmhostinfo-memoryavailstring.md)<br/>                     | Sola lettura<br/> | Quantità di memoria fisica disponibile nel computer host, in megabyte, come stringa.<br/> |
| [**MemoryTotalString**](ivmhostinfo-memorytotalstring.md)<br/>                     | Sola lettura<br/> | Quantità totale di memoria fisica nel computer host, in megabyte, come stringa.<br/>     |
| [**Mmx**](ivmhostinfo-mmx.md)<br/>                                                 | Sola lettura<br/> | Indica se il processore supporta il set di istruzioni MMX.<br/>                       |
| [**Oggetti NetworkAdapter**](ivmhostinfo-networkadapters.md)<br/>                         | Sola lettura<br/> | Raccolta enumerabile di schede di interfaccia di rete nel computer host.<br/>                                   |
| [**NetworkAddresses**](ivmhostinfo-networkaddresses.md)<br/>                       | Sola lettura<br/> | Raccolta enumerabile di indirizzi TCP/IP nel computer host.<br/>                       |
| [**OperatingSystem**](ivmhostinfo-operatingsystem.md)<br/>                         | Sola lettura<br/> | Sistema operativo in esecuzione nel computer host.<br/>                                       |
| [**OSMajorVersion**](ivmhostinfo-osmajorversion.md)<br/>                           | Sola lettura<br/> | Versione principale del sistema operativo in esecuzione nel computer host.<br/>                  |
| [**OSMinorVersion**](ivmhostinfo-osminorversion.md)<br/>                           | Sola lettura<br/> | Versione secondaria del sistema operativo in esecuzione nel computer host.<br/>                  |
| [**OSServicePackString**](ivmhostinfo-osservicepackstring.md)<br/>                 | Sola lettura<br/> | Informazioni del Service Pack del sistema operativo in esecuzione nel computer host.<br/>       |
| [**OSVersionString**](ivmhostinfo-osversionstring.md)<br/>                         | Sola lettura<br/> | Versione del sistema operativo in esecuzione nel computer host.<br/>                               |
| [**ParallelPort**](ivmhostinfo-parallelport.md)<br/>                               | Sola lettura<br/> | Porta parallela host che può essere collegata al guest.<br/>                               |
| [**PhysicalProcessorCount**](ivmhostinfo-physicalprocessorcount.md)<br/>           | Sola lettura<br/> | Numero di processori fisici nel computer host.<br/>                                  |
| [**ProcessorFeaturesString**](ivmhostinfo-processorfeaturesstring.md)<br/>         | Sola lettura<br/> | Elenco di funzionalità supportate dal processore host.<br/>                                   |
| [**ProcessorManufacturerString**](ivmhostinfo-processormanufacturerstring.md)<br/> | Sola lettura<br/> | Produttore del processore host.<br/>                                                 |
| [**ProcessorSpeed**](ivmhostinfo-processorspeed.md)<br/>                           | Sola lettura<br/> | Velocità del processore host, in megahertz (MHz) o gigahertz (GHz).<br/>                 |
| [**ProcessorSpeedString**](ivmhostinfo-processorspeedstring.md)<br/>               | Sola lettura<br/> | Velocità del processore host, in megahertz o gigahertz, come stringa.<br/>                |
| [**ProcessorVersionString**](ivmhostinfo-processorversionstring.md)<br/>           | Sola lettura<br/> | Versione del processore host.<br/>                                                      |
| [**SerialPorts**](ivmhostinfo-serialports.md)<br/>                                 | Sola lettura<br/> | Nomi delle porte seriali associati alle porte seriali dell'host.<br/>                                |
| [**Sse**](ivmhostinfo-sse.md)<br/>                                                 | Sola lettura<br/> | Indica se il processore supporta il set di istruzioni SSE.<br/>                       |
| [**SSE2**](ivmhostinfo-sse2.md)<br/>                                               | Sola lettura<br/> | Indica se il processore supporta il set di istruzioni SSE2.<br/>                      |
| [**ThreeDNow**](ivmhostinfo-threednow.md)<br/>                                     | Sola lettura<br/> | Indica se il processore supporta il set di istruzioni 3DNow.<br/>                     |
| [**UTCTime**](ivmhostinfo-utctime.md)<br/>                                         | Sola lettura<br/> | Ora UTC nel computer host.<br/>                                                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



 

