---
title: Metodo IVMMouse GetButton (VPCCOMInterfaces.h)
description: Recupera lo stato corrente del pulsante del mouse specificato.
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- Metodo GetButton Virtual PC
- Metodo GetButton Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, metodo GetButton
topic_type:
- apiref
api_name:
- IVMMouse.GetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af37a303c90fb9c60020f19f22767ec508c53fdc54bcefa533dabc780c38f16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007161"
---
# <a name="ivmmousegetbutton-method"></a>Metodo IVMMouse::GetButton

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera lo stato corrente (verso l'alto o verso il basso) del pulsante del mouse specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetButton(
  [in]          VMMouseButton buttonIndex,
  [out, retval] VARIANT_BOOL  *isDown
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*buttonIndex* \[ Pollici\]
</dt> <dd>

Indice del pulsante di cui viene richiesto lo stato. Per un elenco di valori, vedere [**VMMouseButton.**](vmmousebutton.md)

</dd> <dt>

*isDown* \[ out, retval\]
</dt> <dd>

Stato del pulsante indicato. **TRUE** se il pulsante è attualmente in basso nella macchina virtuale, **FALSE in caso contrario.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                        | Descrizione                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                | Il *parametro isDown* è **NULL.**<br/>                                                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>             | Il *parametro buttonIndex* non è valido.<br/>                                            |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE**</dt> <dt>0xA0040206</dt> </dl>   | La macchina virtuale a cui è collegato il dispositivo mouse non è attualmente in esecuzione.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ MOUSE \_ NOT \_ ACTIVE**</dt> <dt>0xA0040800</dt> </dl> | Il dispositivo mouse non è stato acceso.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>        | Si è verificato un errore imprevisto.<br/>                                                    |



 

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

 

