---
title: Metodo IVMDisplay SetDimensions (VPCCOMInterfaces.h)
description: Imposta l'altezza e la larghezza dello schermo della macchina virtuale, in pixel.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Metodo SetDimensions Virtual PC
- Metodo SetDimensions Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, metodo SetDimensions
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbf1db342342e9fbb8c0eff2df18f9c2a76443a4d20014bad34934ccecd3dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473361"
---
# <a name="ivmdisplaysetdimensions-method"></a>Metodo IVMDisplay::SetDimensions

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Imposta l'altezza e la larghezza dello schermo della macchina virtuale(VM), in pixel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*displayPixelWidth* \[ Pollici\]
</dt> <dd>

Larghezza, in pixel. Il valore deve essere compreso tra 640 e 2048. Se il valore non è divisibile in modo uniforme per 8, verrà ridotto al successivo multiplo inferiore di 8.

</dd> <dt>

*displayPixelHeight* \[ Pollici\]
</dt> <dd>

Altezza, in pixel. Il valore deve essere compreso tra 480 e 1920.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                    | Descrizione                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                                                                                                                                                                         |
| <dl> <dt>**E \_ InvalidARG**</dt> <dt>0x80000003</dt> </dl>                         | Il *parametro displayPixelWidth* non è divisibile in modo uniforme per 8 o il parametro *displayPixelWidth* o *displayPixelHeight* non rientra nei valori minimi consentiti (640x480) o al massimo 2048x1920.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ TIMEOUT \_ 0xA0040202**</dt> <dt></dt> </dl>                     | La modifica della risoluzione non è stata completata in modo corretto.<br/>                                                                                                                                              |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE**</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale deve essere in esecuzione per questa operazione.<br/>                                                                                                                                               |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>                    | La macchina virtuale non è valida o non è attualmente in esecuzione.<br/>                                                                                                                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ NO \_ DISPLAY**</dt> <dt>0xA0040850</dt> </dl>                    | Impossibile individuare una visualizzazione valida per la macchina virtuale.<br/>                                                                                                                                                          |
| <dl> <dt>**Macchina virtuale \_ FUNZIONALITÀ \_ DELLE AGGIUNTE E NON \_ \_ \_ 0XA0040505**</dt> <dt></dt> </dl> | La versione dei componenti di integrazione installata nel sistema operativo guest non supporta questa operazione.<br/>                                                                                    |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                     |



 

## <a name="remarks"></a>Commenti

La dimensione minima dello schermo della macchina virtuale è 640 x 480 pixel. La dimensione massima è 2048 x 1920. I tentativi di impostare le dimensioni di visualizzazione su valori al di fuori di questi limiti o su qualsiasi larghezza non uniformemente divisibile per 8 restituiranno un errore **E \_ INVALIDARG.**

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

 

