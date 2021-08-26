---
title: Elemento ASX
description: L'elemento ASX definisce un file come metafile.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Elemento ASX Windows Media Player
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 509cdbc25c57c6d0b556433c3bee8b1e68083248c8356769a31529b83c2df1f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902830"
---
# <a name="asx-element"></a>Elemento ASX

**L'elemento ASX** definisce un file come metafile.

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a>Attributi

`VERSION` (obbligatorio)

Numero decimale che rappresenta il numero di versione della sintassi per il metafile. Impostare su 3 o 3.0.

**PREVIEWMODE** (facoltativo)

Valore che indica se Windows Media Player attiva la modalità di anteprima prima di riprodurre il primo clip.

Deve essere uno dei valori seguenti.



| Valore | Descrizione                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| YES   | Windows Media Player la modalità di anteprima prima di riprodurre il primo clip.                            |
| NO    | Il valore predefinito. Windows Media Player non entra nella modalità di anteprima prima di riprodurre il primo clip. |



 

**BANNERBAR** (facoltativo)

Valore che indica se Windows Media Player spazio per un'immagine del banner.

Deve essere uno dei valori seguenti.



| Valore | Descrizione                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| AUTO  | Il valore predefinito. Windows Media Player spazio per la barra del banner solo quando una parte di contenuto ne include una.                       |
| FIXED | Windows Media Player riserva uno spazio fisso per un'immagine del banner per ogni contenuto riprodotto, indipendentemente dal fatto che sia presente un banner associato. |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre | Nessuno. **L'elemento ASX** deve essere il primo elemento in ogni metafile.                                                                                                 |
| Elementi figlio  | **ABSTRACT,** **AUTHOR,** **BANNER,** **BASE,** **COPYRIGHT,** **ENTRY,** **ENTRYREF,** **EVENT,** **MOREINFO,** **PREVIEWDURATION,** **PARAM,** **REPEAT,** **TITLE** |



 

## <a name="remarks"></a>Commenti

I primi quattro caratteri di una playlist di metafile devono essere "<ASX". Altri elementi definiti nell'ambito dell'elemento **ASX,** ad esempio **TITLE** e **AUTHOR,** sono associati alle informazioni di visualizzazione visualizzate da Windows Media Player.

Ad Windows Media Player, il numero di versione della sintassi è 3.0. Windows Media Player supporta tutte le versioni precedenti della sintassi dei metafile. I valori accettabili per **l'attributo VERSION** includono sia 3.0 che 3 (senza separatore decimale).

Se il valore **dell'attributo PREVIEWMODE** è YES, Windows Media Player attiva immediatamente la modalità di anteprima prima di riprodurre il primo clip. Quando Windows Media Player attiva la modalità di anteprima, visualizza in anteprima ogni clip a cui viene fatto riferimento nel metafile. **L'elemento PREVIEWDURATION** determina la durata di ogni anteprima.

**L'attributo BANNERBAR** definisce se Windows Media Player riserva spazio per un'immagine banner. Un banner è un elemento grafico visualizzato nell'area di visualizzazione video durante la riproduzione del contenuto multimediale. Usare **l'elemento BANNER** per aggiungere un banner al contenuto. Se il valore di **BANNERBAR** è FIXED, Windows Media Player spazio del banner per ogni contenuto multimediale, indipendentemente dal fatto che il contenuto multimediale abbia un banner. Se a una parte di contenuto multimediale non è associato un banner, lo spazio riservato per uno è nero. Se il valore **dell'attributo BANNERBAR** è AUTO, Windows Media Player spazio per il banner solo quando il contenuto multimediale ne include uno.

Se si crea un metafile con più clip (elementi **ENTRY** o **ENTRYREF)** e si imposta il valore dell'attributo **BANNERBAR** su AUTO, Windows Media Player potrebbe ridimensionare per consentire lo spazio per un'immagine banner per un clip e quindi ridimensionare di nuovo se il clip successivo non contiene un'immagine banner. Se si vuole che le dimensioni della finestra rimangano le stesse (tranne quando le dimensioni del video cambiano), usare il valore FIXED per **l'attributo BANNERBAR.**

Lo spazio riservato per un'immagine banner è alto 32 pixel per 194 pixel. Lo spazio riservato viene visualizzato sotto qualsiasi contenuto video sottoposto a rendering e 6 pixel sopra il bordo inferiore dell'area video, consentendo lo spazio per il bordo dell'area video di 6 pixel. Lo spazio del banner riservato è centrato orizzontalmente.

Windows Media Player esegue il rendering dell'elemento grafico a partire dal pixel più a sinistra dello spazio del banner. Se l'immagine riempie l'intero spazio, verrà visualizzata al centro orizzontalmente. In caso contrario, sarà presente spazio finale. Si noti che la larghezza minima Windows Media Player è sempre più ampia delle dimensioni del clip video, indipendentemente dal valore **dell'attributo BANNERBAR.**

## <a name="examples"></a>Esempio


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------|
| Versione<br/> | Windows Media Player versione 70 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Windows Informazioni di riferimento su elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





