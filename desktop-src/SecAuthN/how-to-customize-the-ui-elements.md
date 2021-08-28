---
description: Una pagina Web personalizza l'interfaccia utente con il titolo, l'icona e il colore dell'intestazione usando i tag di metadati definiti nella pagina Web.
ms.assetid: 6F1E0B2E-E013-4C5B-86A4-0AF8606D0C12
title: Come personalizzare gli elementi dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a99e8e7da789653226db40763116472eb065df0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884555"
---
# <a name="how-to-customize-the-ui-elements"></a>Come personalizzare gli elementi dell'interfaccia utente

Una pagina Web personalizza l'interfaccia utente con il titolo, l'icona e il colore dell'intestazione usando i tag di metadati definiti nella pagina Web. Gli sviluppatori Web possono usare i metatag HTML per visualizzare la personalità e il marchio del &lt; &gt; provider nell'interfaccia utente di Web Authentication Broker. Inoltre, gli sviluppatori possono indirizzare azioni utente più complesse, ad esempio la registrazione e il ripristino delle password. Il concetto è molto simile alla funzionalità Siti aggiunti di Windows Internet Explorer 9 e Windows 7.

Oltre a personalizzare l'interfaccia utente intorno all'area della pagina Web, la pagina Web deve anche sfruttare gli stili dei controlli Windows 8, essere abilitata per il tocco e consentire l'apertura dei collegamenti nel browser dove appropriato.

Di seguito è riportato un esempio di pagina Web che ha sfruttato il modello di personalizzazione di Gestore autenticazione Web. ![Elementi dell'interfaccia utente del broker di autenticazione Web](images/wab-figure7.png)

## <a name="instructions"></a>Istruzioni

### <a name="step-1-customize-the-icon"></a>Passaggio 1: Personalizzare l'icona

La pagina Web può fornire un'icona usando un metatag mswebdialog-logo.

``` syntax
<meta name="mswebdialog-logo" content="https://www.contoso.com/logo.png"/>
```

Il contenuto è un URL che può essere una pagina relativa o assoluta. Lo schema dell'URL può essere HTTP o HTTPS. Il formato del file deve essere PNG o JPG. Le dimensioni dell'immagine devono essere di 30x30 pixel. Se l'immagine ha dimensioni diverse, verrà ridotta o ridotta dal sistema operativo per adattarsi allo spazio di 30x30. L'immagine deve essere progettata in modo da essere visualizzata correttamente quando viene ridimensionata fino al 140% e al 180% per prendere in considerazione schermi con risoluzione superiore. Per testare diversi fattori di scala, usare l'app di esempio [Web Authentication Broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) caricata in Visual Studio 11 che consente di simulare risoluzioni e fattori di ridimensionamento diversi usando le finestre dispositivo della modalità progettazione.

### <a name="step-2-customize-the-title-text"></a>Passaggio 2: Personalizzare il testo del titolo

La pagina Web può fornire il titolo usando il tag meta mswebdialog-title.

``` syntax
<meta name="mswebdialog-title" content="Contoso Social"/>
```

Il titolo deve essere breve e deve riflettere il marchio del provider (ad esempio, Contoso).

### <a name="step-3-customize-the-header-color"></a>Passaggio 3: Personalizzare il colore dell'intestazione

La pagina Web può fornire il colore che rappresenta l'identità del marchio da usare per l'intestazione della finestra di dialogo usando il tag meta mswebdialog-header-color.

``` syntax
<meta name="mswebdialog-header-color" content="#1267DF"/>
```

Il colore può essere qualsiasi valore specificato qui. Tuttavia, Il Gestore autenticazione Web ignorerà qualsiasi valore del canale alfa. Con questo colore in particolare e con i colori usati nella pagina in generale, è consigliabile seguire gli stessi colori usati nell'app Windows 8 del provider, se tale app esiste.

> [!Note]  
> Le icone e i colori vengono memorizzati nella cache per ogni server nel client dopo l'analisi dei tag META. Cancellare la cache del client prima di avviare l'interfaccia utente per l'applicazione delle modifiche. A tale scopo, modificare le impostazioni del Registro di sistema seguenti.

 

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

Una volta scaricata, un'icona non viene prelevata nuovamente per 24 ore. Per eseguire il test con le immagini del logo, impostare la chiave reg precedente con un valore inferiore.

### <a name="step-4-customize-the-web-page"></a>Passaggio 4: Personalizzare la pagina Web

Oltre a personalizzare l'interfaccia utente per la pagina Web, gli sviluppatori devono anche creare pagine Web senza problemi e integrate con l'esperienza Windows 8 generale. Ciò include l'uso degli stili consigliati, la verifica del funzionamento delle pagine Web con i dispositivi abilitati per il tocco e l'apertura di determinate pagine Web nel Web browser.

-   Stile

    È consigliabile usare lo stile consigliato qui per creare un'esperienza utente più coerente tra le pagine Web di Web Authentication Broker e altri componenti dell'interfaccia utente di Windows 8. La pagina Web deve usare uno sfondo bianco e nessun bordo. I pulsanti, ad esempio Login o Cancel, devono essere posizionati nell'angolo inferiore destro e usare lo stesso colore dell'intestazione. Infine, poiché Gestore autenticazione Web fornisce un pulsante Indietro, è consigliabile eliminare completamente un pulsante Annulla dalla pagina Web.

-   Abilitazione del tocco

    La pagina Web deve essere progettata in base all'interazione utente basata sul tocco. Per altre informazioni sulla progettazione per il tocco in Windows 8, vedere l'argomento [Progettazione dell'interazione tramite](https://msdn.microsoft.com/library/Hh465415(v=Win.10).aspx) tocco.

-   Personalizzazione della destinazione dei collegamenti ipertestuali

    Web Authentication Broker è ideale per la distribuzione di pagine Web che richiedono un'azione utente singola, ad esempio le pagine di accesso o di autorizzazione OAuth. Tuttavia, per flussi utente più complessi, ad esempio la creazione di un account, il ripristino da una password persa o dimenticata, la visualizzazione di informative sulla privacy e così via, in cui l'utente deve investire del tempo per comprendere e completare il flusso, è consigliabile avviare queste pagine nel browser preferito dell'utente per supportare la navigazione completa e l'esplorazione. Per impostazione predefinita, Web Authentication Broker non consente l'apertura di nuove finestre del browser da una pagina Web.Per altri dettagli, vedere la sezione No New windows By Default (Nessuna nuova finestra per impostazione predefinita). Tuttavia, usando il metatag `mswebdialog-newwindowurl` la pagina Web può dichiarare quali URL devono essere aperti nel browser.

    consente alla pagina Web di specificare un URL o una parte dell'URL che verrà utilizzato da Web Authentication Broker per la corrispondenza (corrispondenza tra stringhe a sinistra) ogni volta che viene richiesto di aprire un URL in una nuova finestra usando l'attributo di destinazione o il metodo `mswebdialog-newwindowurl` window.open(). Se è presente una corrispondenza, l'URL verrà aperto nel browser predefinito dell'utente. Se non è presente alcuna corrispondenza, Il Gestore autenticazione Web passa all'URL stesso (comportamento predefinito). Ad esempio:`<meta name="mswebdialog-newwindowurl" content="https://www.contoso.com/privacy"/>`

    Nel caso di questo metatag, Il Gestore autenticazione Web aprirà nel browser, ma https://www.contoso.com/privacy/policy.html passa direttamente a https://www.contoso.com/termsofuse.html . Si noti che i collegamenti che non tentano di aprire in una nuova finestra (ad esempio, i collegamenti che non usano l'attributo di destinazione o il metodo window.open() ) non sono interessati da questo meta tag. Il contenuto è un URL che può essere una pagina relativa o assoluta. Lo schema dell'URL può essere HTTP o HTTPS. È consigliabile definire i metatag per coprire tutti i collegamenti che non fanno parte del flusso utente principale, ad esempio le informative sulla privacy, i moduli di iscrizione `mswebdialog-newwindowurl` e così modo. Se si supporta l'accesso con un provider di autenticazione di terze parti(ad esempio, provider OpenID), assicurarsi di mantenere tali interazioni all'interno di Web Authentication Broker. Per consentire l'apertura sicura di tutti i collegamenti nella pagina nel browser, usare la sintassi a stella, ad esempio " " può essere usato solo esclusivamente e non può essere combinato con un altro URL, ad esempio " *" non è una sintassi `  <meta name="mswebdialog-newwindowurl" content="*"/>` \* https://www.contoso.com/\ valida.

### <a name="step-5-rules-applied-to-all-meta-tags"></a>Passaggio 5: Regole applicate a tutti i metatag

Quando Web Authentication Broker elabora i metatag, si applicano le regole seguenti:

-   L'effetto del tag meta verrà mantenuto in tutte le pagine nello stesso dominio di secondo livello (ad esempio, contoso.com), a meno che non venga rilevato un altro tag meta con lo stesso nome ma contenuto diverso.
-   Se nella stessa pagina vengono rilevati più metatag con lo stesso nome, Web Authentication Broker ne sceglierà solo uno e ignorerà il resto. Il metatag specifico scelto non è definito.
    > [!Note]  
    > Questa regola non si applica al `mswebdialog-newwindowurl` tag meta che consente più istanze nella stessa pagina.

     

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni relative allo sviluppo di pagine Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[App di esempio Web Authentication Broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
