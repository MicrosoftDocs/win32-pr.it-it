---
title: Metodo IVMVirtualMachine AddDVDROMDrive (VPCCOMInterfaces.h)
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
ms.openlocfilehash: 63a875af50d38270b898c17f2848a4e4b33fe79a4b17d9ab7b6be58cdcfcf92f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123231"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a>Metodo IVMVirtualMachine::AddDVDROMDrive

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*dvdDrive* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMDVDDrive.**](ivmdvddrive.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                               | Descrizione                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                     | L'operazione è stata completata.<br/>                       |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                       | Il *parametro dvdDrive* è **NULL.**<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                    | Un parametro non è valido.<br/>                           |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>               | La configurazione è sconosciuta.<br/>                       |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE IN ESECUZIONE O SALVATA \_ \_ \_ 0XA004020B**</dt> <dt></dt> </dl>    | Lo stato della macchina virtuale è in esecuzione o salvato.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ DRIVE \_ BUS \_ LOC IN USO \_ \_ 0XA00400503**</dt> <dt></dt> </dl> | La posizione del bus specificata è in uso.<br/>               |
| <dl> <dt>**Macchina virtuale \_ E \_ UNITÀ \_ NON**</dt> VALIDA <dt>0xA0040502</dt> </dl>            | L'unità specificata non è valida.<br/>                   |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>               | Si è verificato un errore imprevisto.<br/>                   |



 

## <a name="remarks"></a>Commenti

È possibile aggiungere una nuova unità CD o DVD solo a una macchina virtuale arrestata.

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

 

