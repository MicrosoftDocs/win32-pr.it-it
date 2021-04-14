---
title: Spostamento tra i riquadri attività del servizio
description: Spostamento tra i riquadri attività del servizio
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player Online Stores, spostamento
- negozi online, esplorazione
- digitare 2 archivi online, spostamento
- Windows Media Player Online Stores, riquadri attività servizio
- archivi online, riquadri attività del servizio
- digitare 2 archivi online, riquadri attività servizio
- Windows Media Player Online Stores, riquadri attività
- archivi online, riquadri attività
- digitare 2 archivi online, riquadri attività
- spostamento nei negozi online di tipo 2
- Media Player di Windows, riquadri attività servizio
- Media Player di Windows, riquadri attività
- riquadri attività servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035215f822c67bb40c528f141422977efc8653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329980"
---
# <a name="navigating-between-service-task-panes"></a>Spostamento tra i riquadri attività del servizio

Per spostarsi tra i riquadri attività del servizio in Windows Media Player, utilizzare il metodo **NavigateTaskPaneURL** , disponibile tramite l'oggetto **Window. External** . Quando si usa questo metodo, si specificano i valori per tre parametri:

-   *bstrKeyName*. Si tratta del nome della chiave dell'archivio online. Quando si esegue la navigazione all'interno di un archivio online, usare il nome della chiave dell'archivio corrente.
-   *bstrTaskPane*. Questa stringa contiene il nome del riquadro attività del servizio in cui si desidera spostarsi.
-   *bstrParams*. Questa stringa contiene i parametri della stringa di query che si desidera aggiungere all'URL per la pagina Web ospitata dal riquadro attività del servizio in cui si desidera spostarsi.

La navigazione viene gestita da una pagina Web creata, denominata pagina Navigate. L'URL della pagina Navigate viene specificato dall'elemento **Navigate** nel documento ServiceInfo. Quando si chiama **NavigateTaskPaneURL**, Windows Media Player apre la pagina Navigate, non la pagina Web specificata dagli elementi **ServiceTask1**, **ServiceTask2** o **ServiceTask3** . Si tratta della pagina Navigate che riceve la stringa di query specificata da *bstrParams*. La pagina Navigate deve contenere le regole che determinano quale contenuto viene visualizzato in un riquadro attività del servizio dopo lo spostamento.

Si supponga, ad esempio, di voler fare in modo che gli utenti clicchino su un collegamento per passare da **ServiceTask1** a **ServiceTask2**. Per creare il collegamento, è possibile usare il codice HTML seguente:


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



Quando l'utente fa clic sul collegamento video, Windows Media Player passa a **ServiceTask2** e apre la pagina Navigate, aggiungendo la stringa di query seguente al relativo URL.


```C++
?From=Music&To=2

```



Il parametro from identifica la pagina dalla quale l'utente ha fatto clic sul collegamento e il parametro to identifica il numero del riquadro attività del servizio a cui vuole spostarsi. Si noti che non c'è niente di speciale su questi parametri. È possibile usare tutti i parametri desiderati per qualsiasi scopo.

Ad esempio, il codice di esempio seguente mostra l'elemento **Navigate** in un documento ServiceInfo:


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



L'URL risultante, completo con la stringa di query, è illustrato nell'esempio seguente:


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



Il codice di esempio seguente mostra la pagina Navigate:


```C++
<%
    Dim sURL
    Dim sQS
    Dim sTo

    sURL = ""
    sQS = Request.ServerVariables("QUERY_STRING")
    sTo = "" & Request.QueryString("To")
 
    Select Case sTo
       Case "1" sURL = sURL & "Music_Music.asp"
       Case "2" sURL = sURL & "Music_Video.asp"
       Case "3" sURL = sURL & "Music_Radio.asp"
       Case Else sURL = sURL & "Music_Music.asp"
    End Select
     
    sURL = sURL & "?" & sQS

    Response.Redirect(sURL)    
%>

```



Il codice precedente crea semplicemente un URL e ne reindirizza il browser. In primo luogo, il codice recupera i valori dalla stringa di query dell'URL e dalla stringa di query stessa. Usa il valore del parametro to per determinare la pagina da visualizzare. Viene quindi aggiunta la stringa di query originale all'URL. Infine, Esplora il browser usando un URL simile al seguente:


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



Quando si esegue la navigazione in questo modo, assicurarsi di specificare [External. SelectedTaskPane](external-selectedtaskpane.md) per assicurarsi che il pulsante attività corretto sia evidenziato.

-   **Avviso** di Prestare attenzione all'uso dei parametri della stringa di query per la navigazione.

Le pagine Web di HTMLView possono essere fornite da chiunque crei una playlist ASX. Ciò significa che i siti Web dannosi possono passare i valori della stringa di query allo Store online usando **NavigateTaskPaneURL**. È necessario pianificare questa possibilità per garantire la protezione del proprio negozio online. Ad esempio, se l'archivio online Visualizza semplicemente un valore della stringa di query per l'utente, un sito Web dannoso potrebbe visualizzare un testo imprevisto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Navigate-elemento**](navigate-element.md)
</dt> <dt>

[**Navigazione per i negozi di tipo 2 online**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




