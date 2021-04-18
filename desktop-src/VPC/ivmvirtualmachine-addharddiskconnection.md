---
title: Metodo IVMVirtualMachine AddHardDiskConnection (VPCCOMInterfaces. h)
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
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301776"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a>Metodo IVMVirtualMachine:: AddHardDiskConnection

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*hardDiskPath* \[ in\]
</dt> <dd>

Percorso completo del file del disco rigido virtuale (VHD) da connettere.

</dd> <dt>

*busNumber* \[ in\]
</dt> <dd>

Il bus al quale verrà collegata l'unità.



| Valore                                                                        | Significato                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | L'unità verrà collegata al primo bus.<br/>  |
| <dl> <dt>1</dt> </dl> | L'unità verrà collegata al secondo bus.<br/> |



 

</dd> <dt>

*deviceNumber* \[ in\]
</dt> <dd>

Dispositivo a cui verrà collegata l'unità.



| Valore                                                                        | Significato                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | L'unità verrà collegata al primo dispositivo del bus.<br/>  |
| <dl> <dt>1</dt> </dl> | L'unità verrà collegata al secondo dispositivo del bus.<br/> |



 

</dd> <dt>

*hardDiskConnection* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMHardDiskConnection**](ivmharddiskconnection.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                              | Descrizione                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'operazione è stata completata.<br/>                                                                                                                  |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                      | Il parametro *hardDiskConnection* è **null**.<br/>                                                                                                |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                                   | Il parametro *hardDiskPath* è **null** o il parametro *busNumber* o *deviceNumber* non è valido.<br/>                                            |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)**</dt> <dt>0x80070002</dt> </dl>   | Il sistema non è in grado di trovare il file specificato dal parametro *hardDiskPath* .<br/>                                                                     |
| <dl> <dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt> </dl>   | Il sistema non è in grado di trovare il percorso specificato dal parametro *hardDiskPath* .<br/>                                                                     |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt> </dl>      | Il parametro *hardDiskPath* contiene un carattere non valido (uno di " \* ? <>/ \| ": ").<br/>                                                        |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt> </dl>      | Il parametro *hardDiskPath* specifica un percorso vuoto o relativo. È necessario specificare un percorso assoluto.<br/>                                                |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt> </dl>   | Il percorso specificato dal parametro *hardDiskPath* è troppo lungo. Il percorso deve essere composto da meno di 260 caratteri.<br/>                                     |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>                              | La configurazione è sconosciuta.<br/>                                                                                                                  |
| <dl> <dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt> </dl>                   | Lo stato della macchina virtuale è in esecuzione o salvato.<br/>                                                                                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ la \_ \_ loc \_ del bus di unità in \_ use**</dt> <dt>0xA00400503</dt> </dl>                | Il percorso del bus specificato è in uso.<br/>                                                                                                          |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ \_ file HD non valido**</dt> <dt>0xA0040682</dt> </dl>                        | Il disco rigido virtuale è maggiore di 127 GB e non può essere connesso al bus IDE.<br/>                                                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ \_ \_ tipo di disco HD non supportato**</dt> <dt>0xA00400686</dt> </dl>             | Il parametro *hardDiskPath* fa riferimento a un VHD collegato o a un disco rigido virtuale differenze in un disco rigido virtuale collegato. Non è possibile collegare VHD collegati alle macchine virtuali.<br/> |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (violazione della condivisione degli errori \_ \_ )**</dt> <dt>0x80070020</dt> </dl> | Il disco rigido virtuale specificato è già connesso a un altro percorso del bus per questa macchina virtuale.<br/>                                                                    |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                              | Si è verificato un errore imprevisto.<br/>                                                                                                              |



 

## <a name="remarks"></a>Commenti

È possibile aggiungere solo una nuova connessione al disco rigido a una macchina virtuale arrestata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

