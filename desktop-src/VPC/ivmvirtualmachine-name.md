---
title: Proprietà Name di IVMVirtualMachine (VPCCOMInterfaces. h)
description: Nome della configurazione della macchina virtuale.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Nome proprietà PC virtuale
- Proprietà nome Virtual PC, interfaccia IVMVirtualMachine
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
ms.openlocfilehash: c163173a778d8103922fd8c8948ab5156f512ed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120051"
---
# <a name="ivmvirtualmachinename-property"></a>Proprietà IVMVirtualMachine:: Name

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

Specifica il nome della configurazione della macchina virtuale. La lunghezza del nome non può superare i 80 caratteri e la lunghezza totale del percorso completo che include il file di configurazione del nome della macchina virtuale non può essere maggiore di **Max \_ path** (260) caratteri.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                    | Significato                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                       | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                         | Il parametro è **null**.<br/>                                                           |
| <dl> <dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG </dl>                      | Il parametro non è valido o è una stringa vuota.<br/>                                    |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl>                 | La configurazione è sconosciuta.<br/>                                                        |
| <dl> <dt>Macchina virtuale \_ 0xA0040302 \_ virtuale E pref \_ VM \_ attiva</dt> <dt></dt> </dl>            | La macchina virtuale è in esecuzione o salvata.<br/>                                             |
| <dl> <dt>Macchina virtuale \_ E \_ config \_ senza \_ nome</dt> <dt>0xA0040400</dt> </dl>            | Il parametro *virtualMachineName* è vuoto.<br/>                                         |
| <dl> <dt>Macchina virtuale \_ Nome di configurazione di E \_ \_ \_ troppo \_ lungo</dt> <dt>0xA00400401</dt> </dl>    | Il parametro contiene troppi caratteri.<br/>                                          |
| <dl> <dt>Macchina virtuale \_ Il \_ nome di configurazione E 0xA0040402 \_ non è \_ valido \_ </dt> <dt></dt> </dl> | Il parametro contiene uno dei seguenti caratteri non validi \* : "?: <>/ \| \\ " ".<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ config \_ \_ nome duplicato</dt> <dt>0xA0040403</dt> </dl>     | Il nome specificato esiste già come nome di un'altra macchina virtuale.<br/>            |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                 | Si è verificato un errore imprevisto.<br/>                                                    |



## <a name="remarks"></a>Commenti

I nomi delle macchine virtuali non fanno distinzione tra maiuscole e minuscole, ad esempio "MyVM" e "MyVM" fanno riferimento alla stessa macchina virtuale. Si tratta della proprietà predefinita per [**IVMVirtualMachine**](ivmvirtualmachine.md).

Se VPC.exe è in esecuzione e la macchina virtuale viene salvata, l'impostazione della proprietà **Name** avrà esito negativo. Se VPC.exe non è in esecuzione e la macchina virtuale viene salvata, l'impostazione della proprietà **Name** avrà esito positivo al successivo avvio di VPC.exe.

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

 

