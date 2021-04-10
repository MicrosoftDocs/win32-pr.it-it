---
title: Abilitazione degli stili di visualizzazione
description: In questo argomento viene illustrato come configurare l'applicazione per assicurarsi che i controlli comuni siano visualizzati nello stile di visualizzazione preferito dell'utente.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39339c0535767011a59730534486604389f62468
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963522"
---
# <a name="enabling-visual-styles"></a>Abilitazione degli stili di visualizzazione

In questo argomento viene illustrato come configurare l'applicazione per assicurarsi che i controlli comuni siano visualizzati nello stile di visualizzazione preferito dell'utente.

In questo argomento sono incluse le sezioni seguenti.

-   [Uso di manifesti o direttive per garantire che gli stili di visualizzazione possano essere applicati alle applicazioni](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [Uso di ComCtl32.dll versione 6 in un'applicazione che usa solo le estensioni standard](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [Uso di ComCtl32 versione 6 nel pannello di controllo o in una DLL eseguita da RunDll32.exe](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [Aggiunta del supporto dello stile di visualizzazione a un'estensione, un plug-in, uno snap-in MMC o una DLL introdotta in un processo](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [Disattivazione degli stili di visualizzazione](#turning-off-visual-styles)
-   [Uso degli stili di visualizzazione con contenuto HTML](#using-visual-styles-with-html-content)
-   [Quando gli stili visivi non vengono applicati](#when-visual-styles-are-not-applied)
-   [Compatibilità dell'applicazione con le versioni precedenti di Windows](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [Argomenti correlati](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a>Uso di manifesti o direttive per garantire che gli stili di visualizzazione possano essere applicati alle applicazioni

Per consentire all'applicazione di usare gli stili di visualizzazione, è necessario usare ComCtl32.dll versione 6 o successiva. Poiché la versione 6 non è ridistribuibile, è disponibile solo quando l'applicazione è in esecuzione in una versione di Windows che la contiene. Windows viene fornito sia con la versione 5 che con la versione 6. ComCtl32.dll versione 6 contiene sia i controlli utente che i controlli comuni. Per impostazione predefinita, le applicazioni usano i controlli utente definiti in User32.dll e i controlli comuni definiti in ComCtl32.dll versione 5. Per un elenco delle versioni di DLL e delle relative piattaforme di distribuzione, vedere [versioni di controllo comuni](common-control-versions.md).

Se si vuole che l'applicazione usi gli stili di visualizzazione, è necessario aggiungere un manifesto dell'applicazione o una direttiva del compilatore che indichi che è necessario usare ComCtl32.dll versione 6, se disponibile.

Un manifesto dell'applicazione consente a un'applicazione di specificare le versioni di un assembly richiesto. In Microsoft Win32, un assembly è un set di dll e un elenco di oggetti con versione che sono contenuti in tali dll.

I manifesti sono scritti in XML. Il nome del file manifesto dell'applicazione è il nome dell'eseguibile seguito dall'estensione del nome file. manifest; ad esempio, MyApp.exe. manifest. Il manifesto di esempio seguente mostra che la prima sezione descrive il manifesto stesso. La tabella seguente Mostra gli attributi impostati dall'elemento **assemblyIdentity** nella sezione Descrizione del manifesto.



| Attributo             | Descrizione                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| version               | Versione del manifesto. Il formato della versione deve essere Major. minor. Revision. Build (ovvero n. n. n. n, dove n <= 65535). |
| processorArchitecture | Processore per cui viene sviluppata l'applicazione.                                                                          |
| name                  | Include il nome della società, il nome del prodotto e il nome dell'applicazione.                                                                   |
| tipo                  | Tipo di applicazione, ad esempio Win32.                                                                                    |



 

Il manifesto di esempio fornisce anche una descrizione dell'applicazione e specifica le dipendenze dell'applicazione. Nella tabella seguente vengono illustrati gli attributi impostati dall'elemento **assemblyIdentity** nella sezione Dependency.



| Attributo             | Descrizione                                      |
|-----------------------|--------------------------------------------------|
| type                  | Tipo di componente di dipendenza, ad esempio Win32. |
| name                  | Nome del componente.                           |
| version               | Versione del componente.                        |
| processorArchitecture | Processore per il quale è stato progettato il componente.    |
| publicKeyToken        | Token di chiave utilizzato con il componente.              |
| Linguaggio              | Lingua del componente.                       |



 

Di seguito è riportato un esempio di file manifesto.

> [!IMPORTANT]
> Impostare la voce **processorArchitecture** su **"x86"** se l'applicazione è destinata alla piattaforma Windows a 32 bit o a **"amd64"** se l'applicazione è destinata alla piattaforma Windows a 64 bit. È anche possibile specificare **" \* "**, che garantisce la destinazione di tutte le piattaforme, come illustrato negli esempi seguenti.

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



Se si usa Microsoft Visual C++ 2005 o versione successiva, è possibile aggiungere la direttiva del compilatore seguente al codice sorgente anziché creare manualmente un manifesto. Per migliorare la leggibilità, la direttiva è suddivisa in più righe.


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



Negli argomenti seguenti vengono descritti i passaggi per l'applicazione degli stili di visualizzazione a diversi tipi di applicazioni. Si noti che il formato del manifesto è lo stesso in ogni caso.

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a>Uso di ComCtl32.dll versione 6 in un'applicazione che usa solo le estensioni standard

Di seguito sono riportati alcuni esempi di applicazioni che non utilizzano estensioni di terze parti.

-   Calcolatrice
-   FreeCell
-   Dragamine
-   Blocco note
-   Solitaire

**Per creare un manifesto e consentire all'applicazione di usare gli stili di visualizzazione.**

1.  Collegamento a ComCtl32. lib e chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Aggiungere un file denominato YourApp.exe. manifest all'albero di origine con formato manifesto XML.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  Aggiungere il manifesto al file di risorse dell'applicazione come segue:
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > Quando si aggiunge la voce precedente alla risorsa, è necessario formattarla in una sola riga. In alternativa, è possibile inserire il file manifesto XML nella stessa directory del file eseguibile dell'applicazione. Il sistema operativo caricherà il manifesto dal file system prima, quindi controlla la sezione delle risorse del file eseguibile. La versione del file system ha la precedenza.

     

Quando si compila l'applicazione, il manifesto verrà aggiunto come risorsa binaria.

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a>Uso di ComCtl32 versione 6 nel pannello di controllo o in una DLL eseguita da RunDll32.exe

**Per creare un manifesto e consentire all'applicazione di usare gli stili di visualizzazione.**

1.  Collegamento a ComCtl32. lib e chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Aggiungere un file denominato YourApp.cpl. manifest all'albero di origine con formato manifesto XML.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  Aggiungere il manifesto al file di risorse dell'applicazione come ID risorsa 123.

> [!Note]  
> Quando si crea un'applicazione del pannello di controllo, posizionarla nella categoria appropriata. Il pannello di controllo supporta ora la categorizzazione delle applicazioni del pannello di controllo. Ciò significa che alle applicazioni del pannello di controllo possono essere assegnati identificatori e suddivisi in aree attività, ad esempio installazione applicazioni, aspetto e temi oppure data, ora, lingua e opzioni internazionali.

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a>Aggiunta del supporto dello stile di visualizzazione a un'estensione, un plug-in, uno snap-in MMC o una DLL introdotta in un processo

Il supporto per gli stili visivi può essere aggiunto a un'estensione, a un plug-in, a uno snap-in MMC o a una DLL introdotta in un processo. Utilizzare, ad esempio, la procedura seguente per aggiungere il supporto degli stili di visualizzazione per uno snap-in di Microsoft Management Console (MMC).

1.  Compilare lo snap-in con il flag-DISOLATION \_ Aware \_ Enabled oppure inserire la seguente istruzione prima dell' \# istruzione include "Windows. h".

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    Per ulteriori informazioni sull' \_ \_ Abilitazione dell'isolamento, vedere [Isolating Components](/windows/desktop/SbsCs/isolating-components).

2.  Includere il file di intestazione del controllo comune nell'origine dello snap-in.
    ```C++
    #include <commctrl.h>
    ```

    

3.  Aggiungere un file denominato YourApp. manifest all'albero di origine che usa il formato manifesto XML.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  Aggiungere il manifesto al file di risorse dello snap-in. Per informazioni dettagliate sull'aggiunta di un manifesto a un file di risorse [, vedere uso di Comctl32 versione 6 in un'applicazione che usa estensioni, plug-in o una dll introdotta in un processo](/previous-versions//ms649781(v=vs.85)) .

## <a name="turning-off-visual-styles"></a>Disattivazione degli stili di visualizzazione

È possibile disattivare gli stili di visualizzazione per un controllo o per tutti i controlli in una finestra chiamando la funzione [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) nel modo seguente:


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



Nell'esempio precedente, *HWND* è l'handle della finestra in cui disabilitare gli stili di visualizzazione. Dopo la chiamata, viene eseguito il rendering del controllo senza stili di visualizzazione.

## <a name="using-visual-styles-with-html-content"></a>Uso degli stili di visualizzazione con contenuto HTML

Le pagine HTML che modificano le proprietà del Cascading Style Sheets (CSS), ad esempio sfondo o bordo, non dispongono di stili di visualizzazione applicati. Visualizzano l'attributo CSS specificato. Quando viene specificato come parte del contenuto, la maggior parte delle proprietà CSS si applicano agli elementi con stili di visualizzazione applicati.

Per impostazione predefinita, gli stili di visualizzazione vengono applicati ai controlli HTML intrinseci nelle pagine visualizzate in Microsoft Internet Explorer 6 e versioni successive. Per disattivare gli stili di visualizzazione per una pagina HTML, aggiungere un tag META al <head> . Questa tecnica si applica anche al contenuto incluso nel pacchetto come applicazioni HTML (HTA). Per disattivare gli stili di visualizzazione, il tag META deve essere il seguente:


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> Se l'impostazione del browser e l'impostazione del tag non accettano, la pagina non applica gli stili di visualizzazione. Se, ad esempio, il tag META è impostato su "No" e il browser è impostato per abilitare gli stili di visualizzazione, gli stili di visualizzazione non verranno applicati alla pagina. Tuttavia, se il browser o il tag META è impostato su "Sì" e l'altro elemento non è specificato, verranno applicati gli stili di visualizzazione.

 

Gli stili di visualizzazione potrebbero modificare il layout del contenuto. Inoltre, se si impostano determinati attributi nei controlli HTML intrinseci, ad esempio la larghezza di un pulsante, è possibile che l'etichetta del pulsante sia illeggibile in determinati stili di visualizzazione.

È necessario testare accuratamente il contenuto utilizzando gli stili di visualizzazione per determinare se l'applicazione di stili visivi ha un effetto negativo sul contenuto e sul layout.

## <a name="when-visual-styles-are-not-applied"></a>Quando gli stili visivi non vengono applicati

Per evitare di applicare stili di visualizzazione a una finestra di primo livello, assegnare alla finestra un'area non null (**SetWindowRgn**). Il sistema presuppone che una finestra con un'area non NULL sia una finestra specializzata che non usa gli stili di visualizzazione. Una finestra figlio associata a una finestra di primo livello degli stili non visivi può comunque applicare gli stili di visualizzazione anche se la finestra padre non lo è.

Se si desidera disabilitare l'utilizzo di stili di visualizzazione per tutte le finestre dell'applicazione, chiamare [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) e non passare il flag STAP \_ allow \_ nonclient. Se un'applicazione non chiama **SetThemeAppProperties**, i valori del flag presupposto sono STAP \_ allow \_ nonclient \| STAP \_ allow \_ Controls \| STAP \_ allow \_ WebContent. I valori ipotizzati provocano l'applicazione di uno stile di visualizzazione per l'area non client, i controlli e il contenuto Web.

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a>Compatibilità dell'applicazione con le versioni precedenti di Windows

Gran parte dell'architettura dello stile di visualizzazione è progettata per semplificare l'invio del prodotto a versioni precedenti di Windows che non supportano la modifica dell'aspetto dei controlli. Quando si distribuisce un'applicazione per più sistemi operativi, tenere presente quanto segue:

-   Nelle versioni di Windows precedenti a Windows 8, gli stili visivi sono spenti quando si verifica un contrasto elevato. Per supportare un contrasto elevato, un'applicazione legacy che supporta gli stili visivi deve fornire un percorso di codice separato per disegnare correttamente gli elementi dell'interfaccia utente con un contrasto elevato. In Windows 8, il contrasto elevato è una parte degli stili di visualizzazione. Tuttavia, un'applicazione di Windows 8, che include il GUID di Windows 8 nella sezione compatibilità del manifesto dell'applicazione, deve comunque fornire un percorso di codice separato per eseguire il rendering in modo corretto con un contrasto elevato in Windows 7 e versioni precedenti.
-   Se si usano le funzionalità di ComCtl32.dll versione 6, ad esempio la visualizzazione affiancata o il controllo collegamento, è necessario gestire il caso in cui tali controlli non sono disponibili nel computer dell'utente. ComCtl32.dll versione 6 non è ridistribuibile.
-   Testare l'applicazione per assicurarsi di non basarsi sulle funzionalità di ComCtl32.dll versione 6 senza prima verificare la versione corrente.
-   Non collegarsi a UxTheme. lib.
-   Scrivere il codice di gestione degli errori per le istanze quando gli stili di visualizzazione non funzionano come previsto.
-   L'installazione del manifesto dell'applicazione nelle versioni precedenti non influirà sul rendering dei controlli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stili di visualizzazione](themes-overview.md)
</dt> </dl>

 

 