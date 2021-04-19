---
title: Elemento COPYRIGHT (msfeeds. h)
description: L'elemento COPYRIGHT definisce una stringa di testo che specifica le informazioni sul copyright per un elemento ASX o ENTRY.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Elemento COPYRIGHT Windows Media Player
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b757528cfb14a01854346854a342ee9faced65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330117"
---
# <a name="copyright-element"></a>COPYRIGHT (elemento)

L'elemento **Copyright** definisce una stringa di testo che specifica le informazioni sul copyright per un elemento **ASX** o **entry** .

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **ASX**, **voce** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento definisce una stringa di testo che specifica le informazioni sul copyright per un elemento **ASX** o **entry** .

Quando questo elemento viene visualizzato all'interno di un elemento **ASX** , la stringa di copyright viene visualizzata solo come **Mostra** informazioni. Quando questo elemento viene visualizzato all'interno di un elemento **entry** , il testo viene visualizzato come informazioni di ritaglio. Ogni elemento **ASX** e **entry** padre deve contenere al massimo un elemento **Copyright** figlio. Più elementi di **Copyright** dopo il primo verranno ignorati e non verranno visualizzati.

I caratteri per il copyright e i simboli di registrazione dei marchi (o) potrebbero non essere visualizzati correttamente se il metafile non è codificato con lo schema di codifica UTF-8. In questo caso, per visualizzare correttamente uno di questi simboli per tutti gli utenti, è invece possibile usare gli equivalenti ASCII (c) e (R).

Se il metafile è codificato con UTF-8, i simboli del copyright e dei marchi vengono visualizzati correttamente.

## <a name="examples"></a>Esempio


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/>                                 |
| Intestazione<br/>  | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di caratteri di copyright a metafile**](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





