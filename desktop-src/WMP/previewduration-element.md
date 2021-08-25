---
title: Elemento PREVIEWDURATION
description: L'elemento PREVIEWDURATION definisce il periodo di tempo per cui un clip viene riprodotto in modalità di anteprima.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- Elemento PREVIEWDURATION Windows Media Player
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd01180b56816aa3458396f1c6183518d4365dce2f41643328e899057ed1ee72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862021"
---
# <a name="previewduration-element"></a>Elemento PREVIEWDURATION

**L'elemento PREVIEWDURATION** definisce il periodo di tempo per cui un clip viene riprodotto in modalità di anteprima.

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attributi

**VALUE** (obbligatorio)

Periodo di tempo (in ore, minuti, secondi e centesimi di secondo) di riproduzione del clip in modalità di anteprima.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                    |
|-----------------|-----------------------------|
| Elementi padre | **ASX,** **ENTRY,** **REF** |
| Elementi figlio  | nessuno                        |



 

## <a name="remarks"></a>Osservazioni

Questo elemento definisce il periodo di tempo per cui un clip viene riprodotto in modalità di anteprima. Se questo elemento viene visualizzato **all'interno** di un elemento ENTRY o **REF,** si applica alla clip definita da tale elemento. Se viene visualizzato nell'ambito di un **elemento ASX,** viene applicato a ogni clip nel metafile. Un **elemento PREVIEWDURATION** in un elemento **REF** ha la precedenza su uno in un elemento **ENTRY** e ha la precedenza su un elemento **PREVIEWDURATION** in un **elemento ASX.** Se per un clip non è definito alcun elemento **PREVIEWDURATION,** il tempo di anteprima predefinito è 10 secondi.

Se è presente un **elemento STARTTIME** o **STARTMARKER** per il clip, Windows Media Player esegue il rendering della clip a partire dal punto definito da uno di questi elementi; in caso contrario, viene eseguito il rendering dall'inizio del clip. Il clip si arresta normalmente se è più breve dell'ora definita **dall'elemento PREVIEWDURATION.**

**L'elemento DURATION** esegue l'override **di un elemento PREVIEWDURATION.**

## <a name="examples"></a>Esempio


```XML
<PREVIEWDURATION VALUE="0:30.0" />
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------|
| Versione<br/> | Windows Media Player versione 70 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





