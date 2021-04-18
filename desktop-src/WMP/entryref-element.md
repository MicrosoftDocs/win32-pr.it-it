---
title: Elemento ENTRYREF
description: L'elemento ENTRYREF punta agli elementi ENTRY in un metafile esterno.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Finestra elementi ENTRYREF Media Player
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325254"
---
# <a name="entryref-element"></a>Elemento ENTRYREF

L'elemento **ENTRYREF** punta agli elementi **entry** in un metafile esterno.

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attributi

**Href** (obbligatorio)

URL di un metafile a cui si fa riferimento.

**CLIENTBIND**

Questo attributo non è più supportato.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                       |
|-----------------|--------------------------------|
| Elementi padre | **ASX**, **evento**, **ripetizione** |
| Elementi figlio  | nessuno                           |



 

## <a name="remarks"></a>Osservazioni

Questo elemento punta al contenuto di un metafile esterno. Windows Media Player elabora gli elementi **voce** del metafile a cui si fa riferimento come se fossero inclusi nel metafile primario nella posizione dell'elemento **ENTRYREF** . Tuttavia, ignora qualsiasi elemento **entry** nel metafile a cui si fa riferimento con l'attributo **SKIPIFREF** impostato su Yes.

Windows Media Player 7,0, 7,1 e Windows Media Player per Windows XP ignorano tutti gli elementi **ENTRYREF** nel metafile a cui si fa riferimento. Di conseguenza, i metafile possono essere annidati solo a livello profondo quando si usano queste versioni del lettore. Windows Media Player ignora anche l'elemento **ASX** nel file a cui si fa riferimento insieme ai relativi attributi. Windows Media Player 9 Series o versioni successive supporta la nidificazione di metafile fino a cinque livelli di profondità.

L'URL specificato nell'attributo **href** diventa l'URL di base per qualsiasi URL relativo nel metafile esterno. Questo URL viene usato quando una voce del metafile esterno viene riprodotta e l'utente la aggiunge alla libreria.

## <a name="examples"></a>Esempio


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
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

 

 





