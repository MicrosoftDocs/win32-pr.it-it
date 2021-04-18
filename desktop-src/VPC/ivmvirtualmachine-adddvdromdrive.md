---
title: Metodo IVMVirtualMachine AddDVDROMDrive (VPCCOMInterfaces. h)
description: Aggiunge una nuova unità CD o DVD alla macchina virtuale.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- Metodo AddDVDROMDrive Virtual PC
- Metodo AddDVDROMDrive Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo AddDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7acbe70f6b338b3490c12ab67bcdfdc997d90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301777"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a>Metodo IVMVirtualMachine:: AddDVDROMDrive

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Aggiunge una nuova unità CD o DVD alla macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

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

*dvdDrive* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMDVDDrive**](ivmdvddrive.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                               | Descrizione                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                     | L'operazione è stata completata.<br/>                       |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                       | Il parametro *dvdDrive* è **null**.<br/>               |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                    | Un parametro non è valido.<br/>                           |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>               | La configurazione è sconosciuta.<br/>                       |
| <dl> <dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt> </dl>    | Lo stato della macchina virtuale è in esecuzione o salvato.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ la \_ \_ loc \_ del bus di unità in \_ use**</dt> <dt>0xA00400503</dt> </dl> | Il percorso del bus specificato è in uso.<br/>               |
| <dl> <dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt> </dl>            | L'unità specificata non è valida.<br/>                   |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>               | Si è verificato un errore imprevisto.<br/>                   |



 

## <a name="remarks"></a>Commenti

È possibile aggiungere solo una nuova unità CD o DVD a una macchina virtuale arrestata.

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

 

