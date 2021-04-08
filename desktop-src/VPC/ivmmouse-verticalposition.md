---
title: Proprietà IVMMouse VerticalPosition (VPCCOMInterfaces. h)
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
ms.openlocfilehash: 64712f557a3fcd59181e8ce65d835b630da68e48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964870"
---
# <a name="ivmmouseverticalposition-property"></a>Proprietà IVMMouse:: VerticalPosition

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

Coordinata y che indica la nuova posizione del mouse. Quando si usano le coordinate assolute, questo valore specifica la nuova coordinata y del mouse. Quando si usano le coordinate relative, questo valore specifica il numero di pixel che il mouse deve spostare nella direzione y.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                                                                                                                |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                            | Il parametro è **null**.<br/>                                                                                                                   |
| <dl> <dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale a cui questo dispositivo mouse è collegato non è attualmente in esecuzione.<br/>                                                         |
| <dl> <dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt> </dl> | È necessario installare i componenti di integrazione per recuperare la posizione del mouse o per impostare la posizione del mouse quando si utilizzano le coordinate assolute.<br/>       |
| <dl> <dt>Macchina virtuale \_ E \_ utilizzo \_ di \_ coordinate relative</dt> <dt>0xA0040802</dt> </dl>   | Il dispositivo mouse è attualmente impostato per l'utilizzo di coordinate relative del mouse.<br/>                                                                         |
| <dl> <dt>Macchina virtuale \_ E \_ mouse \_ non \_ attivo</dt> <dt>0xA0040800</dt> </dl>             | Non è possibile recuperare le coordinate assolute se il dispositivo mouse non è acceso o se non è attualmente attivo nella macchina virtuale.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                                                                                            |



## <a name="remarks"></a>Commenti

Impossibile recuperare questa proprietà quando si utilizzano le coordinate relative.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse è definito come ac903f6d-6346-4F29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

