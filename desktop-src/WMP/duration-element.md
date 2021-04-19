---
title: DURATION-elemento
description: L'elemento DURATION definisce l'intervallo di tempo in cui Windows Media Player eseguirà il rendering della voce della playlist associata.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Finestra di Media Player elemento DURATION
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331746"
---
# <a name="duration-element"></a>DURATION-elemento

L'elemento **Duration** definisce l'intervallo di tempo in cui Windows Media Player eseguirà il rendering della voce della playlist associata.

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attributi

**Valore** (obbligatorio)

Periodo di tempo, in ore, minuti, secondi e centesimi di secondo, in base al quale viene eseguito il rendering di una voce da parte di Windows Media Player. Il valore predefinito è l'intera lunghezza della voce. Se la voce è un file grafico, è necessario specificare un valore Duration.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **voce**, **ref** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento definisce l'intervallo di tempo in cui deve essere eseguito il rendering di un flusso. Se l'attributo **value** supera la lunghezza del flusso di contenuto, il flusso termina in corrispondenza del normale endpoint.

Questo elemento può essere presente all'interno di un elemento **ref** o all'interno di un elemento **entry** . Tuttavia, un elemento **Duration** definito all'interno di un elemento **ref** esegue l'override di uno che viene visualizzato all'interno dell'elemento **entry** padre dell'elemento **ref** .

L'elemento **Duration** esegue l'override di un elemento **PREVIEWDURATION** .

## <a name="examples"></a>Esempio


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





