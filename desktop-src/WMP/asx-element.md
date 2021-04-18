---
title: Elemento ASX
description: L'elemento ASX definisce un file come metafile.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Windows elemento ASX Media Player
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331404"
---
# <a name="asx-element"></a>Elemento ASX

L'elemento **ASX** definisce un file come metafile.

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

Numero decimale che rappresenta il numero di versione della sintassi per il metafile. Impostare su 3 o 3,0.

**PREVIEWMODE** (facoltativo)

Valore che indica se Windows Media Player passa alla modalità di anteprima prima di riprodurre il primo clip.

Deve essere uno dei valori seguenti.



| Valore | Descrizione                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| YES   | Windows Media Player passa alla modalità di anteprima prima di riprodurre il primo clip.                            |
| NO    | Il valore predefinito. Windows Media Player non entra in modalità di anteprima prima di riprodurre il primo clip. |



 

**BANNERBAR** (facoltativo)

Valore che indica se Windows Media Player riserva spazio per una rappresentazione grafica del banner.

Deve essere uno dei valori seguenti.



| Valore | Descrizione                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| AUTO  | Il valore predefinito. Windows Media Player riserva spazio per la barra del banner solo quando una parte di contenuto ne include una.                       |
| FIXED | Windows Media Player riserva uno spazio fisso per un grafico banner per ogni parte di contenuto riprodotta, a prescindere dal fatto che sia presente un banner associato. |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre | Nessuna. L'elemento **ASX** deve essere il primo elemento di ogni metafile.                                                                                                 |
| Elementi figlio  | **abstract**, **Author**, **banner**, **base**, **Copyright**, **entry**, **ENTRYREF**, **Event**, **moreinfo**, **PREVIEWDURATION**, **param**, **Repeat**, **title** |



 

## <a name="remarks"></a>Commenti

I primi quattro caratteri di una playlist di metafile devono essere "<ASX". Gli altri elementi definiti nell'ambito dell'elemento **ASX** , ad esempio **titolo** e **autore**, sono associati alle informazioni di visualizzazione visualizzate da Windows Media Player.

Per Windows Media Player, il numero di versione della sintassi è 3,0. Windows Media Player supporta tutte le versioni precedenti della sintassi del metafile. I valori accettabili per l'attributo **Version** includono sia 3,0 che 3 (senza virgola decimale).

Se il valore dell'attributo **PREVIEWMODE** è sì, Windows Media Player passa immediatamente alla modalità di anteprima prima di riprodurre il primo clip. Quando Windows Media Player passa alla modalità di anteprima, Visualizza in anteprima ogni clip a cui viene fatto riferimento nel metafile. L'elemento **PREVIEWDURATION** determina la durata di ogni anteprima.

L'attributo **BANNERBAR** definisce se Windows Media Player riserva spazio per una rappresentazione grafica del banner. Un banner è un grafico che viene visualizzato nell'area di visualizzazione del video mentre viene riprodotto il contenuto multimediale. (Usare l'elemento **banner** per aggiungere un banner al contenuto). Se il valore di **BANNERBAR** è fisso, Windows Media Player riserva lo spazio del banner per ogni contenuto multimediale, indipendentemente dal fatto che il contenuto multimediale includa un banner. Se a un contenuto multimediale non è associato alcun banner, lo spazio riservato per uno è nero. Se il valore dell'attributo **BANNERBAR** è auto, Windows Media Player riserva spazio per il banner solo quando il contenuto multimediale ne include uno.

Se si crea un metafile con più clip (elementi **entry** o **ENTRYREF** ) e si imposta il valore dell'attributo **BANNERBAR** su auto, Windows Media Player potrebbe essere ridimensionato in modo da consentire lo spazio per un'immagine del banner per un clip e quindi ridimensionarlo nuovamente se il clip successivo non contiene una rappresentazione grafica del banner. Se si desidera che la dimensione della finestra resti invariata (tranne quando le dimensioni del video cambiano), utilizzare il valore fisso per l'attributo **BANNERBAR** .

Lo spazio riservato per una rappresentazione grafica del banner è 32 pixel di altezza di 194 pixel di larghezza. Lo spazio riservato viene visualizzato al di sotto di qualsiasi contenuto video di cui è stato eseguito il rendering e 6 pixel sopra il bordo inferiore dell'area video, consentendo lo spazio per il bordo dell'area video a 6 pixel. Lo spazio del banner riservato viene centrato orizzontalmente.

Windows Media Player esegue il rendering dell'elemento grafico a partire dal pixel più a sinistra dello spazio del banner. Se il grafico riempie l'intero spazio, verrà visualizzato al centro orizzontalmente. In caso contrario, sarà presente uno spazio finale. Si noti che la larghezza minima di Windows Media Player è sempre più ampia della dimensione del clip video, indipendentemente dal valore dell'attributo **BANNERBAR** .

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

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





