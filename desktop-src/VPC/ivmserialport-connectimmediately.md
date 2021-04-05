---
title: Proprietà IVMSerialPort ConnectImmediately (VPCCOMInterfaces. h)
description: Determina se la porta seriale deve essere aperta senza attendere la ricezione di un comando del modem.
ms.assetid: 5ac22906-0fe2-477d-98af-7c05ce274cc5
keywords:
- Proprietà ConnectImmediately Virtual PC
- Proprietà ConnectImmediately Virtual PC, interfaccia IVMSerialPort
- Interfaccia IVMSerialPort Virtual PC, proprietà ConnectImmediately
topic_type:
- apiref
api_name:
- IVMSerialPort.ConnectImmediately
- IVMSerialPort.get_ConnectImmediately
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7661b9cf3b118427b1ecb2b6f450913e35e35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741743"
---
# <a name="ivmserialportconnectimmediately-property"></a>Proprietà IVMSerialPort:: ConnectImmediately

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se la porta seriale deve essere aperta senza attendere la ricezione di un comando del modem.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ConnectImmediately(
  [out, retval] VARIANT_BOOL *vmConnectImmediately
);
```



## <a name="property-value"></a>Valore proprietà

**Variante \_ TRUE** se la porta seriale deve essere aperta senza attendere la ricezione di un comando del modem. **Variante \_** In caso contrario, false.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                            |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>                               |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl> | La configurazione per questa macchina virtuale non è valida.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/>                        |



## <a name="remarks"></a>Commenti

Questa proprietà è valida solo se la proprietà [**tipo**](ivmserialport-type.md) porta è **vmSerialPort \_ portahost**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort è definito come 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

