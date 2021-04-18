---
title: Elemento SKIN (deprecato)
description: Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Elemento SKIN (deprecato) Windows Media Player
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329915"
---
# <a name="skin-element-deprecated"></a>Elemento SKIN (deprecato)

Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.

L'elemento **Skin** specifica un URL per un bordo.

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attributi

**Href** (obbligatorio)

URL per un file di bordo compresso con estensione WMZ. Per Windows Media Player 9 serie o versioni successive, questo valore può fare riferimento solo ai file di bordo nel disco rigido dell'utente che si trova nella stessa directory della playlist del metafile. Vedere il codice di esempio.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi |
|-----------------|----------|
| Elementi padre | **ASX**  |
| Elementi figlio  | nessuno     |



 

## <a name="remarks"></a>Osservazioni

L'elemento **Skin** viene usato per creare un bordo, che è simile a un oggetto Skin, ma viene visualizzato nell'area **Now Play** della modalità Full Windows Media Player. L'elemento **Skin** viene usato solo per i bordi, che vengono visualizzati all'interno del Media Player di Windows in modalità completa e non per le interfacce normali, che sostituiscono completamente le Media Player di Windows in modalità compatta.

In un pacchetto di download di Windows Media (con estensione di file WMD), l'elemento **Skin** Abilita un bordo per il contenuto e il collegamento ad altri siti. Il pacchetto di download di Windows Media è un file compresso che contiene un file di bordo e un metafile di Windows Media. Il file del bordo (con estensione WMZ) viene compresso e include un file di definizione dell'interfaccia (con estensione WMS).

Un elemento **Skin** è costituito da tre componenti:

-   Interfaccia personalizzata
-   Contenuto
-   Un metafile

Le interfacce incluse nei pacchetti di download di Windows Media devono essere rettangolari in forma. La creazione di bordi con interfacce che non sono rettangolari può produrre risultati imprevisti.

## <a name="examples"></a>Esempio


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------|
| Versione<br/> | Windows Media Player versione 70 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Bordi per Windows Media Player (deprecato)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





