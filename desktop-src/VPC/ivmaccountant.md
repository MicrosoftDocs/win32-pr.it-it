---
title: Interfaccia IVMAccountant (VPCCOMInterfaces. h)
description: Consente di accedere alle informazioni relative all'accounting per una macchina virtuale.
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- Interfaccia IVMAccountant Virtual PC
- Interfaccia IVMAccountant Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d207833b92794510789e66e31b10e94d70b319fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743474"
---
# <a name="ivmaccountant-interface"></a>Interfaccia IVMAccountant

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Consente di accedere alle informazioni relative all'accounting per una macchina virtuale. Per recuperare **IVMAccountant** per una macchina virtuale, usare la proprietà [**IVMVirtualMachine:: Accountant**](ivmvirtualmachine-accountant.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMAccountant** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMAccountant** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IVMAccountant** ha queste proprietà.



| Proprietà                                                                        | Tipo di accesso          | Descrizione                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [**CPUUtilization**](ivmaccountant-cpuutilization.md)<br/>               | Sola lettura<br/> | Percentuale di utilizzo della CPU corrente per questa macchina virtuale.<br/>                          |
| [**CPUUtilizationHistory**](ivmaccountant-cpuutilizationhistory.md)<br/> | Sola lettura<br/> | L'utilizzo della CPU recente della macchina virtuale, come una matrice di valori percentuali.<br/>       |
| [**DiskBytesRead**](ivmaccountant-diskbytesread.md)<br/>                 | Sola lettura<br/> | Il numero totale di byte letti da tutti i controller di archiviazione per questa macchina virtuale.<br/>          |
| [**DiskBytesWritten**](ivmaccountant-diskbyteswritten.md)<br/>           | Sola lettura<br/> | Il numero totale di byte scritti da tutti i controller di archiviazione per questa macchina virtuale.<br/>       |
| [**NetworkBytesReceived**](ivmaccountant-networkbytesreceived.md)<br/>   | Sola lettura<br/> | Il numero totale di byte ricevuti da tutte le schede di rete virtuali per questa macchina virtuale.<br/> |
| [**NetworkBytesSent**](ivmaccountant-networkbytessent.md)<br/>           | Sola lettura<br/> | Numero totale di byte inviati da tutte le schede di rete virtuali per questa macchina virtuale.<br/>     |
| [**Tempo**](ivmaccountant-uptime.md)<br/>                               | Sola lettura<br/> | Numero di secondi di esecuzione della macchina virtuale.<br/>                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant è definito come 6376c067-7f57-4D63-b754-06e2e4f51d73<br/>              |



 

