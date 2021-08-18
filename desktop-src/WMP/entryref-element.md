---
title: Elemento ENTRYREF
description: L'elemento ENTRYREF punta agli elementi ENTRY in un metafile esterno.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Elemento ENTRYREF Windows Media Player
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61fa3403fc56c6a02f97330b3c2f62d1c3e3c723f50672520ea42fb4a2018705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996671"
---
# <a name="entryref-element"></a>Elemento ENTRYREF

**L'elemento ENTRYREF** punta agli **elementi ENTRY** in un metafile esterno.

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attributi

**HREF** (obbligatorio)

URL di un metafile di riferimento.

**CLIENTBIND**

Questo attributo non è più supportato.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                       |
|-----------------|--------------------------------|
| Elementi padre | **ASX**, **EVENT**, **REPEAT** |
| Elementi figlio  | nessuno                           |



 

## <a name="remarks"></a>Osservazioni

Questo elemento punta al contenuto di un metafile esterno. Windows Media Player elabora gli elementi **ENTRY** del metafile di riferimento come se fossero inclusi nel metafile primario nella posizione dell'elemento **ENTRYREF.** Ignora tuttavia tutti gli elementi **ENTRY** nel metafile a cui si fa riferimento con l'attributo **SKIPIFREF** impostato su YES.

Windows Media Player 7.0, 7.1 e Windows Media Player per Windows XP ignorano tutti gli elementi **ENTRYREF** nel metafile di riferimento. Di conseguenza, i metafile possono essere annidati solo a un livello di profondità quando si usano queste versioni del lettore. Windows Media Player inoltre ignora **l'elemento ASX** nel file di riferimento insieme ai relativi attributi. Windows Media Player serie 9 o versioni successive supporta l'annidamento di metafile fino a cinque livelli di profondità.

L'URL specificato **nell'attributo HREF** diventa l'URL di base per tutti gli URL relativi nel metafile esterno. Questo URL viene usato quando viene riprodotta una voce dal metafile esterno e l'utente la aggiunge alla libreria.

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

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





