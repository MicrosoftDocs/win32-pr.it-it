---
description: Questo argomento descrive le procedure consigliate per la progettazione di pagine Web che usano Web Authentication Broker per l'accesso.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Procedure consigliate per la progettazione di pagine Web di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80fbf38c0e020cad342331d67278818b56ce331ff39434aefd726dea52bae1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883617"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a>Procedure consigliate per la progettazione di pagine Web di autenticazione

Questo argomento descrive le procedure consigliate per la progettazione di pagine Web che usano Web Authentication Broker per l'accesso.

-   [Uso di metatag](#use-of-metatags)
-   [Uso di stili CSS Windows 8 css](#use-of-windows-8-css-styling)
-   [Uso di colori e temi](#use-of-color-and-themes)
-   [Allineamento](#alignment)
-   [Progettazione per lo snap](#designing-for-snap)
-   [Progettazione per un'esperienza di accesso veloce e fluida](#designing-for-a-fast-and-fluid-login-experience)
-   [Security Considerations](#security-considerations)
-   [Argomenti correlati](#related-topics)

## <a name="use-of-metatags"></a>Uso di metatag

Usando i metatag, il provider "Contoso Social" può specificare il titolo, l'icona e il colore dell'intestazione. Nel file HTML di esempio (WebAuthLogin.html), questa operazione viene eseguita usando il codice seguente.


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



Ciò consente Windows integrare la presenza del provider in modo importante nell'intestazione dell'interfaccia utente, come evidenziato dalla casella rossa nello screenshot seguente. ![Pagina di accesso che mostra l'intestazione contoso nell'interfaccia utente](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a>Uso di stili CSS Windows 8 css

Il foglio di stile ui-light.css fornito è Windows 8 foglio di stile usato dalle app Windows Store. Definisce lo stile Windows app dello Store per la tipografia e i controlli standard, ad esempio pulsanti, caselle di testo, collegamenti ipertestuali e caselle di controllo per assicurarsi che siano touch friendly. Quando si progettano e personalizzano le pagine di autorizzazione Web per Windows 8, è necessario usare questo foglio di stile così come è e aggiornarlo in base alle esigenze, purché la pagina Web segua comunque le procedure consigliate a modo suo.

Ad esempio, se si dispone di un foglio di stile speciale per l'aspetto e l'aspetto dei collegamenti ipertestuali nella pagina Web, è consigliabile assicurarsi che lo stile fornito sia touch friendly allo stesso modo dei collegamenti ipertestuali Windows 8 standard. Questo è essenziale per la base di consumer che usa Windows 8 nei dispositivi touch.

## <a name="use-of-color-and-themes"></a>Uso di colori e temi

Questo esempio illustra un uso riflessivo del colore in diversi modi.

-   Sfondo bianco per la pagina Web. Come si può vedere dallo screenshot precedente, la pagina Web è ospitata all'interno di una superficie bianca che si estende sulla larghezza dello schermo. Per assicurarsi che la pagina Web si integri con la superficie, è consigliabile che la pagina Web abbia uno sfondo bianco.
-   Colorazione dei controlli in base al colore del marchio. Il file CSS theme-colors.css fornisce uno stile per eseguire l'override dei colori standard dei controlli nel foglio di stile ui-light in modo che corrispondano il tema dei controlli al colore dell'intestazione. Ad esempio, nello screenshot seguente i pulsanti e i collegamenti ipertestuali accettano i colori derivati dal colore dell'intestazione. ![Screenshot dei pulsanti e del testo con lo stesso colore dell'intestazione](images/wab-figure11.png)
-   Colore dell'intestazione. L'uso del colore del marchio Contoso nell'intestazione crea una personalità unificata per il marchio del provider all'interno dell'interfaccia utente del sistema.

## <a name="alignment"></a>Allineamento

La pagina Web stessa non ha spaziatura interna a sinistra o a destra per consentire l'allineamento tipografico con il titolo nell'intestazione a sinistra e l'icona nell'intestazione a destra.

Si noterà anche che i pulsanti sono sempre allineati in basso a destra nella pagina Web e allineati a destra con l'icona nell'intestazione. Si tratta di una procedura consigliata Windows 8 gli utenti saranno abituati a flussi di dialogo simili con pulsanti in basso a destra.

## <a name="designing-for-snap"></a>Progettazione per lo snap

Nell'immagine seguente è possibile visualizzare le pagine di accesso e autorizzazioni in stato di aggancia.

![visualizzazione agganciata della schermata di accesso ](images/wab-figure12.png) . ![Visualizzazione agganciata della pagina delle autorizzazioni ](images/wab-figure13.png)

Nel file di esempio ui-webauth.css è possibile vedere l'uso di media query che ottimizzano il layout della pagina per lo stato di allineamento in base alla larghezza disponibile per la pagina Web. Il frammento di codice racchiuso nell'ambito seguente implementa CSS personalizzato per lo stato di aggancia.


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



In Windows 8, la larghezza dello stato dello snap è di 320 pixel. La pagina di autenticazione Web occupa 260 pixel nell'interfaccia utente precedente. Si usa un valore di larghezza massima con un margine sufficiente, quindi il codice media query del provider non è associato alla larghezza esatta dello stato di allineamento.

Per personalizzare l'app per la visualizzazione agganciata, è importante che l'utente non perda alcun contesto nelle altre visualizzazioni dell'esperienza di autenticazione Web (visualizzazioni complete, di riempimento o di accesso), ma è utile ri-strutturare il layout e la gerarchia degli elementi nella pagina in modo che le informazioni necessarie per mantenere il contesto siano visibili e interattive. Sono stati illustrati alcuni esempi di come l'esempio adatta la pagina Web per lo stato di aggancia.

-   Ad esempio, per la pagina di accesso in stato di agganciamento, la proprietà width del campo di testo di input (come specificato in ui-light.css) è stata sottoposta a override ed è stata impostata come valore numerico più piccolo, in modo che il campo di testo non venga ritagliato orizzontalmente.
-   Come altro esempio, nello stato di allineamento, le dimensioni del carattere delle intestazioni h1 e h2 vengono ridotte rispettivamente a 20 pt e 11 pt da 42 pt e 20 pt. Questa operazione viene eseguita in base alla Windows 8 di tipo e ottimizza il testo in modo che sia più compatto nel viewport modificato.
-   Come altro esempio, si noti che le dimensioni delle icone nella pagina delle autorizzazioni sono inferiori (confrontare con la pagina di visualizzazione completa precedente). Anche in questo caso, questa operazione viene eseguita per mantenere il contesto, scambiando gli asset di progettazione con quelli più ottimali per il viewport modificato.

## <a name="designing-for-a-fast-and-fluid-login-experience"></a>Progettazione per un'esperienza di accesso veloce e fluida

Nelle prime fasi della progettazione di questa pagina Web è stato preso in gioco il fatto che una cosa ottimale per questa pagina è un'esperienza di accesso veloce e fluida. Di conseguenza, l'interfaccia utente più importante nel flusso è il campo nome utente e password nella pagina di accesso per un'esperienza di immissione rapida delle credenziali. Anche se è stato identificato che esistono altri scenari comuni, ad esempio il recupero delle password e il riferimento alle informative sulla privacy, l'esperienza del Web è un luogo migliore per queste esperienze. Per tutti i flussi non correlati all'esperienza di autenticazione Web sicura, è consigliabile passare all'utente nel browser. Questa operazione viene illustrata nel file HTML di esempio (WebAuthLogin.html) come segue: apre tutte le pagine Web collegate dalla pagina di accesso o autorizzazioni nel browser predefinito dell'utente in cui l'utente può completare questi flussi e quindi tornare `<meta name="mswebdialog-newwindowurl" content="*" />` all'app per accedere.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Gli articoli seguenti forniscono indicazioni per la scrittura di codice C++ sicuro.

-   [Procedure consigliate per la sicurezza per C++](/cpp/security/security-best-practices-for-cpp)
-   [Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni relative allo sviluppo di pagine Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Domande frequenti su Web Authentication Broker](faq-for-web-authentication-broker.yml)
</dt> <dt>

[App di esempio di Web Authentication Broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
