---
title: Spostamento tra i riquadri attività del servizio
description: Spostamento tra i riquadri attività del servizio
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player store online, navigazione
- negozi online, navigazione
- tipo 2 negozi online, navigazione
- Windows Media Player online store,riquadri attività servizio
- negozi online, riquadri attività del servizio
- tipo 2 negozi online, riquadri attività del servizio
- Windows Media Player online, riquadri attività
- negozi online, riquadri attività
- tipo 2 negozi online, riquadri attività
- esplorazione dei negozi online di tipo 2
- Windows Media Player, riquadri attività servizio
- Windows Media Player, riquadri attività
- riquadri attività del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f54a82f2637fe11b0a2a7703cc241c47e799999a89b56ba8ba19c079b7393de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647581"
---
# <a name="navigating-between-service-task-panes"></a>Spostamento tra i riquadri attività del servizio

Per spostarsi tra i riquadri attività del servizio in Windows Media Player, usare il metodo **NavigateTaskPaneURL,** disponibile tramite **l'oggetto window.external.** Quando si usa questo metodo, si specificano i valori per tre parametri:

-   *bstrKeyName*. Si tratta del nome della chiave dello store online. Quando ci si sposta all'interno di un negozio online, usare il nome della chiave dello store corrente.
-   *bstrTaskPane*. Questa stringa contiene il nome del riquadro attività del servizio in cui si desidera spostarsi.
-   *bstrParams*. Questa stringa contiene i parametri della stringa di query da aggiungere all'URL per la pagina Web ospitata dal riquadro attività del servizio in cui si vuole spostarsi.

La navigazione è gestita da una pagina Web creata, denominata pagina di navigazione. L'URL per la pagina di navigazione viene specificato **dall'elemento Navigate** nel documento ServiceInfo. Quando si chiama **NavigateTaskPaneURL,** Windows Media Player apre la pagina di navigazione, non la pagina Web specificata dagli elementi **ServiceTask1,** **ServiceTask2** o **ServiceTask3.** È la pagina di navigazione che riceve la stringa di query specificata da *bstrParams*. La pagina di navigazione deve contenere le regole che determinano il contenuto visualizzato in un riquadro attività del servizio dopo la navigazione.

Si supponga, ad esempio, di voler fare clic su un collegamento per passare da **ServiceTask1** a **ServiceTask2.** È possibile usare il codice HTML seguente per creare il collegamento:


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



Quando l'utente fa clic sul collegamento Video, Windows Media Player passa a **ServiceTask2** e apre la pagina di navigazione, aggiungendo la stringa di query seguente al relativo URL.


```C++
?From=Music&To=2

```



Il parametro From identifica la pagina da cui l'utente ha fatto clic sul collegamento e il parametro A identifica il numero del riquadro attività del servizio in cui si vuole spostarsi. Si noti che questi parametri non sono particolari. È possibile usare qualsiasi parametro per qualsiasi scopo.

Ad esempio, il codice di esempio seguente mostra **l'elemento Navigate** in un documento ServiceInfo:


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



L'URL risultante, completo di stringa di query, è illustrato nell'esempio seguente:


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



Il codice di esempio seguente mostra la pagina di navigazione:


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



Il codice precedente crea semplicemente un URL e reindirizza il browser a esso. In primo luogo, il codice recupera i valori to dalla stringa di query dell'URL e dalla stringa di query stessa. Usa il valore del parametro To per determinare la pagina da visualizzare. Aggiunge quindi la stringa di query originale all'URL. Infine, si sposta nel browser usando un URL simile al seguente:


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



Ogni volta che si esegue la navigazione in questo modo, assicurarsi di specificare [External.SelectedTaskPane](external-selectedtaskpane.md) per assicurarsi che sia evidenziato il pulsante di attività corretto.

-   **Avviso** Prestare attenzione all'uso dei parametri della stringa di query per la navigazione.

Le pagine Web HTMLView possono essere fornite da chiunque crei una playlist ASX. Ciò significa che i siti Web dannosi possono passare i valori della stringa di query al negozio online **usando NavigateTaskPaneURL.** È necessario pianificare questa possibilità per mantenere sicuro lo store online. Ad esempio, se lo store online visualizza semplicemente un valore di stringa di query per l'utente, un sito Web dannoso potrebbe visualizzare testo imprevisto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento Navigate**](navigate-element.md)
</dt> <dt>

[**Navigazione per i negozi online di tipo 2**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




