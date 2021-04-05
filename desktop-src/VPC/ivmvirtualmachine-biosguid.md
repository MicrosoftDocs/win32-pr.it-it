---
title: Proprietà IVMVirtualMachine BIOSGUID (VPCCOMInterfaces. h)
description: GUID del BIOS.
ms.assetid: d866838d-31e9-41f1-be57-43e778b9db95
keywords:
- Proprietà BIOSGUID Virtual PC
- Proprietà BIOSGUID Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà BIOSGUID
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSGUID
- IVMVirtualMachine.get_BIOSGUID
- IVMVirtualMachine.put_BIOSGUID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10263e32ab71c2a5b9533b3dde6547f774d6b302
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873738"
---
# <a name="ivmvirtualmachinebiosguid-property"></a>Proprietà IVMVirtualMachine:: BIOSGUID

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e imposta il GUID del BIOS.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BIOSGUID(
  [in]          BSTR biosGUID
);

HRESULT get_BIOSGUID(
  [out, retval] BSTR *biosGUID
);
```



## <a name="property-value"></a>Valore proprietà

Specifica il GUID del BIOS. Includere le parentesi graffe sinistra e destra intorno alle cifre esadecimali.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                               | Significato                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                  | L'operazione è stata completata.<br/>                       |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                    | Il parametro è **null**.<br/>                          |
| <dl> <dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG </dl>                 | Il parametro non è valido o è una stringa vuota.<br/>   |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl>            | La configurazione è sconosciuta.<br/>                       |
| <dl> <dt>Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata</dt> <dt>0xA004020B</dt> </dl> | Lo stato della macchina virtuale è in esecuzione o salvato.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>            | Si è verificato un errore imprevisto.<br/>                   |



## <a name="remarks"></a>Commenti

Questa proprietà non conterrà informazioni valide fino a quando la macchina virtuale non viene avviata per la prima volta. Se viene letta prima dell'avvio iniziale, verrà restituita una stringa vuota.

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

 

