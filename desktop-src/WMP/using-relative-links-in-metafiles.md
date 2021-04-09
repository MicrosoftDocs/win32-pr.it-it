---
title: Uso di collegamenti relativi nei metafile
description: Uso di collegamenti relativi nei metafile
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Playlist Windows Media Metafile, collegamenti relativi
- playlist, collegamenti relativi
- playlist di metafile, collegamenti relativi
- Metafile, collegamenti relativi
- Metafile di Windows Media, collegamenti relativi
- collegamenti relativi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855842"
---
# <a name="using-relative-links-in-metafiles"></a>Uso di collegamenti relativi nei metafile

I collegamenti relativi sono una funzionalità completamente supportata dei file di Windows Media. È possibile usare collegamenti relativi nei metafile in modo analogo a come vengono usati nei documenti HTML. L'utilizzo di collegamenti relativi consente di creare metafile portabili, ovvero è possibile copiare o spostare un'intera struttura di directory in un altro server senza aggiornare i percorsi a file grafici utilizzati come banner o gli attributi **href** degli elementi **moreinfo** (se fanno riferimento a file nello stesso server Web del metafile archiviato). I collegamenti relativi funzionano in qualsiasi applicazione che li supporta, perché le parti dell'URL non incluse nell'attributo **href** di un elemento sono incluse nell'URL inviato dall'applicazione al server quando viene richiesto l'URL. Ciò significa che il protocollo (ad esempio https://), il nome del server e la directory virtuale in cui si trova il file contenente il collegamento relativo sono tutti inclusi nell'URL inviato al server. Se il file multimediale o l'URL a cui si collega il collegamento utilizzando un collegamento relativo non si trova nello stesso server del metafile, il collegamento relativo non è valido.

> [!Note]  
> Queste informazioni sui collegamenti relativi sono corrette solo quando si usa un collegamento ai metafile aperti nel Media Player Windows autonomo. Quando si usa il controllo Media Player Windows incorporato, tutti i collegamenti sono relativi alla pagina in cui è ospitato il controllo, a meno che l'elemento figlio di **base** dell'elemento **ASX** non venga usato per reindirizzare il percorso relativo.

 

Tutti i collegamenti relativi nel metafile devono essere completamente relativi, non relativi all'unità, per i flussi multimediali. Quando un URL inizia con un \\ carattere "", il collegamento è relativo all'unità. Windows Media Player tenta di aprire il file collegato all'unità in cui è stato aperto il metafile, in genere un server Web. Poiché i server Web utilizzano le directory virtuali, Windows Media Player tenta di trovare il flusso o il file multimediale specificato in una sottodirectory di una directory virtuale nel server Web da cui è stato aperto il metafile. Un utente non può accedere a una directory del server. Nell'esempio riportato in questa sezione viene illustrato l'utilizzo di un collegamento completamente relativo.

È possibile utilizzare i collegamenti relativi alle unità quando si utilizzano metafile in un singolo computer in cui sono presenti tutti i file multimediali collegati alla playlist del metafile in un dispositivo di archiviazione del computer. Tuttavia, non è possibile eseguire lo streaming di file multimediali in questo modo.

Quando si usa un collegamento a un altro metafile per consentire i collegamenti relativi, il nome visualizzato come titolo di Windows Media Player è il titolo del metafile originale.

Non è possibile usare collegamenti relativi per gli URL di un server dei flussi multimediali perché vengono usati protocolli diversi per accedere al contenuto dei flussi multimediali.

Nella playlist di esempio seguente, il primo **ENTRYREF** contiene un URL per un'altra playlist, relativa. Wax.


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



L'esempio seguente è il file relativo. Wax, che contiene collegamenti relativi.


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



L'URL che contiene il riferimento alla playlist, relativa. Wax, può esistere in una playlist di metafile ovunque sia accessibile all'utente. Affinché l'URL venga elaborato correttamente, deve essere presente un server Web denominato "example.microsoft.com". Il server Web deve avere una directory virtuale definita come "Metafiles". La playlist a cui si fa riferimento, relativa. Wax, deve esistere nel server Web denominato "example.microsoft.com" nella directory virtuale "Metafiles".

Per poter accedere e riprodurre correttamente i file multimediali a cui viene fatto riferimento nella playlist relativa. Wax, è necessario che sia presente una directory denominata "graphics", che è una sottodirectory della directory virtuale del server "Metafiles". Il file di grafica Logo1.jpg, a cui si fa riferimento nell'elemento **banner** , deve essere la sottodirectory denominata graphics.

Analogamente, un documento denominato Category1.htm deve trovarsi in una sottodirectory denominata Categoria1. La directory denominata Categoria1 deve esistere come sottodirectory della directory virtuale "Metafiles" sul server Web example.microsoft.com.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




