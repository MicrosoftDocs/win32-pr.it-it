---
title: Proprietà IVMMouse HorizontalPosition (VPCCOMInterfaces.h)
description: Coordinata x assoluta del mouse.
ms.assetid: 8cf2a247-b6db-49f6-8e19-c862004f26cd
keywords:
- Proprietà HorizontalPosition Virtual PC
- Proprietà HorizontalPosition Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, proprietà HorizontalPosition
topic_type:
- apiref
api_name:
- IVMMouse.HorizontalPosition
- IVMMouse.get_HorizontalPosition
- IVMMouse.put_HorizontalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2cb3fde1caff23845c653024d9c5e2859b0b7b5df8502dbaea167d3e969a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007151"
---
# <a name="ivmmousehorizontalposition-property"></a>Proprietà IVMMouse::HorizontalPosition

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la coordinata x assoluta del mouse.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_HorizontalPosition(
  [in]          long position
);

HRESULT get_HorizontalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a>Valore proprietà

Coordinata x che indica la nuova posizione del mouse. Quando si usano coordinate assolute, questo valore specifica la nuova coordinata x del mouse. Quando si usano le coordinate relative, questo valore specifica il numero di pixel in cui il mouse deve essere spostato nella direzione x.

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

 

