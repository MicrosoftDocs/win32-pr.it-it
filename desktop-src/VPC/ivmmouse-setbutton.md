---
title: Metodo IVMMouse (VPCCOMInterfaces. h)
description: Imposta lo stato corrente (verso l'alto o verso il basso) del pulsante del mouse specificato.
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- Metodo sebutton Virtual PC
- Metodo sebutton Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, metodo sebutton
topic_type:
- apiref
api_name:
- IVMMouse.SetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d30ae131ac33eeff339b98511fd2da60a1e606
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121102"
---
# <a name="ivmmousesetbutton-method"></a>Metodo IVMMouse:: MyButton

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Imposta lo stato corrente (verso l'alto o verso il basso) del pulsante del mouse specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetButton(
  [in] VMMouseButton buttonIndex,
  [in] VARIANT_BOOL  down
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ButtonIndex* \[ in\]
</dt> <dd>

Indice del pulsante. Per un elenco di valori, vedere [**VMMouseButton**](vmmousebutton.md).

</dd> <dt>

in *basso* \[ in\]
</dt> <dd>

Nuovo stato del pulsante. Utilizzare **true** se lo stato del pulsante deve essere impostato su inattivo e **false** se deve essere impostato su up.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                        | Descrizione                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | L'operazione è stata completata.<br/>                                                                                                          |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>             | Il parametro *ButtonIndex* non è valido.<br/>                                                                                              |
| <dl> <dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt> </dl>   | La macchina virtuale a cui questo dispositivo mouse è collegato non è attualmente in esecuzione.<br/>                                                   |
| <dl> <dt>**Macchina virtuale \_ E \_ mouse \_ non \_ attivo**</dt> <dt>0xA0040800</dt> </dl> | Non è stato possibile completare l'operazione perché il dispositivo mouse non è acceso o non è attualmente attivo nella macchina virtuale.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>        | Si è verificato un errore imprevisto.<br/>                                                                                                      |



 

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

 

