---
title: Proprietà IVMVirtualMachine Name (VPCCOMInterfaces.h)
description: Nome della configurazione della macchina virtuale.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Proprietà Name Virtual PC
- Proprietà Name Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà Name
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219e6fcb24805feb0370bd157d014767a9348e87e500d8c94fa26ff502b6597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006801"
---
# <a name="ivmvirtualmachinename-property"></a>Proprietà IVMVirtualMachine::Name

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera e imposta il nome della configurazione della macchina virtuale.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a>Valore proprietà

Specifica il nome della configurazione della macchina virtuale. La lunghezza del nome non può essere superiore a 80 caratteri e la lunghezza totale del percorso completo che include il file di configurazione del nome della macchina virtuale non può essere superiore a **MAX \_ PATH** (260).

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                    | Significato                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                       | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                         | Il parametro è **NULL.**<br/>                                                           |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                      | Il parametro non è valido o è una stringa vuota.<br/>                                    |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>                 | La configurazione è sconosciuta.<br/>                                                        |
| <dl> <dt>Macchina virtuale \_ E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl>            | La macchina virtuale è in esecuzione o salvata.<br/>                                             |
| <dl> <dt>Macchina virtuale \_ E \_ CONFIG \_ NO \_ NAME</dt> <dt>0xA0040400</dt> </dl>            | Il *parametro virtualMachineName* è vuoto.<br/>                                         |
| <dl> <dt>Macchina virtuale \_ E \_ CONFIG NAME TOO \_ \_ \_ LONG</dt> <dt>0xA00400401</dt> </dl>    | Il parametro contiene troppi caratteri.<br/>                                          |
| <dl> <dt>Macchina virtuale \_ E \_ CONFIG NAME INVALID \_ \_ \_ CHAR</dt> <dt>0xA0040402</dt> </dl> | Il parametro contiene uno dei caratteri non validi seguenti " \* ?:<>/ \| \\ "".<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ CONFIG \_ DUPLICATE \_ NAME</dt> <dt>0xA0040403</dt> </dl>     | Il nome specificato esiste già come nome di un'altra macchina virtuale.<br/>            |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                 | Si è verificato un errore imprevisto.<br/>                                                    |



## <a name="remarks"></a>Commenti

I nomi delle macchine virtuali non fanno distinzione tra maiuscole e minuscole, ad esempio "MyVM" e "myvm" fanno riferimento alla stessa macchina virtuale. Si tratta della proprietà predefinita per [**IVMVirtualMachine**](ivmvirtualmachine.md).

Se VPC.exe è in esecuzione e la macchina virtuale viene salvata, l'impostazione **della proprietà Name** non avrà esito positivo. Se VPC.exe non è in esecuzione e la macchina virtuale viene salvata, l'impostazione della proprietà **Name** avrà esito positivo al VPC.exe successivo avvio.

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

 

