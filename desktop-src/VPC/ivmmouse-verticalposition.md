---
title: Proprietà IVMMouse VerticalPosition (VPCCOMInterfaces.h)
description: Coordinata y assoluta del mouse.
ms.assetid: 02fd3677-95d8-44b4-b398-d3ec62e5d9f0
keywords:
- Proprietà VerticalPosition Virtual PC
- Proprietà VerticalPosition Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, proprietà VerticalPosition
topic_type:
- apiref
api_name:
- IVMMouse.VerticalPosition
- IVMMouse.get_VerticalPosition
- IVMMouse.put_VerticalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f202a81e5d95909f1ec223087aceecb2a221c9836d1fcd799734f81a250141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344808"
---
# <a name="ivmmouseverticalposition-property"></a>Proprietà IVMMouse::VerticalPosition

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la coordinata y assoluta del mouse.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_VerticalPosition(
  [in]          long position
);

HRESULT get_VerticalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a>Valore proprietà

Coordinata y che indica la nuova posizione del mouse. Quando si usano coordinate assolute, questo valore specifica la nuova coordinata y del mouse. Quando si usano coordinate relative, questo valore specifica il numero di pixel in cui il mouse deve essere spostato nella direzione y.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                                                                                                                |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                            | Il parametro è **NULL.**<br/>                                                                                                                   |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale a cui è collegato il dispositivo mouse non è attualmente in esecuzione.<br/>                                                         |
| <dl> <dt>Macchina virtuale \_ FUNZIONALITÀ \_ DELLE AGGIUNTE E NON \_ \_ \_ 0XA0040505</dt> <dt></dt> </dl> | I componenti di integrazione devono essere installati per recuperare la posizione del mouse o per impostare la posizione del mouse quando si utilizzano coordinate assolute.<br/>       |
| <dl> <dt>Macchina virtuale \_ E \_ USO DELLE COORDINATE RELATIVE \_ \_ 0XA0040802</dt> <dt></dt> </dl>   | Il dispositivo mouse è attualmente impostato per l'utilizzo di coordinate relative del mouse.<br/>                                                                         |
| <dl> <dt>Macchina virtuale \_ E \_ MOUSE \_ NOT \_ ACTIVE</dt> <dt>0xA0040800</dt> </dl>             | Le coordinate assolute non possono essere recuperate se il dispositivo mouse non è acceso o se non è attualmente attivo nella macchina virtuale.<br/> |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                                                                                            |



## <a name="remarks"></a>Commenti

Questa proprietà non può essere recuperata quando si utilizzano coordinate relative.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse è definito come ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

