---
title: Utilizzo di pagine ASP per la creazione dinamica di playlist di metafile di Windows Media
description: Utilizzo di pagine ASP per la creazione dinamica di playlist di metafile di Windows Media
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Playlist Windows Media Metafile, creazione
- playlist di metafile, creazione
- playlist, creazione
- Playlist Windows Media Metafile, creazione dinamica
- playlist di metafile, creazione dinamica
- playlist, creazione dinamica
- Playlist Windows Media Metafile, pagine ASP
- playlist di metafile, pagine ASP
- playlist, pagine ASP
- creazione di playlist Windows Media Metafile
- creazione dinamica di playlist Windows Media Metafile
- ASP (pagine)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515688"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a>Utilizzo di pagine ASP per la creazione dinamica di playlist di metafile di Windows Media

È possibile utilizzare Active Server pagine (file ASP o ASP) per generare in modo dinamico le playlist in base alle informazioni fornite dagli utenti. Una pagina ASP è una pagina Web dinamica utilizzata insieme a Microsoft Internet Information Services (IIS). ASP è un ambiente in cui è possibile combinare HTML, script e componenti server ActiveX riutilizzabili per creare soluzioni aziendali dinamiche e potenti basate sul Web. Le pagine ASP consentono l'esecuzione di script sul lato server per IIS con supporto nativo sia per Microsoft Visual Basic Scripting Edition (VBScript) che per Microsoft JScript. In questa discussione si presuppone che l'utente abbia familiarità con ASP e definendo le variabili.

Tutte le informazioni di intestazione devono essere contenute nella prima riga della stringa di pagina ASP restituita a Windows Media Player.

Quando si usano le pagine ASP per generare playlist, è necessario specificare i valori per le proprietà **ContentType** dell'oggetto **risposta** e la **scadenza** della pagina ASP a causa di problemi di latenza con Windows Media Player. Il valore **Response. ContentType** deve essere un'estensione di nome file valida per i file di Windows Media. I valori accettabili sono WMA, Wax, WMV, WVX, ASF e ASX.

La proprietà **Response. Expires** specifica il periodo di tempo, in secondi, in cui Windows Media Player memorizza nella cache il file della playlist. Se si specifica un valore pari a zero, in Windows Media Player richiesta una nuova playlist dal server ogni volta che l'utente aggiorna la pagina.

Per informazioni dettagliate sull'uso dell'oggetto **risposta** nelle pagine Active Server, vedere Platform SDK.

Il codice seguente è un esempio di pagina ASP utilizzata per generare una playlist di Windows Media Metafile.


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> </dl>

 

 




