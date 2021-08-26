---
title: Metodo IVMMouse Click (VPCCOMInterfaces.h)
description: Simula il clic di un pulsante del mouse.
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- Fare clic sul metodo Virtual PC
- Fare clic sul metodo Virtual PC , interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, metodo Click
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d1d1aaf538ac6b30a27df904729f2ad3187ebde29cb915c3d7ef35d1e9cf57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974250"
---
# <a name="ivmmouseclick-method"></a>Metodo IVMMouse::Click

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Simula il clic di un pulsante del mouse.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*buttonIndex* \[ Pollici\]
</dt> <dd>

Indice del pulsante selezionato. Per un elenco di valori, vedere [**VMMouseButton.**](vmmousebutton.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                        | Descrizione                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | L'operazione è stata completata.<br/>                                                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>             | Il parametro è **NULL.**<br/>                                                                                                             |
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

 

