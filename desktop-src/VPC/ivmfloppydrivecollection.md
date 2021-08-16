---
title: Interfaccia IVMFloppyDriveCollection (VPCCOMInterfaces.h)
description: Definisce una raccolta di unità floppy all'interno della macchina virtuale.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- Interfaccia IVMFloppyDriveCollection Virtual PC
- Interfaccia IVMFloppyDriveCollection Virtual PC , descritto
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6637c0c4a8c8b87f4458081b0893b0939c8eaf04c97738c02d39da5e0fd8eebb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653591"
---
# <a name="ivmfloppydrivecollection-interface"></a>Interfaccia IVMFloppyDriveCollection

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce una raccolta di unità floppy all'interno della macchina virtuale. Per ottenere un **oggetto IVMFloppyDriveCollection,** usare la [**proprietà IVMVirtualMachine::FloppyDrives.**](ivmvirtualmachine-floppydrives.md)

## <a name="members"></a>Membri

**L'interfaccia IVMFloppyDriveCollection** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMFloppyDriveCollection** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia IVMFloppyDriveCollection** ha queste proprietà.



| Proprietà                                                          | Tipo di accesso          | Descrizione                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmfloppydrivecollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                                |
| [**Conteggio**](ivmfloppydrivecollection-count.md)<br/>        | Sola lettura<br/> | Numero di unità floppy in questa raccolta.<br/>                  |
| [**Elemento**](ivmfloppydrivecollection-item.md)<br/>          | Sola lettura<br/> | Oggetto unità floppy che corrisponde all'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDriveCollection è definito come 8ba70a25-f698-4ee5-85ce-3cc93a925516<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> <dt>

[**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

