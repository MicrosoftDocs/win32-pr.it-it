---
title: ClosedCaption.SAMIFileName
description: La proprietà SAMIFileName specifica o Recupera il nome del file contenente le informazioni necessarie per la didascalia chiusa.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- Media Player Windows ClosedCaption. SAMIFileName
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
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326732"
---
# <a name="closedcaptionsamifilename"></a>ClosedCaption.SAMIFileName

La proprietà **SAMIFileName** specifica o Recupera il nome del file contenente le informazioni necessarie per la didascalia chiusa.

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Il file di interscambio multimediale accessibile sincronizzato (SAMI) deve usare un'estensione del nome file. SMI o. Sami.

Se non si specifica un valore per **SAMIFileName**, questa proprietà recupera una stringa contenente il nome file o l'URL associato all'elemento multimediale corrente. Questa associazione può verificarsi quando un file SAMI viene specificato con il parametro dell'URL *Sami* oppure automaticamente quando il file Sami ha lo stesso nome del file multimediale digitale, ad eccezione dell'estensione del nome file. Se al supporto corrente non è associato alcun file SAMI, questa proprietà recupera una stringa vuota ("").

Quando si specifica un valore per **SAMIFileName**, tale valore viene mantenuto fino a quando non si specifica un nuovo valore o finché non viene aperto un nuovo elemento multimediale con il parametro *Sami* URL. Pertanto, è necessario specificare un nuovo valore per questa proprietà prima di riprodurre ogni nuovo elemento multimediale. In questo modo, il nuovo valore di **SAMIFileName** verrà applicato quando viene aperto il successivo elemento multimediale (o quando il *lettore*.**Close** viene chiamato). La specifica di un nuovo valore per **SAMIFileName** non ha alcun effetto sui supporti correnti.

Per fare in modo che Windows Media Player ritorni a utilizzando il file SAMI associato a un particolare elemento multimediale, specificare un valore per **SAMIFileName** uguale a una stringa vuota ("") prima di riprodurre il successivo elemento multimediale.

**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura e restituisce sempre una stringa vuota.

## <a name="examples"></a>Esempio

Nei tre esempi di JScript seguenti viene utilizzato *ClosedCaption*. **SAMIFileName** per specificare il nome di un file di testo del titolo chiuso. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di didascalie chiuse a file multimediali digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Oggetto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**Player. Close**](player-close.md)
</dt> </dl>

 

 





