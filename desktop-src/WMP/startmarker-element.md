---
title: Elemento STARTMARKER
description: L'elemento STARTMARKER specifica un marcatore da cui Windows Media Player il rendering del flusso.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Elemento STARTMARKER Windows Media Player
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fa80da249edc4b9e3ab7d8796bc6ff135cb7cfb2b19a1cb11216ebe4a9c122c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123041"
---
# <a name="startmarker-element"></a>Elemento STARTMARKER

**L'elemento STARTMARKER** specifica un marcatore dal quale Windows Media Player inizierà a eseguire il rendering del flusso.

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Attributi

**Numero**

Numero di un marcatore numerico nell'indice. Il valore predefinito è l'inizio del contenuto su richiesta o la posizione corrente in un flusso in tempo reale.

**NOME**

Nome di un marcatore denominato nell'indice. Il valore predefinito è l'inizio del contenuto su richiesta o la posizione corrente in un flusso in tempo reale.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **ENTRY,** **REF** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento specifica il marcatore da Windows Media Player avviare il rendering del flusso definito **nell'elemento ENTRY** o **REF** padre.

**Nota**

Usare questo elemento con **l'attributo NUMBER** **o NAME,** ma non con entrambi.

Un **elemento STARTMARKER** definito all'interno di un elemento **REF** ha la precedenza su un elemento **STARTMARKER** definito all'interno dell'elemento ENTRY padre dell'elemento **REF.**  Un **elemento STARTMARKER** ha anche la precedenza su un **elemento STARTTIME.**

Se il marcatore specificato da un elemento **STARTMARKER** si verifica in un secondo momento nel flusso rispetto al marcatore definito da un elemento **ENDMARKER,** non viene riprodotto alcun contenuto, ma non viene generato alcun errore.

## <a name="examples"></a>Esempio


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
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

 

 





