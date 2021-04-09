---
title: Proprietà IVMVirtualPC SearchPaths (VPCCOMInterfaces. h)
description: Percorsi del file System usati per trovare i file associati a Windows Virtual PC.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- Proprietà SearchPaths Virtual PC
- Proprietà SearchPaths Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà SearchPaths
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287eb07bc9205f9b6f0851bd8809f9a49dcf3242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739746"
---
# <a name="ivmvirtualpcsearchpaths-property"></a>Proprietà IVMVirtualPC:: SearchPaths

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e imposta i percorsi di file system utilizzati per trovare i file associati a Windows Virtual PC.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a>Valore proprietà

Specifica un SafeArray contenente un percorso di file system per ogni voce.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                               | Significato                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                               |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **null**.<br/>                                                                                                  |
| <dl> <dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG </dl>                                 | Il parametro *SearchPaths* non è valido e non può essere analizzato in una matrice di percorsi.<br/>                                    |
| <dl> <dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt> </dl> | Il sistema non è in grado di trovare una directory specificata nel parametro *SearchPaths* .<br/>                                                |
| <dl> <dt>HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)</dt> <dt>0 x 80070003</dt> </dl> | Il sistema non è in grado di trovare un percorso specificato dal parametro *SearchPaths* .<br/>                                                     |
| <dl> <dt>HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )</dt> <dt>0x8007007b</dt> </dl>    | Un percorso specificato nel parametro *SearchPaths* contiene caratteri non validi. I caratteri non validi sono " \* ? <>/ \| ": ".<br/> |
| <dl> <dt>HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)</dt> <dt>0x800700a1</dt> </dl>    | Un percorso contenuto nel parametro *SearchPaths* specifica un percorso vuoto o relativo. È necessario specificare un percorso assoluto.<br/>          |
| <dl> <dt>HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato nel parametro *SearchPaths* è troppo lungo. La lunghezza del percorso deve essere inferiore a 260 caratteri.<br/>     |
| <dl> <dt>Macchina virtuale \_ E \_ pref \_ non \_ trovato</dt> <dt>0xA0040300</dt> </dl>                       | La preferenza non è stata trovata.<br/>                                                                                               |
| <dl> <dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt> </dl>     | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/>                                        |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

