---
title: Elemento STARTMARKER
description: L'elemento STARTMARKER specifica un marcatore dal quale Windows Media Player avvierà il rendering del flusso.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Finestra elementi STARTMARKER Media Player
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331734"
---
# <a name="startmarker-element"></a>Elemento STARTMARKER

L'elemento **STARTMARKER** specifica un marcatore dal quale Windows Media Player avvierà il rendering del flusso.

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Attributi

**NUMERO**

Numero di un marcatore numerico nell'indice. Il valore predefinito è l'inizio del contenuto su richiesta o la posizione corrente in un flusso in tempo reale.

**NOME**

Nome di un marcatore denominato nell'indice. Il valore predefinito è l'inizio del contenuto su richiesta o la posizione corrente in un flusso in tempo reale.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **voce**, **ref** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento specifica il marcatore da cui Windows Media Player deve avviare il rendering del flusso definito nella **voce** padre o nell'elemento **ref** .

**Nota**

Usare questo elemento con l'attributo **Number** o **Name** , ma non con entrambi.

Un elemento **STARTMARKER** definito all'interno di un elemento **ref** ha la precedenza su un elemento **STARTMARKER** definito all'interno dell'elemento **entry** padre dell'elemento **ref** . Un elemento **STARTMARKER** ha anche la precedenza su un elemento **StartTime** .

Se il marcatore specificato da un elemento **STARTMARKER** si trova in un secondo momento nel flusso rispetto al marcatore definito da un elemento **ENDMARKER** , nessun contenuto viene riprodotto, ma non viene generato alcun errore.

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

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





