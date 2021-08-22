---
title: Metodo IVMVirtualPC UnregisterVirtualMachine (VPCCOMInterfaces.h)
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
ms.openlocfilehash: 2e6173d6f43d51384af610b850ec654d185f0a8ce31a375b4dd90bd929c6455b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652731"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a>Metodo IVMVirtualPC::UnregisterVirtualMachine

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Annulla la registrazione di una configurazione di macchina virtuale senza eliminare il file di configurazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*virtualMachine* \[ Pollici\]
</dt> <dd>

Puntatore a un [**oggetto IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta la configurazione della macchina virtuale di cui annullare la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                        | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                | Il *parametro virtualMachine* era **NULL.**<br/>                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ VM \_ RUNNING**</dt> <dt>0xA0040500</dt> </dl>                        | La macchina virtuale è in esecuzione.<br/>                                                                   |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA**</dt> <dt>0XA0040951</dt> </dl> | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Si è verificato un errore imprevisto.<br/>                                                    |



 

## <a name="remarks"></a>Commenti

È possibile annullare la registrazione solo delle macchine virtuali arrestate. I dati esistenti dello stato salvato o dell'unità di annullamento per questa configurazione verranno mantenuti quando viene annullata la registrazione di una macchina virtuale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC è definito come \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

