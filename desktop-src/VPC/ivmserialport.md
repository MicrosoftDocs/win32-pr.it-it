---
title: Interfaccia IVMSerialPort (VPCCOMInterfaces.h)
description: Definisce una porta seriale all'interno di una macchina virtuale.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- Interfaccia IVMSerialPort Virtual PC
- Interfaccia IVMSerialPort Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385f22caf7b843a91987eea01a7713544475c24be741bbb56d59610cb2cd521d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752827"
---
# <a name="ivmserialport-interface"></a>Interfaccia IVMSerialPort

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce una porta seriale all'interno di una macchina virtuale. Questa interfaccia consente di configurare le porte seriali all'interno di una macchina virtuale. È possibile recuperare un **oggetto IVMSerialPort** dall'oggetto [**IVMSerialPortCollection**](ivmserialportcollection.md) restituito dalla [**proprietà IVMVirtualMachine::SerialPorts.**](ivmvirtualmachine-serialports.md)

## <a name="members"></a>Membri

**L'interfaccia IVMSerialPort** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMSerialPort** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IVMSerialPort** include questi metodi.



| Metodo                                       | Descrizione                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [**\_ID**](ivmserialport--id.md)            | Recupera l'identificatore interno della porta seriale.<br/> |
| [**Configurare**](ivmserialport-configure.md) | Configura la porta seriale.<br/>                           |



 

### <a name="properties"></a>Proprietà

Queste **proprietà sono disponibili nell'interfaccia IVMSerialPort.**



| Proprietà                                                                  | Tipo di accesso          | Descrizione                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [**ConnectImmediately**](ivmserialport-connectimmediately.md)<br/> | Sola lettura<br/> | Indica se la porta seriale deve essere aperta senza attendere la ricezione di un comando modem.<br/> |
| [**Nome**](ivmserialport-name.md)<br/>                             | Sola lettura<br/> | Nome della porta seriale.<br/>                                                                           |
| [**Tipo**](ivmserialport-type.md)<br/>                             | Sola lettura<br/> | Tipo della porta seriale.<br/>                                                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort è definito come 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



 

