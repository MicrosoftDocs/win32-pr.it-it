---
title: Proprietà Height IVMDisplay (VPCCOMInterfaces.h)
description: Altezza dello schermo della macchina virtuale, in pixel.
ms.assetid: 4fbb7c2b-6d5f-4af6-b8cc-3a7546b15cbd
keywords:
- Proprietà Height di Virtual PC
- Proprietà Height Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, proprietà Height
topic_type:
- apiref
api_name:
- IVMDisplay.Height
- IVMDisplay.get_Height
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab20a1990d16591bec284514a2d8ad7b3f2a05ea9f6fcae234037078d66f4ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654321"
---
# <a name="ivmdisplayheight-property"></a>Proprietà IVMDisplay::Height

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera l'altezza dello schermo della macchina virtuale, in pixel.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Height(
  [out, retval] long *displayPixelHeight
);
```



## <a name="property-value"></a>Valore proprietà

Altezza, in pixel.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                         | Significato                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | L'operazione è stata completata.<br/>                                 |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>              | Il parametro è **NULL.**<br/>                                    |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE</dt> <dt>0xA0040206</dt> </dl> | La macchina virtuale deve essere in esecuzione per questa operazione.<br/>       |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>      | La macchina virtuale non è valida o non è attualmente in esecuzione.<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ NESSUNA \_ VISUALIZZAZIONE</dt> <dt>0xA0040850</dt> </dl>      | Impossibile individuare una visualizzazione valida per la macchina virtuale.<br/>     |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>      | Si è verificato un errore imprevisto.<br/>                             |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

