---
title: Metodo IVMVirtualMachine AddHardDiskConnection (VPCCOMInterfaces.h)
description: Aggiunge una nuova connessione al disco rigido alla macchina virtuale.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- Metodo AddHardDiskConnection Virtual PC
- Metodo AddHardDiskConnection Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo AddHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67bbeb5cdb347327a807b19ec16c901c211cdddb72ce88a8b5b00804b195f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592759"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a>Metodo IVMVirtualMachine::AddHardDiskConnection

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Aggiunge una nuova connessione al disco rigido alla macchina virtuale (VM).

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hardDiskPath* \[ Pollici\]
</dt> <dd>

Percorso completo del file del disco rigido virtuale (VHD) da connettere.

</dd> <dt>

*busNumber* \[ Pollici\]
</dt> <dd>

Bus a cui verrà collegata l'unità.



| Valore                                                                        | Significato                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | L'unità verrà collegata al primo bus.<br/>  |
| <dl> <dt>1</dt> </dl> | L'unità verrà collegata al secondo bus.<br/> |



 

</dd> <dt>

*deviceNumber* \[ Pollici\]
</dt> <dd>

Dispositivo a cui verrà collegata l'unità.



| Valore                                                                        | Significato                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | L'unità verrà collegata al primo dispositivo sul bus.<br/>  |
| <dl> <dt>1</dt> </dl> | L'unità verrà collegata al secondo dispositivo sul bus.<br/> |



 

</dd> <dt>

*hardDiskConnection* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMHardDiskConnection.**](ivmharddiskconnection.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                              | Descrizione                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'operazione è stata completata.<br/>                                                                                                                  |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                      | Il *parametro hardDiskConnection* è **NULL.**<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | Un *parametro hardDiskPath* è **NULL** o il *parametro busNumber* o *deviceNumber* non è valido.<br/>                                            |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND) 0X80070002**</dt> <dt></dt> </dl>   | Il sistema non riesce a trovare il file specificato dal *parametro hardDiskPath.*<br/>                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND) 0X80070003**</dt> <dt></dt> </dl>   | Il sistema non riesce a trovare il percorso specificato dal *parametro hardDiskPath.*<br/>                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>      | Il *parametro hardDiskPath* contiene un carattere non valido (uno di " \* ?<>/ \| ":").<br/>                                                        |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>      | Il *parametro hardDiskPath* specifica un percorso vuoto o relativo. È necessario un percorso assoluto.<br/>                                                |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl>   | Il percorso specificato dal *parametro hardDiskPath* è troppo lungo. Il percorso deve contenere meno di 260 caratteri.<br/>                                     |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0XA0040207</dt> </dl>                              | La configurazione è sconosciuta.<br/>                                                                                                                  |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE IN ESECUZIONE O SALVATA \_ \_ \_ 0XA004020B**</dt> <dt></dt> </dl>                   | La macchina virtuale è in uno stato in esecuzione o salvato.<br/>                                                                                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ DRIVE \_ BUS \_ LOC IN USO \_ \_ 0XA00400503**</dt> <dt></dt> </dl>                | La posizione del bus specificata è in uso.<br/>                                                                                                          |
| <dl> <dt>**Macchina virtuale \_ E \_ INVALID \_ HD \_ FILE**</dt> <dt>0xA0040682</dt> </dl>                        | Il disco rigido virtuale è maggiore di 127 GB e non può essere connesso al bus IDE.<br/>                                                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ TIPO DI DISCO HD NON \_ \_ \_ SUPPORTATO**</dt> <dt>0xA00400686</dt> </dl>             | Il *parametro hardDiskPath* fa riferimento a un disco rigido virtuale collegato o a un disco rigido virtuale che differisce da un disco rigido virtuale collegato. I dischi rigidi virtuali collegati non possono essere collegati alle macchine virtuali.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ SHARING \_ VIOLATION)**</dt> <dt>0x80070020</dt> </dl> | Il disco rigido virtuale specificato è già connesso a un'altra posizione del bus per questa macchina virtuale.<br/>                                                                    |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Si è verificato un errore imprevisto.<br/>                                                                                                              |



 

## <a name="remarks"></a>Commenti

È possibile aggiungere una nuova connessione al disco rigido solo a una macchina virtuale arrestata.

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
</dt> </dl>

 

