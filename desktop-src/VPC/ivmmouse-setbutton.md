---
title: Metodo IVMMouse SetButton (VPCCOMInterfaces.h)
description: Imposta lo stato corrente (verso l'alto o verso il basso) del pulsante del mouse specificato.
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- Metodo SetButton Virtual PC
- Metodo SetButton Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, metodo SetButton
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
ms.openlocfilehash: 04bdd3d7e0075b050c5184beee0a5da21f184040a03731317f2d61e09c07fd9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974111"
---
# <a name="ivmmousesetbutton-method"></a>Metodo IVMMouse::SetButton

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*buttonIndex* \[ Pollici\]
</dt> <dd>

Indice del pulsante. Per un elenco di valori, vedere [**VMMouseButton.**](vmmousebutton.md)

</dd> <dt>

*down* \[ Pollici\]
</dt> <dd>

Stato del nuovo pulsante. Usare **TRUE** se lo stato del pulsante deve essere impostato su down e **FALSE** se deve essere impostato su up.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                        | Descrizione                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | L'operazione è stata completata.<br/>                                                                                                          |
| <dl> <dt>**E \_ InvalidARG**</dt> <dt>0x80000003</dt> </dl>             | Il *parametro buttonIndex* non è valido.<br/>                                                                                              |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE**</dt> <dt>0xA0040206</dt> </dl>   | La macchina virtuale a cui è collegato il dispositivo mouse non è attualmente in esecuzione.<br/>                                                   |
| <dl> <dt>**Macchina virtuale \_ E \_ MOUSE \_ NOT \_ ACTIVE**</dt> <dt>0xA0040800</dt> </dl> | Non è stato possibile completare l'operazione perché il dispositivo mouse non è acceso o non è attualmente attivo nella macchina virtuale.<br/> |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>        | Si è verificato un errore imprevisto.<br/>                                                                                                      |



 

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

 

