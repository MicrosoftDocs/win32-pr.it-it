---
title: Proprietà SAMIFileName di IWMPClosedCaption
description: La proprietà SAMIFileName Ottiene o imposta il nome di un file contenente le informazioni necessarie per la didascalia chiusa.
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Finestra delle proprietà di SAMIFileName Media Player
- Proprietà di SAMIFileName Media Player Windows, interfaccia IWMPClosedCaption
- Interfaccia IWMPClosedCaption Windows Media Player, proprietà SAMIFileName
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
ms.openlocfilehash: d251f2bbf0c8839ab9a0005c69e1869c47af16ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329283"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a>Proprietà IWMPClosedCaption:: SAMIFileName

La proprietà **SAMIFileName** Ottiene o imposta il nome di un file contenente le informazioni necessarie per la didascalia chiusa.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a>Valore proprietà

**System. String** che rappresenta il nome del file di Media Interchange accessibile sincronizzato (Sami).

## <a name="remarks"></a>Commenti

Il file SAMI deve usare un'estensione del nome file. SMI o. Sami.

Se non si imposta un valore utilizzando **SAMIFileName**, questa proprietà ottiene una **stringa** contenente il nome file o l'URL predefinito associato all'elemento multimediale corrente. Questa associazione può verificarsi quando un file SAMI viene specificato tramite il parametro dell'URL *Sami* oppure automaticamente quando il file Sami ha lo stesso nome del file multimediale digitale, ad eccezione dell'estensione del nome file. Se al supporto corrente non è associato alcun file SAMI predefinito, questa proprietà ottiene una stringa di lunghezza zero ("").

Quando si imposta un valore usando **SAMIFileName**, tale valore viene mantenuto fino a quando non si imposta un nuovo valore (o fino a quando non viene aperto un nuovo elemento multimediale usando il parametro dell'URL Sami). Pertanto, è necessario impostare un nuovo valore per questa proprietà prima di riprodurre ogni nuovo elemento multimediale. In questo modo, il nuovo valore di **SAMIFileName** verrà applicato quando viene aperto il successivo elemento multimediale (o quando viene chiamato **AxWindowsMediaPlayer. Close** ). La specifica di un nuovo valore per **SAMIFileName** non ha alcun effetto sui supporti correnti.

Per fare in modo che Windows Media Player usi il file SAMI predefinito associato a un particolare elemento multimediale, impostare **SAMIFileName** su una stringa di lunghezza zero ("") prima di riprodurre il successivo elemento multimediale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di didascalie chiuse a file multimediali digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**AxWindowsMediaPlayer. Close**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





