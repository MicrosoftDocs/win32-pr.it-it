---
title: Abilitazione degli stili di visualizzazione
description: Questo argomento illustra come configurare l'applicazione per garantire che i controlli comuni siano visualizzati nello stile di visualizzazione preferito dell'utente.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4673d0a47f42f557e09f4afe46131cd48bad1b0
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102170"
---
# <a name="enabling-visual-styles"></a>Abilitazione degli stili di visualizzazione

Questo argomento illustra come configurare l'applicazione per garantire che i controlli comuni siano visualizzati nello stile di visualizzazione preferito dell'utente.

In questo argomento sono incluse le sezioni seguenti.

-   [Uso di manifesti o direttive per garantire che gli stili di visualizzazione possano essere applicati alle applicazioni](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [Uso ComCtl32.dll versione 6 in un'applicazione che usa solo estensioni standard](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [Uso di ComCtl32 versione 6 in Pannello di controllo o una DLL eseguita da RunDll32.exe](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [Aggiunta del supporto dello stile di visualizzazione a un'estensione, un plug-in, uno snap-in MMC o una DLL che viene portata in un processo](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [Disattivazione degli stili di visualizzazione](#turning-off-visual-styles)
-   [Uso degli stili di visualizzazione con contenuto HTML](#using-visual-styles-with-html-content)
-   [Quando gli stili di visualizzazione non vengono applicati](#when-visual-styles-are-not-applied)
-   [Rendere l'applicazione compatibile con le versioni precedenti di Windows](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [Argomenti correlati](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a>Uso di manifesti o direttive per garantire che gli stili di visualizzazione possano essere applicati alle applicazioni

Per consentire all'applicazione di usare gli stili di visualizzazione, è necessario usare ComCtl32.dll versione 6 o successiva. Poiché la versione 6 non è ridistribuibile, è disponibile solo quando l'applicazione è in esecuzione in una versione di Windows che la contiene. Windows viene fornito sia con la versione 5 che con la versione 6. ComCtl32.dll versione 6 contiene sia i controlli utente che i controlli comuni. Per impostazione predefinita, le applicazioni usano i controlli utente definiti in User32.dll e i controlli comuni definiti in ComCtl32.dll versione 5. Per un elenco delle versioni dll e delle relative piattaforme di distribuzione, vedere [Versioni di controllo comuni](common-control-versions.md).

Se si vuole che l'applicazione usi gli stili di visualizzazione, è necessario aggiungere un manifesto dell'applicazione o una direttiva del compilatore che indichi che è necessario usare ComCtl32.dll versione 6, se disponibile.

Un manifesto dell'applicazione consente a un'applicazione di specificare le versioni di un assembly necessarie. In Microsoft Win32 un assembly è un set di DLL e un elenco di oggetti versionable contenuti all'interno di tali DLL.

I manifesti vengono scritti in XML. Il nome del file manifesto dell'applicazione è il nome del file eseguibile seguito dall'estensione .manifest. ad esempio MyApp.exe.manifest. Il manifesto di esempio seguente mostra che la prima sezione descrive il manifesto stesso. Nella tabella seguente vengono illustrati gli attributi impostati **dall'elemento assemblyIdentity** nella sezione relativa alla descrizione del manifesto.



| Attributo             | Descrizione                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| version               | Versione del manifesto. La versione deve essere nel formato major.minor.revision.build, ovvero n.n.n.n.n, dove n <=65535). |
| processorArchitecture | Processore per cui viene sviluppata l'applicazione.                                                                          |
| name                  | Include il nome della società, il nome del prodotto e il nome dell'applicazione.                                                                   |
| tipo                  | Tipo dell'applicazione, ad esempio Win32.                                                                                    |



 

Il manifesto di esempio fornisce anche una descrizione dell'applicazione e specifica le dipendenze dell'applicazione. Nella tabella seguente vengono illustrati gli attributi impostati **dall'elemento assemblyIdentity** nella sezione dependency.



| Attributo             | Descrizione                                      |
|-----------------------|--------------------------------------------------|
| type                  | Tipo del componente di dipendenza, ad esempio Win32. |
| name                  | Nome del componente.                           |
| version               | Versione del componente.                        |
| processorArchitecture | Processore per cui è progettato il componente.    |
| Publickeytoken        | Token di chiave usato con questo componente.              |
| Linguaggio              | Lingua del componente.                       |



 

Di seguito è riportato un esempio di file manifesto.

> [!IMPORTANT]
> Impostare la voce **processorArchitecture** su **"X86"** se l'applicazione è destinata alla piattaforma Windows a 32 bit o **su "amd64"** se l'applicazione è destinata alla piattaforma Windows a 64 bit. È anche possibile specificare **" \* "**, che garantisce che tutte le piattaforme siano destinate, come illustrato negli esempi seguenti.

 


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



Se si usa Microsoft Visual C++ 2005 o versione successiva, è possibile aggiungere la direttiva del compilatore seguente al codice sorgente anziché creare manualmente un manifesto. Per motivi di leggibilità, la direttiva è suddivisa in diverse righe.


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



Negli argomenti seguenti vengono descritti i passaggi per l'applicazione di stili di visualizzazione a diversi tipi di applicazioni. Si noti che il formato del manifesto è lo stesso in ogni caso.

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a>Uso ComCtl32.dll versione 6 in un'applicazione che usa solo estensioni standard

Di seguito sono riportati esempi di applicazioni che non usano estensioni di terze parti.

-   Calcolatrice
-   FreeCell (in Windows Vista e Windows 7)
-   Minesweeper (in Windows Vista e Windows 7)
-   Blocco note
-   Solitaire (in Windows Vista e Windows 7)

**Per creare un manifesto e abilitare l'applicazione all'uso degli stili di visualizzazione.**

1.  Collegarsi a ComCtl32.lib e chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Aggiungere un file denominato YourApp.exe.manifest all'albero di origine con il formato manifesto XML.
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
    > Quando si aggiunge la voce precedente alla risorsa, è necessario formattarla in un'unica riga. In alternativa, è possibile inserire il file manifesto XML nella stessa directory del file eseguibile dell'applicazione. Il sistema operativo carica prima il manifesto dal file system, quindi controlla la sezione delle risorse del file eseguibile. La file system precedente ha la precedenza.

     

Quando si compila l'applicazione, il manifesto verrà aggiunto come risorsa binaria.

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a>Uso di ComCtl32 versione 6 in Pannello di controllo o una DLL eseguita da RunDll32.exe

**Per creare un manifesto e abilitare l'applicazione all'uso degli stili di visualizzazione.**

1.  Collegarsi a ComCtl32.lib e chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Aggiungere un file denominato YourApp.cpl.manifest all'albero di origine con il formato manifesto XML.
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
> Quando si crea un'Pannello di controllo, posizionarla nella categoria appropriata. Pannello di controllo ora supporta la categorizzazione Pannello di controllo applicazioni. Ciò significa che Pannello di controllo applicazioni possono essere assegnate identificatori e separate in aree attività come Installazione applicazioni, Aspetto e temi o Data, Ora, Lingua e Opzioni internazionali.

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a>Aggiunta del supporto dello stile di visualizzazione a un'estensione, un plug-in, uno snap-in MMC o una DLL che viene portata in un processo

È possibile aggiungere il supporto per gli stili di visualizzazione a un'estensione, a un plug-in, a uno snap-in MMC o a una DLL che viene portata in un processo. Ad esempio, usare la procedura seguente per aggiungere il supporto degli stili di visualizzazione per uno snap-in Microsoft Management Console (MMC).

1.  Compilare lo snap-in con il flag -DISOLATION AWARE ENABLED o inserire l'istruzione seguente prima dell'istruzione \_ \_ di inclusione \# "windows.h".

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    Per altre informazioni su ISOLATION \_ AWARE \_ ENABLED, vedere [Isolamento dei componenti](/windows/desktop/SbsCs/isolating-components).

2.  Includere il file di intestazione del controllo comune nell'origine snap-in.
    ```C++
    #include <commctrl.h>
    ```

    

3.  Aggiungere un file denominato YourApp.manifest all'albero di origine che usa il formato manifesto XML.
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

    

4.  Aggiungere il manifesto al file di risorse dello snap-in. Per informazioni dettagliate sull'aggiunta di un manifesto a un file di risorse, vedere Using [ComCtl32 Version 6 in an Application That Uses Extensions, Plug-ins, or a DLL That Is Brought into a Process (Uso di ComCtl32 versione 6 in](/previous-versions//ms649781(v=vs.85)) un'applicazione che usa estensioni, plug-in o DLL che vengono aggiunti a un processo) per informazioni dettagliate sull'aggiunta di un manifesto a un file di risorse.

## <a name="turning-off-visual-styles"></a>Disattivazione degli stili di visualizzazione

È possibile disattivare gli stili di visualizzazione per un controllo o per tutti i controlli in una finestra chiamando la [**funzione SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) come indicato di seguito:


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



Nell'esempio precedente *hwnd* è l'handle della finestra in cui disabilitare gli stili di visualizzazione. Dopo la chiamata, il rendering del controllo viene eseguito senza stili di visualizzazione.

## <a name="using-visual-styles-with-html-content"></a>Uso degli stili di visualizzazione con contenuto HTML

Alle pagine HTML che modificano le Cascading Style Sheets (CSS), ad esempio sfondo o bordo, non sono stati applicati stili di visualizzazione. Visualizzano l'attributo CSS specificato. Quando viene specificata come parte del contenuto, la maggior parte delle proprietà CSS si applica agli elementi a cui sono applicati stili di visualizzazione.

Per impostazione predefinita, gli stili di visualizzazione vengono applicati ai controlli HTML intrinseci nelle pagine visualizzate in Microsoft Internet Explorer 6 e versioni successive. Per disattivare gli stili di visualizzazione per una pagina HTML, aggiungere un tag META a <head> . Questa tecnica si applica anche al contenuto in pacchetto come applicazioni HTML (HTA). Per disattivare gli stili di visualizzazione, il tag META deve essere il seguente:


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> Se l'impostazione del browser e l'impostazione del tag non sono d'accordo, la pagina non applica gli stili di visualizzazione. Ad esempio, se il tag META è impostato su "no" e il browser è impostato per abilitare gli stili di visualizzazione, gli stili di visualizzazione non verranno applicati alla pagina. Tuttavia, se il browser o il tag META è impostato su "sì" e l'altro elemento non è specificato, verranno applicati gli stili di visualizzazione.

 

Gli stili di visualizzazione possono modificare il layout del contenuto. Inoltre, se si impostano determinati attributi su controlli HTML intrinseci, ad esempio la larghezza di un pulsante, è possibile che l'etichetta del pulsante sia illeggibile in determinati stili di visualizzazione.

È necessario testare accuratamente il contenuto usando gli stili di visualizzazione per determinare se l'applicazione di stili di visualizzazione ha un effetto negativo sul contenuto e sul layout.

## <a name="when-visual-styles-are-not-applied"></a>Quando gli stili di visualizzazione non vengono applicati

Per evitare di applicare gli stili di visualizzazione a una finestra di primo livello, assegnare alla finestra un'area non Null (**SetWindowRgn**). Il sistema presuppone che una finestra con un'area non NULL sia una finestra specializzata che non usa gli stili di visualizzazione. Una finestra figlio associata a una finestra di primo livello non di stili di visualizzazione può comunque applicare gli stili di visualizzazione anche se la finestra padre non lo fa.

Se si vuole disabilitare l'uso degli stili di visualizzazione per tutte le finestre nell'applicazione, chiamare [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) e non passare il flag STAP \_ ALLOW \_ NONCLIENT. Se un'applicazione non chiama **SetThemeAppProperties,** i valori del flag presunti sono STAP \_ ALLOW \_ NONCLIENT \| STAP \_ ALLOW CONTROLS \_ \| STAP ALLOW \_ \_ WEBCONTENT. I valori presunti determinano l'applicazione di uno stile di visualizzazione all'area non client, ai controlli e al contenuto Web.

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a>Rendere l'applicazione compatibile con le versioni precedenti di Windows

Gran parte dell'architettura dello stile di visualizzazione è progettata per semplificare la spedizione del prodotto nelle versioni precedenti di Windows che non supportano la modifica dell'aspetto dei controlli. Quando si spediva un'applicazione per più di un sistema operativo, tenere presente quanto segue:

-   Nelle versioni di Windows precedenti a Windows 8, gli stili di visualizzazione sono disattivati quando il contrasto elevato è on. Per supportare il contrasto elevato, un'applicazione legacy che supporta gli stili di visualizzazione deve fornire un percorso di codice separato per disegnare correttamente gli elementi dell'interfaccia utente a contrasto elevato. In Windows 8, il contrasto elevato fa parte degli stili di visualizzazione. Tuttavia, un'applicazione Windows 8 (che include il GUID Windows 8 nella sezione di compatibilità del manifesto dell'applicazione) deve comunque fornire un percorso di codice separato per il corretto rendering a contrasto elevato in Windows 7 in precedenza.
-   Se si usano le funzionalità di ComCtl32.dll versione 6, ad esempio la visualizzazione affiancata o il controllo collegamento, è necessario gestire il caso in cui tali controlli non sono disponibili nel computer dell'utente. ComCtl32.dll versione 6 non è ridistribuibile.
-   Testare l'applicazione per assicurarsi di non basarsi sulle funzionalità di ComCtl32.dll versione 6 senza prima verificare la versione corrente.
-   Non collegarsi a UxTheme.lib.
-   Scrivere codice di gestione degli errori per le istanze quando gli stili di visualizzazione non funzionano come previsto.
-   L'installazione del manifesto dell'applicazione nelle versioni precedenti non influisce sul rendering dei controlli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stili di visualizzazione](themes-overview.md)
</dt> </dl>

 

 
