---
description: Una pagina Web Personalizza l'interfaccia utente con il titolo, l'icona e il colore dell'intestazione usando i tag dei metadati definiti nella pagina Web.
ms.assetid: 6F1E0B2E-E013-4C5B-86A4-0AF8606D0C12
title: Come personalizzare gli elementi dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19314f8e4c5d4944a500a0eef3aa0f75cd231b12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883906"
---
# <a name="how-to-customize-the-ui-elements"></a>Come personalizzare gli elementi dell'interfaccia utente

Una pagina Web Personalizza l'interfaccia utente con il titolo, l'icona e il colore dell'intestazione usando i tag dei metadati definiti nella pagina Web. Gli sviluppatori Web possono usare <meta> tag HTML per visualizzare la personalità e il marchio del provider nell'interfaccia utente del broker di autenticazione Web. Inoltre, gli sviluppatori possono indirizzare azioni utente più complesse, ad esempio l'iscrizione e il recupero delle password. Il concetto è molto simile alla funzionalità siti bloccati di Windows Internet Explorer 9 e Windows 7.

Oltre a personalizzare l'interfaccia utente intorno all'area della pagina Web, la pagina Web deve sfruttare anche gli stili dei controlli di Windows 8, essere abilitata per il tocco e consentire l'apertura di collegamenti nel browser laddove appropriato.

Di seguito è riportato un esempio di una pagina Web che ha sfruttato il modello di personalizzazione del broker di autenticazione Web. ![elementi dell'interfaccia utente del broker di autenticazione Web](images/wab-figure7.png)

## <a name="instructions"></a>Istruzioni

### <a name="step-1-customize-the-icon"></a>Passaggio 1: personalizzare l'icona

La pagina Web può fornire un'icona usando un tag meta mswebdialog-logo.

``` syntax
<meta name="mswebdialog-logo" content="https://www.contoso.com/logo.png"/>
```

Il contenuto è un URL che può essere relativo o assoluto. Lo schema dell'URL può essere HTTP o HTTPS. Il formato del file deve essere PNG o JPG. Le dimensioni dell'immagine devono essere 30x30 pixel. Se le dimensioni dell'immagine sono diverse, verranno ridimensionate o ridotte dal sistema operativo per adattarle allo spazio 30x30. L'immagine deve essere progettata in modo da renderla ottimale quando viene scalato fino a 140% e 180% per tenere conto di schermi di risoluzione superiore. Per testare diversi fattori di scalabilità, usare l' [app di esempio Web Authentication broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) caricata in Visual Studio 11, che consente di simulare diversi fattori di risoluzioni e scalabilità usando le finestre del dispositivo della modalità progettazione.

### <a name="step-2-customize-the-title-text"></a>Passaggio 2: personalizzare il testo del titolo

La pagina Web può fornire il titolo usando il tag meta mswebdialog-title.

``` syntax
<meta name="mswebdialog-title" content="Contoso Social"/>
```

Il titolo deve essere breve e deve riflettere il marchio del provider (ad esempio, contoso).

### <a name="step-3-customize-the-header-color"></a>Passaggio 3: personalizzare il colore dell'intestazione

La pagina Web può fornire il colore che rappresenta la propria identità del marchio da usare per l'intestazione della finestra di dialogo usando il tag meta mswebdialog-header-color.

``` syntax
<meta name="mswebdialog-header-color" content="#1267DF"/>
```

Il colore può essere qualsiasi valore specificato qui. Tuttavia, il broker di autenticazione Web ignorerà qualsiasi valore del canale alfa. Con questo colore in particolare e con i colori usati nella pagina in generale, è consigliabile seguire gli stessi colori usati nell'app di Windows 8 del provider, se tale app esiste.

> [!Note]  
> Le icone e i colori vengono memorizzati nella cache per ogni server nel client una volta analizzati i tag META. Cancellare la cache del client prima di avviare l'interfaccia utente affinché le modifiche abbiano effetto. A tale scopo, modificare le impostazioni del registro di sistema seguenti.

 

``` syntax
// Registry location under HKLM used for setting various AuthHost parameters.
#define AUTH_HOST_LOCAL_MACHINE_REGPATH \
    L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Image File Execution Options\\authhost.exe"
// MaxAge to use for downloading logo images
#define AUTH_HOST_LOGO_IMAGE_MAX_AGE_SECONDS_REG_VALUE_NAME \
    L"LogoImageMaxAgeSeconds"
// 24 hours
#define AUTH_HOST_LOGO_IMAGE_MAX_AGE_SECONDS_DEFAULT        \
    (24 * 60 * 60)
```

Una volta scaricata, l'icona non viene rilevata per 24 ore. Per eseguire il test con le immagini del logo, impostare la chiave reg sopra con un valore inferiore.

### <a name="step-4-customize-the-web-page"></a>Passaggio 4: personalizzare la pagina Web

Oltre a personalizzare l'interfaccia utente per la pagina Web, gli sviluppatori devono anche creare pagine Web perfettamente integrabili con l'esperienza complessiva di Windows 8. Questo include l'uso di stili consigliati, assicurandosi che le pagine Web funzionino con i dispositivi abilitati per il tocco e aprano determinate pagine Web nel Web browser.

-   Stile

    Si consiglia vivamente di utilizzare lo stile consigliato per creare un'esperienza utente più coerente tra le pagine Web del broker di autenticazione Web e altri componenti dell'interfaccia utente di Windows 8. La pagina Web deve utilizzare uno sfondo bianco senza bordi. I pulsanti, ad esempio account di accesso o Annulla, devono essere posizionati nell'angolo inferiore destro e utilizzare lo stesso colore dell'intestazione. Infine, poiché il broker di autenticazione Web fornisce un pulsante indietro, provare a eliminare completamente un pulsante Annulla dalla pagina Web.

-   Abilitazione tocco

    La pagina Web deve essere progettata tenendo presente un'interazione utente basata sul tocco. Per ulteriori informazioni sulla progettazione di touch in Windows 8, vedere l'argomento relativo alla [progettazione dell'interazione touch](https://msdn.microsoft.com/library/Hh465415(v=Win.10).aspx) .

-   Personalizzazione della destinazione dei collegamenti ipertestuali

    Il broker di autenticazione Web è ideale per la distribuzione di pagine Web che richiedono una singola azione dell'utente, ad esempio le pagine di autorizzazione Logon o OAuth. Tuttavia, per i flussi utente più complessi, ad esempio la creazione di account, il ripristino da una password persa o dimenticata, la visualizzazione delle informative sulla privacy e così via, in cui l'utente deve investire del tempo per comprendere e completare il flusso, è consigliabile avviare queste pagine nel browser preferito dell'utente per supportare la navigazione completa e raggiungere l'esplorazione. Il broker di autenticazione Web per impostazione predefinita non consente l'apertura di nuove finestre del browser da una pagina Web. per ulteriori informazioni, vedere la sezione nessuna nuova finestra per impostazione predefinita. Tuttavia, usando il tag meta, `mswebdialog-newwindowurl` la pagina Web può dichiarare gli URL da aprire nel browser.

    `mswebdialog-newwindowurl`Consente alla pagina Web di specificare un URL o una parte dell'URL che il broker di autenticazione Web userà per trovare una corrispondenza (corrispondenza della stringa a sinistra) su ogni volta che viene richiesto di aprire un URL in una nuova finestra usando l'attributo di destinazione o il metodo Window. Open (). Se esiste una corrispondenza, l'URL verrà aperto nel browser predefinito dell'utente. Se non esiste alcuna corrispondenza, il broker di autenticazione Web passerà all'URL stesso (comportamento predefinito). Ad esempio:`<meta name="mswebdialog-newwindowurl" content="https://www.contoso.com/privacy"/>`

    Nel caso di questo tag meta, il broker di autenticazione Web aprirà https://www.contoso.com/privacy/policy.html nel browser, ma passerà direttamente a https://www.contoso.com/termsofuse.html . Si noti che i collegamenti che non tentano di aprire in una nuova finestra, ad esempio i collegamenti che non usano l'attributo di destinazione o il metodo Window. Open () non sono interessati da questo tag meta. Il contenuto è un URL che può essere relativo o assoluto. Lo schema dell'URL può essere HTTP o HTTPS. È necessario definire i `mswebdialog-newwindowurl` metatag per coprire tutti i collegamenti che non fanno parte del flusso utente principale, ad esempio informativa sulla privacy, moduli di iscrizione e così. Se si supporta l'accesso con un provider di autenticazione di terze parti (ad esempio, provider OpenID), assicurarsi di mantenere tali interazioni nel broker di autenticazione Web. Per abilitare l'apertura sicura di tutti i collegamenti nella pagina nel browser, usare la sintassi Star, ad esempio, `  <meta name="mswebdialog-newwindowurl" content="*"/>` si noti che " \* " può essere usato solo in modo esclusivo e non può essere combinato con un altro URL, ad esempio " https://www.contoso.com/\ *" non è una sintassi valida.

### <a name="step-5-rules-applied-to-all-meta-tags"></a>Passaggio 5: regole applicate a tutti i tag meta

Quando il broker di autenticazione Web elabora i tag meta, si applicano le regole seguenti:

-   L'effetto del tag meta verrà mantenuto in tutte le pagine nello stesso dominio di secondo livello (ad esempio, contoso.com), a meno che non venga rilevato un altro tag meta con lo stesso nome ma contenuto diverso.
-   Se nella stessa pagina vengono rilevati più tag meta con lo stesso nome, il broker di autenticazione Web sceglierà solo uno di essi e ignorerà il resto. Il tag meta specifico scelto non è definito.
    > [!Note]  
    > Questa regola non si applica al `mswebdialog-newwindowurl` tag meta che consente più istanze nella stessa pagina.

     

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni relative allo sviluppo di pagine Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[App di esempio SDK Web Authentication broker](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
