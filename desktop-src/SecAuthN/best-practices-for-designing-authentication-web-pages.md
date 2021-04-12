---
description: Questo argomento descrive le procedure consigliate per la progettazione di pagine Web che usano il broker di autenticazione Web per l'accesso.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Procedure consigliate per la progettazione di pagine Web di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6360e313b49a69c16aebf532911bcdf562f9a4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344366"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a>Procedure consigliate per la progettazione di pagine Web di autenticazione

Questo argomento descrive le procedure consigliate per la progettazione di pagine Web che usano il broker di autenticazione Web per l'accesso.

-   [Uso dei metatag](#use-of-metatags)
-   [Uso dello stile CSS di Windows 8](#use-of-windows-8-css-styling)
-   [Uso di colori e temi](#use-of-color-and-themes)
-   [Allineamento](#alignment)
-   [Progettazione per snap](#designing-for-snap)
-   [Progettazione per un'esperienza di accesso rapida e fluida](#designing-for-a-fast-and-fluid-login-experience)
-   [Security Considerations](#security-considerations)
-   [Argomenti correlati](#related-topics)

## <a name="use-of-metatags"></a>Uso dei metatag

Utilizzando i metatag, il provider "contoso social" può specificare il titolo, l'icona e il colore dell'intestazione. Nel file HTML di esempio (WebAuthLogin.html), questa operazione viene eseguita usando il codice seguente.


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



Questo consente a Windows di integrare la presenza del provider in modo significativo nell'intestazione dell'interfaccia utente evidenziata dalla casella rossa nello screenshot seguente. ![pagina di accesso che mostra l'intestazione Contoso nell'interfaccia utente](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a>Uso dello stile CSS di Windows 8

Il foglio di stile UI-Light. CSS fornito è il foglio di stile di Windows 8 usato dalle app di Windows Store. Definisce lo stile delle app di Windows Store per la tipografia e i controlli standard, ad esempio pulsanti, caselle di testo, collegamenti ipertestuali e caselle di controllo per assicurarsi che siano compatibili con il tocco. Quando si progettano e si personalizzano le pagine di autorizzazione Web per Windows 8, si consiglia di usare questo foglio di stile e di aggiornarlo in base alle esigenze, purché la pagina Web segua le procedure consigliate in modo specifico.

Se, ad esempio, si dispone di un foglio di stile speciale per i collegamenti ipertestuali che dovrebbero avere un aspetto analogo a quello della pagina Web, è opportuno prestare attenzione a garantire che lo stile fornito sia semplice da usare in modo analogo ai collegamenti ipertestuali standard di Windows 8. Questa operazione è essenziale per la base di utenti che usa Windows 8 sui dispositivi touch.

## <a name="use-of-color-and-themes"></a>Uso di colori e temi

In questo esempio viene illustrato un utilizzo ponderato del colore in diversi modi.

-   Sfondo bianco per la pagina Web. Come si può vedere dallo screenshot precedente, la pagina Web è ospitata all'interno di una superficie bianca che copre la larghezza dello schermo. Per assicurarsi che la pagina Web si integri con la superficie, è consigliabile che la pagina Web disponga di uno sfondo bianco.
-   Colorazione dei controlli in base al colore del marchio. Il file CSS Theme-Colors. CSS fornisce lo stile per eseguire l'override dei colori standard dei controlli nel foglio di stile della luce dell'interfaccia utente in modo che corrisponda a quello dei controlli al colore dell'intestazione. Nello screenshot seguente, ad esempio, i pulsanti e i collegamenti ipertestuali accettano i colori derivati dal colore dell'intestazione. ![screenshot dei pulsanti e del testo con lo stesso colore dell'intestazione](images/wab-figure11.png)
-   Colore dell'intestazione. L'uso del colore del marchio di Contoso nell'intestazione crea una personalità unificata per il marchio del provider nell'interfaccia utente del sistema.

## <a name="alignment"></a>Allineamento

La pagina Web non ha spaziatura interna a sinistra o a destra per consentire l'allineamento tipografico con il titolo nell'intestazione a sinistra e l'icona nell'intestazione a destra.

Si noterà anche che i pulsanti sono sempre allineati in basso a destra nella pagina Web ed è allineato a destra con l'icona nell'intestazione. Si tratta di una procedura consigliata poiché gli utenti di Windows 8 saranno abituati a flussi di finestre di dialogo simili con pulsanti in basso a destra.

## <a name="designing-for-snap"></a>Progettazione per snap

Nell'immagine seguente è possibile visualizzare le pagine account di accesso e autorizzazioni in stato di snap-in.

![visualizzazione snap della schermata di accesso ](images/wab-figure12.png) . ![visualizzazione snap della pagina autorizzazioni ](images/wab-figure13.png)

Nel file di esempio UI-WebAuth. CSS è possibile vedere l'uso di query multimediali per ottimizzare il layout della pagina per lo stato di snap in base alla larghezza disponibile per la pagina Web. Il frammento di codice incluso nell'ambito seguente implementa il CSS personalizzato per lo stato di snap.


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



In Windows 8, la larghezza dello stato di allineamento è 320 pixel. La pagina autenticazione Web occupa 260 pixel nell'interfaccia utente precedente. Si sta usando un valore di larghezza massima con un margine sufficiente, quindi il codice di query del supporto del provider non è associato alla larghezza esatta dello stato di allineamento.

Per personalizzare l'app per la visualizzazione snap, è importante che l'utente non perda alcun contesto presente nelle altre visualizzazioni dell'esperienza di autenticazione Web (viste Full, Fill o charm), ma è utile ristrutturare il layout e la gerarchia degli elementi nella pagina in modo che le informazioni necessarie per mantenere il contesto siano visibili e interattive. Sono stati illustrati alcuni esempi del modo in cui l'esempio segue la pagina Web per lo stato di allineamento.

-   Per la pagina di accesso nello stato di allineamento, ad esempio, la proprietà Width del campo di testo di input (come specificato in UI-Light. CSS) è stata sottoposta a override ed è stata impostata come valore numerico più piccolo, in modo che il campo di testo non venga troncato orizzontalmente.
-   Come altro esempio, nello stato di snap, le dimensioni del carattere delle intestazioni H1 e H2 vengono ridotte rispettivamente a 20 PT e 11 PT da 42 PT e 20 PT. Questa operazione viene eseguita in base alla rampa di tipo Windows 8 e ottimizza il testo in modo da essere più compatto nel viewport modificato.
-   Per un altro esempio, si noti che le dimensioni delle icone nella pagina autorizzazioni sono inferiori (confrontare la pagina di visualizzazione completa precedente). Anche in questo caso, questa operazione viene eseguita per mantenere il contesto, scambiando le risorse di progettazione per quelle più ottimali per il viewport modificato.

## <a name="designing-for-a-fast-and-fluid-login-experience"></a>Progettazione per un'esperienza di accesso rapida e fluida

Nella fase iniziale della progettazione di questa pagina Web, abbiamo creato un punto di interesse per l'accesso rapido e fluido a questa pagina. Di conseguenza, l'interfaccia utente più importante nel flusso è il campo nome utente e password nella pagina di accesso per una rapida esperienza di immissione delle credenziali. Sebbene sia stato rilevato che esistono altri scenari comuni, ad esempio il recupero delle password e il riferimento a informative sulla privacy, l'esperienza avanzata del Web è una posizione migliore per tali esperienze. Per tutti i flussi non correlati all'esperienza di autenticazione Web sicura, è consigliabile passare all'utente nel browser. Questa operazione viene mostrata nel file HTML di esempio (WebAuthLogin.html) come indicato di seguito: `<meta name="mswebdialog-newwindowurl" content="*" />` consente di aprire tutte le pagine Web collegate a dalla pagina account di accesso o autorizzazioni nel browser predefinito dell'utente, in cui l'utente può completare questi flussi e tornare all'app per accedere.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Gli articoli seguenti forniscono indicazioni per la scrittura di codice C++ sicuro.

-   [Procedure di protezione ottimali per C++](/cpp/security/security-best-practices-for-cpp)
-   [Modelli & procedure consigliate per la sicurezza delle applicazioni](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni relative allo sviluppo di pagine Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Domande frequenti sul broker di autenticazione Web](faq-for-web-authentication-broker.md)
</dt> <dt>

[App di esempio SDK Web Authentication broker](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
