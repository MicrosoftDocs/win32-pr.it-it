---
title: ClosedCaption.SAMIFileName
description: La proprietà SAMIFileName specifica o recupera il nome del file contenente le informazioni necessarie per i sottotitoli codificati.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- ClosedCaption.SAMIFileName Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ba314208db3cb5529042011f269f026a4cf2bd4d4b01d1b8d64719b96a5f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119512"
---
# <a name="closedcaptionsamifilename"></a>ClosedCaption.SAMIFileName

La **proprietà SAMIFileName** specifica o recupera il nome del file contenente le informazioni necessarie per i sottotitoli codificati.

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

Il file SAMI (Synchronized Accessible Media Interchange) deve usare un'estensione SMI o SAMI.

Se non si specifica un valore per **SAMIFileName,** questa proprietà recupera una stringa contenente il nome file o l'URL associato all'elemento multimediale corrente. Questa associazione può verificarsi quando un file SAMI viene specificato utilizzando il parametro URL *sami* o automaticamente quando il file SAMI ha lo stesso nome del file multimediale digitale (ad eccezione dell'estensione del nome file). Se al supporto corrente non è associato alcun file SAMI, questa proprietà recupera una stringa vuota ("").

Dopo aver specificato un valore per **SAMIFileName**, tale valore viene mantenuto fino a quando non si specifica un nuovo valore (o finché non viene aperto un nuovo elemento multimediale usando il *parametro URL sami).* Pertanto, è necessario specificare un nuovo valore per questa proprietà prima di riprodurre ogni nuovo elemento multimediale. In questo modo, il nuovo valore per **SAMIFileName** avrà effetto all'apertura dell'elemento multimediale successivo (o quando *Player*.**viene chiamato close).** La specifica di un nuovo valore **per SAMIFileName** non ha alcun effetto per il supporto corrente.

Per fare Windows Media Player a utilizzando il file SAMI associato a un particolare elemento multimediale, specificare un valore per **SAMIFileName** uguale a una stringa vuota ("") prima di riprodurre l'elemento multimediale successivo.

**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura e restituisce sempre una stringa vuota.

## <a name="examples"></a>Esempio

I tre esempi JScript usano *ClosedCaption*. **SAMIFileName per** specificare il nome di un file di testo di sottotitoli codificati. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di sottotitoli codificati a supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Oggetto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**Player.close**](player-close.md)
</dt> </dl>

 

 





