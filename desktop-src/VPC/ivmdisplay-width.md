---
title: Proprietà Width IVMDisplay (VPCCOMInterfaces. h)
description: Larghezza, in pixel, dello schermo della macchina virtuale.
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Proprietà larghezza PC virtuale
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
ms.openlocfilehash: 12b6fe7d329498b0f1ffc36304311f733cd990c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518802"
---
# <a name="ivmdisplaywidth-property"></a>Proprietà IVMDisplay:: Width

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera la larghezza della visualizzazione della macchina virtuale (VM), in pixel.

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
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>              | Il parametro è **null**.<br/>                                    |
| <dl> <dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt> </dl> | Per questa operazione è necessario che la macchina virtuale sia in esecuzione.<br/>       |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl>      | La macchina virtuale non è valida o non è attualmente in esecuzione.<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ Nessuna \_ visualizzazione</dt> <dt>0xA0040850</dt> </dl>      | Non è possibile individuare una visualizzazione valida per la macchina virtuale.<br/>     |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>      | Si è verificato un errore imprevisto.<br/>                             |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

