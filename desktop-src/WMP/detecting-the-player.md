---
title: Rilevamento del lettore
description: Rilevamento del lettore
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Windows Media Player negozi online, rilevamento dei lettori
- negozi online, rilevamento di lettori
- store online di tipo 1, rilevamento dei lettori
- store online di tipo 2, rilevamento dei lettori
- Windows Media Player negozi online, rilevamento dei giocatori
- negozi online, rilevamento dei giocatori
- tipo 1 negozi online, rilevamento dei giocatori
- tipo 2 negozi online, rilevamento dei giocatori
- rilevamento del giocatore
- rilevamento di lettori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d511fc8c14a901c6823715293c5eb621b45762cd5e9fae78d8c4df503a03bf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863511"
---
# <a name="detecting-the-player"></a>Rilevamento del lettore

Quando si crea una pagina Web per il negozio online, è possibile decidere che gli utenti possano visualizzare la pagina in un Web browser o in Windows Media Player. È possibile usare uno script ASP per determinare se la pagina Web è ospitata in Player.

Il codice di esempio seguente recupera il parametro version dalla stringa di query URL per determinare se la pagina è ospitata in Windows Media Player:


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



Si noti che il codice precedente presuppone che il parametro version esista nella stringa di query quando è ospitato in Windows Media Player. Questo vale per le pagine aperte dall'utente, ma potrebbe non essere vero per le pagine aperte tramite **External.NavigateTaskPaneURL**. Perché la stringa di query della versione esista durante la navigazione a livello di codice, è necessario aggiungere il parametro version alla chiamata al metodo o aggiungere dinamicamente la versione all'URL di base dell'elemento **Navigate** del documento ServiceInfo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione dinamica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**External.NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




