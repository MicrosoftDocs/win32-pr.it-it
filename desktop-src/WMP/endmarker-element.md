---
title: Elemento ENDMARKER
description: L'elemento ENDMARKER specifica un marcatore in corrispondenza del quale Windows Media Player arresterà il rendering del flusso.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- Finestra elementi ENDMARKER Media Player
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94d00eae3681775476af9c3169134b636e2904c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333247"
---
# <a name="endmarker-element"></a>Elemento ENDMARKER

L'elemento **ENDMARKER** specifica un marcatore in corrispondenza del quale Windows Media Player arresterà il rendering del flusso.

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Attributi

**NUMERO**

Numero di un marcatore numerico nell'indice. Il valore predefinito è la fine del contenuto.

**NOME**

Nome di un marcatore denominato nell'indice. Il valore predefinito è la fine del contenuto.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **voce**, **ref** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento specifica il marcatore in cui Windows Media Player sta per arrestare il rendering del flusso definito nella **voce** padre o nell'elemento **ref** .

Nota

Usare l'elemento **ENDMARKER** con l'attributo **Number** o **Name** , ma non con entrambi.

In modalità di anteprima, il raggiungimento di un marcatore finale interrompe l'anteprima, anche se non è trascorso il tempo specificato dall'elemento **PREVIEWDURATION** . L'elemento **ENDMARKER** ha anche la precedenza sull'elemento **Duration** .

Un elemento **ENDMARKER** definito all'interno di un elemento **ref** ha la precedenza su un **ENDMARKER** definito all'interno dell'elemento **entry** padre dell'elemento **ref** .

Se il marcatore specificato da un elemento **ENDMARKER** si verifica in precedenza nel flusso rispetto al marcatore definito da un elemento **STARTMARKER** , nessun contenuto viene riprodotto, ma non viene generato alcun errore.

## <a name="examples"></a>Esempio


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

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

 

 





