---
title: Recupero dei metadati
description: Recupero dei metadati
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Playlist Windows Media Metafile, recupero di metadati
- playlist, recupero di metadati
- playlist di metafile, recupero di metadati
- Playlist Windows Media Metafile, recupero di metadati
- playlist, recupero di metadati
- playlist di metafile, recupero di metadati
- metadati, recupero
- recupero di metadati
- Media Player di Windows, recupero di metadati
- Media Player di Windows, recupero di metadati
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c9855ec1dc95a52429561e91aa82abdac088523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955610"
---
# <a name="retrieving-metadata"></a>Recupero dei metadati

Durante la riproduzione di una visualizzazione o di una clip, lo script può recuperare i metadati, ad esempio il titolo e l'autore, usando i metodi **GetItemInfo** degli oggetti Windows Media Player **media** e **playlist** . È possibile recuperare i metadati dall'ambito ASX usando i metodi dell'oggetto **playlist** e dall'ambito della voce usando i metodi dell'oggetto **multimediale** .

Ad esempio, per recuperare i valori per AUTHOR, ABSTRACT e PARAM nel file seguente, usare il metodo **GetItemInfo** dell'oggetto **playlist** . Il nome dell'attributo è obbligatorio per questo metodo. I nomi degli attributi possono essere ottenuti specificando il numero di indice per la proprietà **attributeName** . Gli indici disponibili per un oggetto **playlist** possono essere ottenuti usando la proprietà **attributeCount** .

## <a name="example-code"></a>Codice di esempio


```XML

    <ASX version="3.0">
        <AUTHOR>My Talking File</AUTHOR>
        <ABSTRACT>Talking File Album</ABSTRACT>
        <PARAM name="one" value="111"/>
        <ENTRY>
            <REF href="Artists_Only.wma"/>
            <TITLE>Artists Only</TITLE>
            <COPYRIGHT>2000</COPYRIGHT>
            <PARAM name="three" value="333"/>
        </ENTRY>
        <PARAM name="two" value="222"/>
    </ASX>
    

```



Per recuperare i valori dell'oggetto **multimediale** corrente nell'ambito della voce per ref, title, copyright e Param ("Three"), usare la proprietà **CurrentMedia** dell'oggetto **Player** . Utilizzare la proprietà **attributeCount** dell'oggetto **supporto** per determinare il numero di attributi disponibili per l'oggetto **supporto** specificato. Usare i numeri di indice con il metodo **getItemInfoByAtom** per recuperare i valori di attributo. Usare i numeri di indice con il metodo **GetAttribute** dell'oggetto **multimediale** per determinare i nomi degli attributi disponibili e quindi usare i risultati con il metodo **GetItemInfo** .

Per un esempio dell'uso di Windows Media Player metodi dell'oggetto per recuperare i metadati, vedere [playlist. attributeCount](playlist-attributecount.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




