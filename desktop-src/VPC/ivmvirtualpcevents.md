---
title: Interfaccia IVMVirtualPCEvents (VPCCOMInterfaces. h)
description: Definisce l'interfaccia evento in uscita per l'interfaccia IVMVirtualPC.
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- Interfaccia IVMVirtualPCEvents Virtual PC
- Interfaccia IVMVirtualPCEvents Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a6fd22f75027d1424b8605e8e36e373064069
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048605"
---
# <a name="ivmvirtualpcevents-interface"></a>Interfaccia IVMVirtualPCEvents

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce l'interfaccia evento in uscita per l'interfaccia [**IVMVirtualPC**](ivmvirtualpc.md) . Il client implementa questi metodi per ricevere gli eventi inviati da [**IVMVirtualPC**](ivmvirtualpc.md).

## <a name="members"></a>Membri

L'interfaccia **IVMVirtualPCEvents** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualPCEvents** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IVMVirtualPCEvents** dispone di questi metodi.



| Metodo                                                        | Descrizione                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnEventLogged**](ivmvirtualpcevents-oneventlogged.md)     | Riceve la notifica che Windows Virtual PC registra un evento.<br/>      |
| [**OnVMStateChange**](ivmvirtualpcevents-onvmstatechange.md) | Riceve una notifica che lo stato di una macchina virtuale è stato modificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents è definito come efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



 

