---
title: Interfaccia IVMHardDisk (VPCCOMInterfaces. h)
description: Consente di accedere a un'immagine del disco rigido. È possibile accedervi tramite la proprietà IVMHardDiskConnection HardDisk o il metodo IVMVirtualPC getharddisk.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- Interfaccia IVMHardDisk Virtual PC
- Interfaccia IVMHardDisk Virtual PC, descritta
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
ms.openlocfilehash: 24d6df46e7c698676e3873dd17a854fd0b7d7933
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475040"
---
# <a name="ivmharddisk-interface"></a>Interfaccia IVMHardDisk

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Consente di accedere a un'immagine del disco rigido. È possibile accedervi tramite la proprietà [**IVMHardDiskConnection:: harddisk**](ivmharddiskconnection-harddisk.md) o il metodo [**IVMVirtualPC:: getharddisk**](ivmvirtualpc-getharddisk.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMHardDisk** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDisk** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IVMHardDisk** dispone di questi metodi.



| Metodo                                 | Descrizione                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Compact**](ivmharddisk-compact.md) | Compatta un'immagine del disco rigido virtuale ad espansione dinamica.<br/>                                                                                        |
| [**Convertire**](ivmharddisk-convert.md) | Converte qualsiasi disco rigido virtuale in un disco rigido virtuale a espansione dinamica o a dimensione fissa.<br/>                            |
| [**Unione**](ivmharddisk-merge.md)     | Unisce un disco rigido virtuale differenze con l'immagine del disco padre.<br/>                                                                              |
| [**MergeTo**](ivmharddisk-mergeto.md) | Unisce un disco rigido virtuale differenze con tutti i relativi elementi padre (fino al disco rigido virtuale padre radice) in un nuovo file di disco rigido.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IVMHardDisk** ha queste proprietà.



| Proprietà                                                              | Tipo di accesso           | Descrizione                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**File**](ivmharddisk-file.md)<br/>                           | Sola lettura<br/>  | Nome del percorso completo del file del disco rigido virtuale.<br/>                                   |
| [**HostFreeDiskSpace**](ivmharddisk-hostfreediskspace.md)<br/> | Sola lettura<br/>  | Quantità di spazio su disco rimanente disponibile nell'host per il disco rigido virtuale.<br/> |
| [**Padre**](ivmharddisk-parent.md)<br/>                       | Lettura/Scrittura<br/> | Elemento padre del disco rigido virtuale differenze.<br/>                                   |
| [**SizeInGuest**](ivmharddisk-sizeinguest.md)<br/>             | Sola lettura<br/>  | Dimensioni del disco rigido virtuale nel sistema operativo guest.<br/>                    |
| [**SizeOnHost**](ivmharddisk-sizeonhost.md)<br/>               | Sola lettura<br/>  | Dimensioni del file del disco rigido virtuale nel computer host.<br/>                        |
| [**Tipo**](ivmharddisk-type.md)<br/>                           | Sola lettura<br/>  | Tipo del disco rigido virtuale.<br/>                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0<br/>                |



 

