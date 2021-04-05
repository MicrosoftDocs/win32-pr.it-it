---
title: Rilevamento del lettore
description: Rilevamento del lettore
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Windows Media Player Online Stores, rilevamento di giocatori
- negozi online, rilevamento di giocatori
- digitare 1 negozi online, rilevamento di giocatori
- digitare 2 archivi online, rilevamento di giocatori
- Windows Media Player Online Stores, rilevamento giocatori
- archivi online, rilevamento di giocatori
- digitare 1 negozi online, rilevamento del lettore
- digitare 2 archivi online, rilevamento del lettore
- rilevamento del lettore
- rilevamento di giocatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955547"
---
# <a name="detecting-the-player"></a>Rilevamento del lettore

Quando si crea una pagina Web per il negozio online, è possibile decidere se si desidera che gli utenti siano in grado di visualizzare la pagina in un Web browser o in Windows Media Player. Per determinare se la pagina Web è ospitata nel lettore, è possibile usare uno script ASP.

Il codice di esempio seguente recupera il parametro version dalla stringa di query dell'URL per determinare se la pagina è ospitata in Windows Media Player:


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



Si noti che il codice precedente presuppone che il parametro version esista nella stringa di query quando è ospitato in Windows Media Player. Questo vale per le pagine aperte dall'utente, ma potrebbe non essere true per le pagine aperte tramite **External. NavigateTaskPaneURL**. Affinché la stringa di query della versione esista durante la navigazione a livello di codice, è necessario aggiungere il parametro version alla chiamata al metodo o accodare dinamicamente la versione all'URL di base dell'elemento **Navigate** del documento ServiceInfo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione dinamica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




