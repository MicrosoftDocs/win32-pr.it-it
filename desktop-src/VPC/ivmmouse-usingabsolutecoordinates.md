---
title: Proprietà IVMMouse UsingAbsoluteCoordinates (VPCCOMInterfaces.h)
description: Recupera un valore che indica se le coordinate del mouse rappresentano coordinate assolute o relative.
ms.assetid: 668278f8-28ae-4128-9653-4985bddbe184
keywords:
- Uso della proprietàAbsoluteCoordinates virtual PC
- Uso della proprietà Virtual PC diAbsoluteCoordinates , interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC , proprietà UsingAbsoluteCoordinates
topic_type:
- apiref
api_name:
- IVMMouse.UsingAbsoluteCoordinates
- IVMMouse.get_UsingAbsoluteCoordinates
- IVMMouse.put_UsingAbsoluteCoordinates
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5695489179abdf6719d9375ac5fa3e2b57a60f3e495475745637aad4b12a3737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118844148"
---
# <a name="ivmmouseusingabsolutecoordinates-property"></a>Proprietà IVMMouse::UsingAbsoluteCoordinates

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera un valore che indica se le coordinate del mouse rappresentano coordinate assolute o relative.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_UsingAbsoluteCoordinates(
  [in]          VARIANT_BOOL usingAbsoluteCoordinates
);

HRESULT get_UsingAbsoluteCoordinates(
  [out, retval] VARIANT_BOOL *usingAbsoluteCoordinates
);
```



## <a name="property-value"></a>Valore proprietà

**VARIANT \_ TRUE** per impostare il dispositivo mouse per l'utilizzo di coordinate assolute, **VARIANT \_ FALSE** per usare le coordinate relative.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                                                                              |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                            | Il parametro è **NULL.**<br/>                                                                                 |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale a cui è collegato il dispositivo mouse non è attualmente in esecuzione.<br/>                       |
| <dl> <dt>Macchina virtuale \_ FUNZIONALITÀ \_ DELLE AGGIUNTE E NON \_ \_ \_ 0XA0040505</dt> <dt></dt> </dl> | I componenti di integrazione non sono installati. I componenti di integrazione sono necessari per usare coordinate assolute.<br/> |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                                                          |



## <a name="remarks"></a>Commenti

Questa proprietà è locale solo per questo oggetto e per impostazione predefinita sarà **VARIANT \_ FALSE** per un [**nuovo oggetto IVMMouse.**](ivmmouse.md) Si noti che i componenti di integrazione devono essere installati per poter usare le coordinate assolute.

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

 

