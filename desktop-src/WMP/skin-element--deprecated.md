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
ms.openlocfilehash: b868b756ed190301c66987b6e26249762bac71842f4a5425d6d7c6d4b16816a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507911"
---
# <a name="skin-element-deprecated"></a>Elemento SKIN (deprecato)

Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.

**L'elemento SKIN** specifica un URL per un bordo.

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attributi

**HREF** (obbligatorio)

URL per un file con bordo compresso con estensione wmz. Per Windows Media Player serie 9 o successive, questo valore può fare riferimento solo ai file di bordo sul disco rigido dell'utente che si trovano nella stessa directory della playlist del metafile. Vedere il codice di esempio.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi |
|-----------------|----------|
| Elementi padre | **Asx**  |
| Elementi figlio  | nessuno     |



 

## <a name="remarks"></a>Osservazioni

**L'elemento SKIN** viene usato per creare un bordo, simile a un'interfaccia, ma visualizzato nell'area  In riproduzione dell'interfaccia Windows Media Player. **L'elemento SKIN** viene usato solo per i bordi, che vengono visualizzati all'interno della modalità Windows Media Player, e non per le normali skin, che sostituiscono completamente la modalità compatta Windows Media Player.

In un Windows di download multimediale (con estensione wmd), l'elemento **SKIN** consente a un bordo di avere contenuto e di collegarsi ad altri siti. Il Windows di download multimediale è un file compresso che contiene un file di bordo e un metafile Windows media. Il file di bordo (con estensione wmz) è compresso e include un file di definizione dell'interfaccia (con estensione wms).

Un **elemento SKIN** ha tre componenti:

-   Un'interfaccia
-   Alcuni contenuti
-   Metafile

Le skin incluse in Windows di download dei supporti devono avere una forma rettangolare. La creazione di bordi con skin non rettangolari può produrre risultati imprevisti.

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

[**Windows Informazioni di riferimento su elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





