---
title: Proprietà IVMVirtualPC SearchPaths (VPCCOMInterfaces.h)
description: Percorsi del file system usati per trovare i file associati Windows Virtual PC.
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
ms.openlocfilehash: ac4ef75bf0a696494b839f330063ca310927a0d796829d96575721f492b8b691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471251"
---
# <a name="ivmvirtualpcsearchpaths-property"></a>Proprietà IVMVirtualPC::SearchPaths

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera e imposta i percorsi file system usati per trovare i file associati Windows Virtual PC.

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

Specifica un safearray contenente un file system per ogni voce.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                               | Significato                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                               |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **NULL.**<br/>                                                                                                  |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                                 | Il *parametro searchPaths* non è valido e non è stato possibile analizzarlo in una matrice di percorsi.<br/>                                    |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0x80070002</dt> </dl> | Il sistema non riesce a trovare una directory specificata nel *parametro searchPaths.*<br/>                                                |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)</dt> <dt>0x80070003</dt> </dl> | Il sistema non riesce a trovare un percorso specificato dal *parametro searchPaths.*<br/>                                                     |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)</dt> <dt>0x8007007b</dt> </dl>    | Un percorso specificato nel *parametro searchPaths* contiene caratteri non validi. I caratteri non validi sono " \* ?<>/ \| ":".<br/> |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)</dt> <dt>0x800700a1</dt> </dl>    | Un percorso contenuto nel *parametro searchPaths* specifica un percorso vuoto o relativo. È necessario un percorso assoluto.<br/>          |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato nel *parametro searchPaths* è troppo lungo. La lunghezza del percorso deve essere minore di 260 caratteri.<br/>     |
| <dl> <dt>Macchina virtuale \_ E \_ PREF \_ NOT \_ FOUND</dt> <dt>0xA0040300</dt> </dl>                       | La preferenza non è stata trovata.<br/>                                                                                               |
| <dl> <dt>Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA</dt> <dt>0xA0040951</dt> </dl>     | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/>                                        |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

