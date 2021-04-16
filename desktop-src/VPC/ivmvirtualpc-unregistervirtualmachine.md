---
title: Metodo IVMVirtualPC UnregisterVirtualMachine (VPCCOMInterfaces. h)
description: Annulla la registrazione di una configurazione di macchina virtuale senza eliminare il file di configurazione.
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- Metodo UnregisterVirtualMachine Virtual PC
- Metodo UnregisterVirtualMachine Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo UnregisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnregisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d74380a822253918791b78bc34ac1c796f595ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478994"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a>Metodo IVMVirtualPC:: UnregisterVirtualMachine

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Annulla la registrazione di una configurazione di macchina virtuale (VM) senza eliminare il file di configurazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*virtualmachine* \[ in\]
</dt> <dd>

Puntatore a un oggetto [**IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta la configurazione della macchina virtuale di cui annullare la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                        | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                | Il parametro *virtualmachine* è **null**.<br/>                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ macchina virtuale \_ che esegue**</dt> <dt>0xA0040500</dt> </dl>                        | La macchina virtuale è in esecuzione.<br/>                                                                   |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt> </dl> | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                        | Si è verificato un errore imprevisto.<br/>                                                    |



 

## <a name="remarks"></a>Commenti

È possibile annullare la registrazione solo delle macchine virtuali arrestate. I dati relativi allo stato salvato o all'unità di annullamento esistenti per questa configurazione verranno conservati quando viene annullata la registrazione di una macchina virtuale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

