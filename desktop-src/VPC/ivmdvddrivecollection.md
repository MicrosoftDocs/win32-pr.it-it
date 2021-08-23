---
title: Interfaccia IVMDVDDriveCollection (VPCCOMInterfaces.h)
description: Definisce la raccolta di unità CD e DVD all'interno della macchina virtuale. Per ottenere un oggetto IVMDVDDriveCollection, usare la proprietà IVMVirtualMachine DVDROMDrives.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- Interfaccia IVMDVDDriveCollection Virtual PC
- Interfaccia IVMDVDDriveCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77225134a88ff2c66be3f53f5d3d44c9f8353d8f44077fb0862f0c943c5aec3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056859"
---
# <a name="ivmdvddrivecollection-interface"></a>Interfaccia IVMDVDDriveCollection

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce la raccolta di unità CD e DVD all'interno della macchina virtuale. Per ottenere un **oggetto IVMDVDDriveCollection,** usare la proprietà [**IVMVirtualMachine::D VDROMDrives.**](ivmvirtualmachine-dvdromdrives.md)

## <a name="members"></a>Membri

**L'interfaccia IVMDVDDriveCollection** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMDVDDriveCollection** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia IVMDVDDriveCollection** ha queste proprietà.



| Proprietà                                                       | Tipo di accesso          | Descrizione                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmdvddrivecollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                                   |
| [**Conteggio**](ivmdvddrivecollection-count.md)<br/>        | Sola lettura<br/> | Numero di unità CD e DVD in questa raccolta.<br/>                 |
| [**Elemento**](ivmdvddrivecollection-item.md)<br/>          | Sola lettura<br/> | Oggetto unità CD o DVD che corrisponde all'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDriveCollection è definito come bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> <dt>

[**IVMVirtualMachine::D VDROMDrives**](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

