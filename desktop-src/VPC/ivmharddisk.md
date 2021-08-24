---
title: Interfaccia IVMHardDisk (VPCCOMInterfaces.h)
description: Fornisce l'accesso a un'immagine del disco rigido. È possibile accedervi tramite la proprietà HardDisk IVMHardDiskConnection o il metodo IVMVirtualPC GetHardDisk.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- Interfaccia IVMHardDisk Virtual PC
- Interfaccia IVMHardDisk Virtual PC , descritto
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525762f66798b95562958fb204119beda1d76a8b94a60a11a7171b0d0b2951e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768161"
---
# <a name="ivmharddisk-interface"></a>Interfaccia IVMHardDisk

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Fornisce l'accesso a un'immagine del disco rigido. È possibile accedervi tramite la [**proprietà IVMHardDiskConnection::HardDisk**](ivmharddiskconnection-harddisk.md) o [**il metodo IVMVirtualPC::GetHardDisk.**](ivmvirtualpc-getharddisk.md)

## <a name="members"></a>Membri

**L'interfaccia IVMHardDisk** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMHardDisk** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IVMHardDisk** include questi metodi.



| Metodo                                 | Descrizione                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Compact**](ivmharddisk-compact.md) | Compatta un'immagine del disco rigido virtuale a espansione dinamica.<br/>                                                                                        |
| [**Converti**](ivmharddisk-convert.md) | Converte qualsiasi disco rigido virtuale in un disco rigido virtuale a espansione dinamica o in un disco rigido virtuale di dimensioni fisse.<br/>                            |
| [**Unione**](ivmharddisk-merge.md)     | Unisce un disco rigido virtuale differenze con l'immagine del disco padre.<br/>                                                                              |
| [**MergeTo**](ivmharddisk-mergeto.md) | Unisce un disco rigido virtuale differenze con tutti i relativi elementi padre (fino al disco rigido virtuale padre radice incluso) in un nuovo file del disco rigido.<br/> |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IVMHardDisk.**



| Proprietà                                                              | Tipo di accesso           | Descrizione                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**File**](ivmharddisk-file.md)<br/>                           | Sola lettura<br/>  | Nome completo del percorso del file del disco rigido virtuale.<br/>                                   |
| [**HostFreeDiskSpace**](ivmharddisk-hostfreediskspace.md)<br/> | Sola lettura<br/>  | Quantità di spazio su disco rimanente disponibile nell'host per il disco rigido virtuale.<br/> |
| [**Padre**](ivmharddisk-parent.md)<br/>                       | Lettura/Scrittura<br/> | Elemento padre del disco rigido virtuale differenze.<br/>                                   |
| [**SizeInGuest**](ivmharddisk-sizeinguest.md)<br/>             | Sola lettura<br/>  | Dimensioni del disco rigido virtuale nel sistema operativo guest.<br/>                    |
| [**SizeOnHost**](ivmharddisk-sizeonhost.md)<br/>               | Sola lettura<br/>  | Dimensioni del file del disco rigido virtuale nel computer host.<br/>                        |
| [**Tipo**](ivmharddisk-type.md)<br/>                           | Sola lettura<br/>  | Tipo di disco rigido virtuale.<br/>                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



 

