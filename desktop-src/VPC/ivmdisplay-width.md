---
title: Proprietà Width di IVMDisplay (VPCCOMInterfaces.h)
description: Larghezza dello schermo della macchina virtuale, in pixel.
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Proprietà Larghezza Virtual PC
- Proprietà Width Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, proprietà Width
topic_type:
- apiref
api_name:
- IVMDisplay.Width
- IVMDisplay.get_Width
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db106804f81f52b669b90920699761061d97fb3412dd58b761f7da1701ec53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654221"
---
# <a name="ivmdisplaywidth-property"></a>Proprietà IVMDisplay::Width

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la larghezza dello schermo della macchina virtuale(VM), in pixel.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Width(
  [out, retval] long *displayPixelWidth
);
```



## <a name="property-value"></a>Valore proprietà

Larghezza, in pixel.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                         | Significato                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | L'operazione è stata completata.<br/>                                 |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>              | Il parametro è **NULL.**<br/>                                    |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE</dt> <dt>0xA0040206</dt> </dl> | La macchina virtuale deve essere in esecuzione per questa operazione.<br/>       |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>      | La macchina virtuale non è valida o non è attualmente in esecuzione.<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ NO \_ DISPLAY</dt> <dt>0xA0040850</dt> </dl>      | Impossibile individuare una visualizzazione valida per la macchina virtuale.<br/>     |
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

 

