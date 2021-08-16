---
title: Proprietà IWMPClosedCaption SAMIFileName
description: La proprietà SAMIFileName ottiene o imposta il nome di un file contenente le informazioni necessarie per i sottotitoli codificati.
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Proprietà SAMIFileName Windows Media Player
- Proprietà SAMIFileName Windows Media Player, interfaccia IWMPClosedCaption
- Interfaccia IWMPClosedCaption Windows Media Player proprietà , SAMIFileName
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 973b0757eca4251e74180d829205ee6c7080ca821db2eeada3abc825bb4b5073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930324"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a>Proprietà IWMPClosedCaption::SAMIFileName

La **proprietà SAMIFileName** ottiene o imposta il nome di un file contenente le informazioni necessarie per i sottotitoli codificati.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a>Valore proprietà

**System.String che** rappresenta il nome del file SAMI (Synchronized Accessible Media Interchange).

## <a name="remarks"></a>Commenti

Il file SAMI deve usare un'estensione SMI o SAMI.

Se non si imposta un valore usando **SAMIFileName,** questa proprietà ottiene una stringa contenente il nome file predefinito o l'URL associato all'elemento multimediale corrente.  Questa associazione può verificarsi quando un file SAMI viene specificato usando il parametro *URL sami* o automaticamente quando il file SAMI ha lo stesso nome del file multimediale digitale (ad eccezione dell'estensione del nome file). Se al supporto corrente non è associato alcun file SAMI predefinito, questa proprietà ottiene una stringa di lunghezza zero ("").

Dopo aver impostato un valore usando **SAMIFileName**, tale valore viene mantenuto fino a quando non si imposta un nuovo valore (o fino a quando non viene aperto un nuovo elemento multimediale usando il parametro URL sami). Pertanto, è necessario impostare un nuovo valore per questa proprietà prima di riprodurre ogni nuovo elemento multimediale. In questo modo, il nuovo valore per **SAMIFileName** avrà effetto all'apertura del successivo elemento multimediale (o quando viene chiamato **AxWindowsMediaPlayer.close).** La specifica di un nuovo valore **per SAMIFileName** non ha alcun effetto per il supporto corrente.

Per fare Windows Media Player utilizzare il file SAMI predefinito associato a un particolare elemento multimediale, impostare **SAMIFileName** su una stringa di lunghezza zero ("") prima di riprodurre l'elemento multimediale successivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di sottotitoli codificati a supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**AxWindowsMediaPlayer.close**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





