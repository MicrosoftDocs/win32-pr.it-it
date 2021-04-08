---
title: Metodo pause IVMVirtualMachine (VPCCOMInterfaces. h)
description: Sospende la macchina virtuale.
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- Sospendere il metodo Virtual PC
- Sospendere il metodo Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo pause
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c953da05d34c999066a6bc87cb1f51983defbd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874173"
---
# <a name="ivmvirtualmachinepause-method"></a>IVMVirtualMachine::P metodo ause

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Sospende la macchina virtuale (VM).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                          | Descrizione                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | L'operazione è stata completata.<br/>                                     |
| <dl> <dt>**E \_ ERRORE**</dt> <dt>0x80004005</dt> </dl>                                     | La macchina virtuale è già sospesa.<br/>                                         |
| <dl> <dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt> </dl> | Il chiamante deve disporre delle autorizzazioni di accesso Execute per sospendere la macchina virtuale.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt> </dl>                           | L'operazione non è stata completata in modo tempestivo.<br/>                |
| <dl> <dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt> </dl>                     | La macchina virtuale non è in esecuzione.<br/>                               |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>                          | La configurazione è sconosciuta.<br/>                                     |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                          | Si è verificato un errore imprevisto.<br/>                                 |



 

## <a name="remarks"></a>Commenti

**Sospende** non salva lo stato corrente della macchina virtuale.

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

 

