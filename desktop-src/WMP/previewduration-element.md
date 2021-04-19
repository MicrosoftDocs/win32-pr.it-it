---
title: Elemento PREVIEWDURATION
description: L'elemento PREVIEWDURATION definisce l'intervallo di tempo in cui una clip viene riprodotta in modalità di anteprima.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- Finestra elementi PREVIEWDURATION Media Player
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a944e86a4bd82bf57961d4d6b474c34afadba6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325991"
---
# <a name="previewduration-element"></a>Elemento PREVIEWDURATION

L'elemento **PREVIEWDURATION** definisce l'intervallo di tempo in cui una clip viene riprodotta in modalità di anteprima.

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attributi

**Valore** (obbligatorio)

Periodo di tempo (in ore, minuti, secondi e centesimi di secondo) in cui il clip viene riprodotto in modalità di anteprima.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                    |
|-----------------|-----------------------------|
| Elementi padre | **ASX**, **entry**, **ref** |
| Elementi figlio  | nessuno                        |



 

## <a name="remarks"></a>Osservazioni

Questo elemento definisce l'intervallo di tempo in cui una clip viene riprodotta in modalità di anteprima. Se questo elemento viene visualizzato all'interno di un elemento **entry** o di un elemento **ref** , si applica alla clip definita da tale elemento. Se viene visualizzato all'interno dell'ambito di un elemento **ASX** , viene applicato a ogni clip del metafile. Un elemento **PREVIEWDURATION** in un elemento **ref** ha la precedenza su uno in un **elemento** entry e ha la precedenza su un elemento **PREVIEWDURATION** in un elemento **ASX** . Se per una clip non è definito alcun elemento **PREVIEWDURATION** , il tempo di anteprima predefinito è di 10 secondi.

Se è presente un elemento **StartTime** o **STARTMARKER** per il clip, Windows Media Player esegue il rendering della clip a partire dal punto definito da uno di questi elementi. in caso contrario, viene eseguito il rendering dall'inizio della clip. Il clip si interrompe normalmente se è più breve del tempo definito dall'elemento **PREVIEWDURATION** .

L'elemento **Duration** esegue l'override di un elemento **PREVIEWDURATION** .

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

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





