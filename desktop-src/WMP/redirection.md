---
title: Reindirizzamento
description: Reindirizzamento
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Playlist Windows Media Metafile, Reindirizzamento
- playlist, Reindirizzamento
- playlist di metafile, Reindirizzamento
- Media Player di Windows, Reindirizzamento
- reindirizzamento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328572"
---
# <a name="redirection"></a>Reindirizzamento

Nella playlist il browser viene reindirizzato a Windows Media Player per riprodurre il flusso multimediale o il file multimediale designato. La playlist di metafile più semplice contiene solo il Uniform Resource Locator (URL) di un file multimediale.

Per creare una playlist di metafile di base, aprire l'editor di testo preferito, ad esempio il blocco note Microsoft, quindi digitare il codice di esempio seguente.


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



Sostituire un percorso valido del file Windows Media usando la sintassi riportata nella tabella seguente.



| Origine del contenuto                                                                                 | Sintassi                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| Il contenuto è un file in un server Windows Media                                                       | mms://ServerName/Path/FileName.wma        |
| Il contenuto è un multicast broadcast a cui si accede da un Windows Media Station                    | https://WebServerName/Stations/kxyz.nsc    |
| Il contenuto è un unicast broadcast a cui si accede da un punto di pubblicazione in un server Windows Media | mms://ServerName/PublishingPointAlias     |
| Il contenuto è un file in un server Web                                                                 | https://WebServerName/Path/Filename.wma    |
| Il contenuto è un file su un disco rigido locale                                                            | file://c: \\ percorso \\ nomefile. WMA             |
| Il contenuto è un file in una condivisione di rete                                                              | file:// \\ \\ NomeServer \\ percorso \\ nomefile. WMA |
| Il contenuto è un file in un server Windows Media                                                       | mms://ServerName/Path/FileName.wmv        |



 

Salvare il file creato con un nome file e un'estensione, come descritto in [estensioni di file](file-name-extensions.md). Fare doppio clic su di esso in Esplora risorse. Windows Media Player dovrebbe aprire e avviare lo streaming del contenuto. È possibile salvare il file nel server Web, insieme alle pagine Web, e collegarlo a un elemento **href** oppure incorporarlo in una pagina Web usando il tag **oggetto** di Windows Media Player.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Uso delle playlist di metafile**](using-metafile-playlists.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




