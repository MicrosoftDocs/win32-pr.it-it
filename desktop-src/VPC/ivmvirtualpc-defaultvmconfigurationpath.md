---
title: Proprietà IVMVirtualPC DefaultVMConfigurationPath (VPCCOMInterfaces. h)
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
ms.openlocfilehash: e13fc2323cb15bdbeb8c42e61810a376e49b3988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742730"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a>IVMVirtualPC::D Proprietà efaultVMConfigurationPath

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

Specifica il percorso della directory per i file di configurazione predefiniti della macchina virtuale. Nella stringa di percorso, una barra rovesciata ( \) può apparire immediatamente prima del carattere null di terminazione.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                               | Significato                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                                 |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro *configurationPath* è **null**.<br/>                                                                                                |
| <dl> <dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt> </dl> | Il sistema non è in grado di trovare la directory specificata dal parametro *configurationPath* .<br/>                                                          |
| <dl> <dt>HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)</dt> <dt>0 x 80070003</dt> </dl> | Il sistema non è in grado di trovare il percorso specificato dal parametro *configurationPath* .<br/>                                                               |
| <dl> <dt>HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )</dt> <dt>0x8007007b</dt> </dl>    | Il parametro *configurationPath* contiene un carattere non valido (uno dei seguenti: " \* ? <>/ \| ": ").<br/>                                   |
| <dl> <dt>HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)</dt> <dt>0x800700a1</dt> </dl>    | Il parametro *configurationPath* specifica un percorso vuoto o relativo. È necessario specificare un percorso assoluto.<br/>                                          |
| <dl> <dt>HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dal parametro *configurationPath* è troppo lungo. La lunghezza del percorso deve essere minore di **Max \_ path** (260) caratteri.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                                             |
| <dl> <dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt> </dl>     | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/>                                                          |



## <a name="remarks"></a>Commenti

Per impostazione predefinita, il valore di questa proprietà è impostato sulla directory seguente: "% LocalAppData% \\ Microsoft \\ Windows Virtual PC \\ macchine virtuali \\ ".

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

 

