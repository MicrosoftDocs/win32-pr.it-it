---
title: Interfaccia IVMHardDiskConnection (VPCCOMInterfaces. h)
description: Definisce la connessione per un disco rigido all'interno della macchina virtuale.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- Interfaccia IVMHardDiskConnection Virtual PC
- Interfaccia IVMHardDiskConnection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e53a092bdca26eee0c46db1d75f7fc040d5ce7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301848"
---
# <a name="ivmharddiskconnection-interface"></a>Interfaccia IVMHardDiskConnection

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce la connessione per un disco rigido all'interno della macchina virtuale. Viene restituito un oggetto **IVMHardDiskConnection** dal metodo [**IVMVirtualMachine:: AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) . È anche possibile recuperare un oggetto **IVMHardDiskConnection** dall'oggetto [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) restituito dalla proprietà [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMHardDiskConnection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDiskConnection** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IVMHardDiskConnection** dispone di questi metodi.



| Metodo                                                         | Descrizione                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [**SetBusLocation**](ivmharddiskconnection-setbuslocation.md) | Imposta la posizione del bus a cui è collegato il disco rigido.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IVMHardDiskConnection** ha queste proprietà.



| Proprietà                                                              | Tipo di accesso          | Descrizione                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [**BusNumber**](ivmharddiskconnection-busnumber.md)<br/>       | Sola lettura<br/> | Numero del bus a cui è collegata l'immagine dell'unità.<br/>                   |
| [**DeviceNumber**](ivmharddiskconnection-devicenumber.md)<br/> | Sola lettura<br/> | Numero del dispositivo a cui è collegata l'immagine dell'unità.<br/>                |
| [**HardDisk**](ivmharddiskconnection-harddisk.md)<br/>         | Sola lettura<br/> | Oggetto disco rigido corrispondente a questa connessione.<br/>                   |
| [**UndoHardDisk**](ivmharddiskconnection-undoharddisk.md)<br/> | Sola lettura<br/> | Oggetto disco rigido corrispondente all'immagine del disco di annullamento della connessione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection è definito come aefa36a5-463A-46AE-9E6C-a1fb4e12e671<br/>      |



 

