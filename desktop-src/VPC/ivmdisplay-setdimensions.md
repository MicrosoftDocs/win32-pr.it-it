---
title: Metodo sedimensions IVMDisplay (VPCCOMInterfaces. h)
description: Imposta l'altezza e la larghezza dello schermo della macchina virtuale, in pixel.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Metodo sedimensions Virtual PC
- Metodo sedimensions Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, metodo sedimensions
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
ms.openlocfilehash: 4730d73e06074714c8e6ed31fda992259d5c19ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302421"
---
# <a name="ivmdisplaysetdimensions-method"></a>Metodo IVMDisplay:: sedimensions

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Imposta l'altezza e la larghezza della visualizzazione della macchina virtuale (VM), in pixel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*displayPixelWidth* \[ in\]
</dt> <dd>

Larghezza, in pixel. Il valore deve essere compreso tra i valori 640 e 2048. Se il valore non è divisibile in modo uniforme per 8, verrà ridotto al multiplo inferiore successivo di 8.

</dd> <dt>

*displayPixelHeight* \[ in\]
</dt> <dd>

Altezza, in pixel. Il valore deve essere compreso tra i valori 480 e 1920.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                    | Descrizione                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                                                                                                                                                                         |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                         | Il parametro *displayPixelWidth* non è divisibile uniformemente per 8 oppure il parametro *displayPixelWidth* o *displayPixelHeight* non è compreso nei valori minimi consentiti (640x480) o 2048x1920 massimi.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt> </dl>                     | La modifica della risoluzione non è stata completata in modo tempestivo.<br/>                                                                                                                                              |
| <dl> <dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt> </dl>               | Per questa operazione è necessario che la macchina virtuale sia in esecuzione.<br/>                                                                                                                                               |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>                    | La macchina virtuale non è valida o non è attualmente in esecuzione.<br/>                                                                                                                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ Nessuna \_ visualizzazione**</dt> <dt>0xA0040850</dt> </dl>                    | Non è possibile individuare una visualizzazione valida per la macchina virtuale.<br/>                                                                                                                                                          |
| <dl> <dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt> </dl> | La versione dei componenti di integrazione installati nel sistema operativo guest non supporta questa operazione.<br/>                                                                                    |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                     |



 

## <a name="remarks"></a>Commenti

Le dimensioni minime della visualizzazione della macchina virtuale sono 640 x 480 pixel. La dimensione massima è 2048 x 1920. Il tentativo di impostare la dimensione di visualizzazione su valori non compresi in questi limiti o su qualsiasi larghezza non divisibile per 8, comporterà la restituzione di un errore **E \_ INVALIDARG** .

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

 

