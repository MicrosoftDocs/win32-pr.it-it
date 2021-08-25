---
title: Elemento DURATION
description: L'elemento DURATION definisce l'intervallo di tempo Windows Media Player eseguirà il rendering della voce della playlist associata.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Elemento DURATION Windows Media Player
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b06b497a6d31b03c4cbec23748f6995a1382fb806ad18fabaa542ed8ff33e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863351"
---
# <a name="duration-element"></a>Elemento DURATION

**L'elemento DURATION** definisce l'intervallo di tempo Windows Media Player eseguirà il rendering della voce della playlist associata.

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attributi

**VALUE** (obbligatorio)

Periodo di tempo, in ore, minuti, secondi e centesimi di secondo, di cui viene eseguito il rendering di una voce Windows Media Player. Il valore predefinito è l'intera lunghezza della voce. Se la voce è un file grafico, è necessario specificare un valore di durata.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **ENTRY**, **REF** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento definisce la durata del rendering di un flusso. Se **l'attributo VALUE** supera la lunghezza del flusso di contenuto, il flusso termina al punto finale normale.

Questo elemento può essere visualizzato all'interno di un **elemento REF** o all'interno di un **elemento ENTRY.** Tuttavia, un **elemento DURATION** definito all'interno di un **elemento REF** ne esegue l'override all'interno dell'elemento **ENTRY** padre dell'elemento **REF.**

**L'elemento DURATION** esegue l'override **di un elemento PREVIEWDURATION.**

## <a name="examples"></a>Esempio


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Windows Informazioni di riferimento su elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





