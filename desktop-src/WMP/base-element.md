---
title: Elemento di BASE
description: L'elemento di BASE definisce una stringa URL aggiunta all'inizio degli URL inviati a Windows Media Player.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- Windows elemento di BASE Media Player
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331018"
---
# <a name="base-element"></a>Elemento di BASE

L'elemento di **base** definisce una stringa URL aggiunta all'inizio degli URL inviati a Windows Media Player.

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attributi

**Href** (obbligatorio)

Stringa accodata all'inizio degli URL inviati a Windows Media Player. Il valore predefinito è la stringa null ("").

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **ASX**, **voce** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento definisce una stringa URL aggiunta all'inizio degli URL di capovolgimento URL inviati a Windows Media Player. Il capovolgimento degli URL è un meccanismo di script che consente a Windows Media Player di aprire un nuovo URL in un browser o in un frame del browser quando riceve un comando per script.

L'elemento di **base** è simile a una home directory per i collegamenti relativi. Influiscono solo sugli URL inviati usando i comandi script come parte del flusso di contenuto che viene riprodotto in Windows Media Player.

Un elemento di **base** definito come figlio di un elemento **ASX** diventa l'impostazione predefinita per l'intero metafile. Un elemento di **base** definito in un elemento **entry** esegue l'override di qualsiasi elemento di **base** nell'elemento **ASX** padre (solo per tale elemento **entry** ).

> [!Note]  
> Se l'attributo **href** non termina con un carattere/, Windows Media Player ne aggiunge uno alla fine della stringa.

 

## <a name="examples"></a>Esempio


```XML
<BASE HREF="https://msdn.microsoft.com/" />

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

 

 





