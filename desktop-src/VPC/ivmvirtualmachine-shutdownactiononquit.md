---
title: Proprietà IVMVirtualMachine ShutdownActionOnQuit (VPCCOMInterfaces.h)
description: Azione da eseguire su questa macchina virtuale se è in esecuzione quando Windows virtual PC viene chiuso.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- Proprietà ShutdownActionOnQuit Virtual PC
- Proprietà ShutdownActionOnQuit Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà ShutdownActionOnQuit
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c859a0f1715685e07ba13d6fb06fc99dc08f712fd20fa56a4672a2cc857b1591
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124701"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a>Proprietà IVMVirtualMachine::ShutdownActionOnQuit

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera e imposta l'azione da eseguire su questa macchina virtuale (VM) se è in esecuzione quando Windows virtual PC viene chiuso.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a>Valore proprietà

Specifica come arrestare la macchina virtuale se è in esecuzione quando Windows virtual PC viene chiuso. Per un elenco di valori, vedere [**VMShutdownAction.**](vmshutdownaction.md)

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                                       |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL** o non è un valore valido.<br/>                     |
| <dl> <dt>E \_ Accesso negato</dt> <dt>0x80070005</dt> </dl>    | L'utente corrente non ha accesso sufficiente al file di configurazione.<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl> | La configurazione è sconosciuta.<br/>                                       |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/>                                   |



## <a name="remarks"></a>Commenti

Per impostazione predefinita, le macchine virtuali in esecuzione vengono salvate quando Windows di Virtual PC viene chiuso. L'azione **di arresto vmShutdownAction \_ Save** (0) salverà lo stato della macchina virtuale. **L'azione vmShutdownAction \_ TurnOff** (1) disattiva la macchina virtuale. **L'azione vmShutdownAction \_ Shutdown** (2) arresterà il sistema operativo guest se i componenti di integrazione sono disponibili e salverà la macchina virtuale in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**VMShutdownAction**](vmshutdownaction.md)
</dt> </dl>

 

