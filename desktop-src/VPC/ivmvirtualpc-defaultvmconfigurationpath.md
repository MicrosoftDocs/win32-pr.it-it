---
title: Proprietà IVMVirtualPC DefaultVMConfigurationPath (VPCCOMInterfaces.h)
description: Directory predefinita in cui cercare i file di configurazione delle macchine virtuali disponibili.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- Proprietà DefaultVMConfigurationPath Virtual PC
- Proprietà DefaultVMConfigurationPath Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà DefaultVMConfigurationPath
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f6370dfb868ec386e05f361240a74412f13a7d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387637"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a>Proprietà IVMVirtualPC::D efaultVMConfigurationPath

\[Virtual PC Windows non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera e imposta la directory predefinita in cui cercare i file di configurazione delle macchine virtuali disponibili.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a>Valore proprietà

Specifica il percorso della directory per i file di configurazione predefiniti della macchina virtuale. Nella stringa di percorso, una barra rovesciata ( ) può essere visualizzata \\ immediatamente prima del carattere Null di terminazione.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                               | Significato                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                                 |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                                    | Il *parametro configurationPath* è **NULL.**<br/>                                                                                                |
| <dl> <dt>HRESULT \_ DA \_ WIN32(FILE \_ DI ERRORE NON \_ \_ TROVATO) 0X80070002</dt> <dt></dt> </dl> | Il sistema non riesce a trovare la directory specificata dal *parametro configurationPath.*<br/>                                                          |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND) 0X80070003</dt> <dt></dt> </dl> | Il sistema non riesce a trovare il percorso specificato dal *parametro configurationPath.*<br/>                                                               |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)</dt> <dt>0x8007007b</dt> </dl>    | Il *parametro configurationPath* contiene un carattere non valido (uno dei seguenti: " \* ?<>/ \| ":").<br/>                                   |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)</dt> <dt>0x800700a1</dt> </dl>    | Il *parametro configurationPath* specifica un percorso vuoto o relativo. È necessario un percorso assoluto.<br/>                                          |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dal *parametro configurationPath* è troppo lungo. La lunghezza del percorso deve essere minore di **MAX \_ PATH** (260 caratteri).<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                                             |
| <dl> <dt>Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA</dt> <dt>0XA0040951</dt> </dl>     | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/>                                                          |



## <a name="remarks"></a>Commenti

Per impostazione predefinita, questo valore della proprietà è impostato sulla directory seguente: "%LocalAppData% \\ Microsoft Windows Virtual PC Virtual \\ \\ \\ Machines".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 7 \[\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC è definito come \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

