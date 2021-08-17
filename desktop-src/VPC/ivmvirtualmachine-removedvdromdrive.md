---
title: Metodo IVMVirtualMachine RemoveDVDROMDrive (VPCCOMInterfaces.h)
description: Rimuove l'unità CD o DVD specificata dalla macchina virtuale.
ms.assetid: 1c45c271-bead-41f6-8371-448d385a1288
keywords:
- Metodo RemoveDVDROMDrive Virtual PC
- Metodo RemoveDVDROMDrive Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo RemoveDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 693d8eebe30c347b41a2b9b0b115c09f6fea75cd8744baa97aa3aca5cd0d1916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752280"
---
# <a name="ivmvirtualmachineremovedvdromdrive-method"></a>Metodo IVMVirtualMachine::RemoveDVDROMDrive

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Rimuove l'unità CD o DVD specificata dalla macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveDVDROMDrive(
  [in] IVMDVDDrive *dvdDrive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dvdDrive* \[ Pollici\]
</dt> <dd>

Unità da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                            | Descrizione                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | L'operazione è stata completata.<br/>                              |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                    | Il parametro è **NULL.**<br/>                                 |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>            | La configurazione è sconosciuta.<br/>                              |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE IN ESECUZIONE O SALVATA \_ \_ \_ 0XA004020B**</dt> <dt></dt> </dl> | La macchina virtuale è in esecuzione o salvata.<br/>        |
| <dl> <dt>**Macchina virtuale \_ E \_ UNITÀ \_ NON VALIDA**</dt> <dt>0xA0040502</dt> </dl>         | L'unità specificata non è connessa a questa posizione del bus.<br/> |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>            | Si è verificato un errore imprevisto.<br/>                          |



 

## <a name="remarks"></a>Commenti

È possibile rimuovere solo un'unità CD o DVD esistente da una macchina virtuale arrestata.

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

 

