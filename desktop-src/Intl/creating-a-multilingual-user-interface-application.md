---
description: Questa esercitazione illustra come prendere un'applicazione monolingue e renderla pronta al mondo. Questa applicazione è sotto forma di una soluzione completa compilata all'interno di Microsoft Visual Studio.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Aggiunta interfaccia utente multilingue a un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5ca1ddba2574610cde1f375f7fab2b07461008665f2092c9c8e88ae9b51f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147694"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a>Aggiunta interfaccia utente multilingue a un'applicazione

Questa esercitazione illustra come prendere un'applicazione monolingue e renderla pronta al mondo. Questa applicazione è sotto forma di una soluzione completa compilata all'interno di Microsoft Visual Studio.

-   [Overview](#splitting-the-various-language-resource-modules-an-overview)
    -   [L'idea alla base di Hello MUI](#the-idea-behind-hello-mui)
-   [Configurazione della soluzione Hello MUI](#setting-up-the-hello-mui-solution)
    -   [Requisiti della piattaforma](#platform-requirements)
    -   [Prerequisiti](#prerequisites)
-   [Passaggio 0: Creazione di Hello MUI hard-coded](#step-0-creating-the-hard-coded-hello-mui)
-   [Passaggio 1: Implementazione del modulo delle risorse di base](#step-1-implementing-the-basic-resource-module)
-   [Passaggio 2: Compilazione del modulo delle risorse di base](#step-2-building-the-basic-resource-module)
    -   [Suddivisione dei vari moduli delle risorse linguistiche: panoramica](#splitting-the-various-language-resource-modules-an-overview)
    -   [Suddivisione dei vari moduli di risorse linguistici: creazione dei file](#splitting-the-various-language-resource-modules-creating-the-files)
-   [Passaggio 3: Creazione di un Resource-Savvy "Hello MUI"](#step-3-creating-a-resource-savvy-hello-mui)
-   [Passaggio 4: Globalizzazione di "Hello MUI"](#step-4-globalizing-hello-mui)
-   [Passaggio 5: Personalizzazione di "Hello MUI"](#step-5-customizing-hello-mui)
-   [Considerazioni aggiuntive per MUI](#additional-considerations-for-mui)
    -   [Supporto per le applicazioni console](#support-for-console-applications)
    -   [Determinazione dei linguaggi da supportare in fase di esecuzione](#determination-of-languages-to-support-at-run-time)
    -   [Supporto di script complessi nelle versioni precedenti a Windows Vista](#complex-script-support-in-versions-prior-to-windows-vista)
-   [Summary](#summary)

## <a name="overview"></a>Panoramica

A partire da Windows Vista, il sistema operativo Windows è stato creato da zero per essere una piattaforma multilingue, con supporto aggiuntivo che consente di creare applicazioni multilingue che usano il modello di risorse MUI Windows.

Questa esercitazione illustra questo nuovo supporto per le applicazioni multilingue, coprendo gli aspetti seguenti:

-   Usa il supporto migliorato della piattaforma MUI per abilitare facilmente le applicazioni multilingue.
-   Estende le applicazioni multilingue per l'esecuzione in versioni di Windows precedenti Windows Vista.
-   Vengono toccate le considerazioni aggiuntive relative allo sviluppo di applicazioni multilingue specializzate, ad esempio applicazioni console.

Questi collegamenti consentono di aggiornare rapidamente i concetti relativi all'internazionalizzazione e a MUI:

-   [Panoramica rapida dell'internazionalizzazione.](understanding-internationalization.md)
-   [Concetti di MUI](understanding-mui.md).
-   [Uso di MUI per sviluppare applicazioni Win32.](using-multilingual-user-interface.md)

### <a name="the-idea-behind-hello-mui"></a>L'idea alla base di Hello MUI

Probabilmente si ha familiarità con l'applicazione Hello World classica, che illustra i concetti di programmazione di base. Questa esercitazione adotta un approccio simile per illustrare come usare il modello di risorse MUI per aggiornare un'applicazione monolingue per creare una versione multilingue denominata Hello MUI.

> [!Note]  
> Le attività di questa esercitazione sono descritte in passaggi dettagliati a causa della precisione con cui queste attività devono essere eseguite e della necessità di spiegare i dettagli agli sviluppatori che hanno poco esperienza con queste attività.

 

## <a name="setting-up-the-hello-mui-solution"></a>Configurazione della soluzione Hello MUI

Questi passaggi illustrano come preparare la creazione della soluzione Hello MUI.

### <a name="platform-requirements"></a>Requisiti della piattaforma

È necessario compilare gli esempi di codice di questa esercitazione usando Windows Software Development Kit (SDK) per Windows 7 e Visual Studio 2008. Windows 7 SDK verrà installato in Windows XP, Windows Vista e Windows 7 e la soluzione di esempio può essere compilata in una qualsiasi di queste versioni del sistema operativo.

Tutti gli esempi di codice di questa esercitazione sono progettati per essere eseguiti nelle versioni x86 e x64 di Windows XP, Windows Vista e Windows 7. Le parti specifiche che non funzioneranno in Windows XP vengono chiamate laddove appropriato.

### <a name="prerequisites"></a>Prerequisiti

1.  Installare Visual Studio 2008.

    Per altre informazioni, vedere [l'Visual Studio Developer Center.](https://msdn.microsoft.com/vstudio/default.aspx)

2.  Installare Windows SDK per Windows 7.

    È possibile installarlo dalla pagina Windows SDK di [Windows Developer Center.](https://msdn.microsoft.com/windowsserver/bb980924.aspx) L'SDK include utilità per sviluppare applicazioni per le versioni del sistema operativo a partire da Windows XP fino alle versioni più recenti.

    > [!Note]  
    > Se il pacchetto non viene installato nel percorso predefinito o se non si sta installando nell'unità di sistema, che in genere è l'unità C, prendere nota del percorso di installazione.

     

3.  Configurare i parametri Visual Studio della riga di comando.

    1.  Aprire una finestra Visual Studio comandi.
    2.  Digitare **set path**.
    3.  Verificare che la variabile path includa il percorso della cartella bin dell'SDK Windows 7: ... Microsoft SDK Windows \\ bin \\ v7.0 \\

4.  Installare il pacchetto aggiuntivo api di livello inferiore microsoft NLS.
    > [!Note]  
    > Nel contesto di questa esercitazione, questo pacchetto è necessario solo se si personalizza l'applicazione per l'esecuzione Windows versioni precedenti a Windows Vista. Vedere [Passaggio 5: Personalizzazione di Hello MUI.](#step-5-customizing-hello-mui)

     

    1.  Scaricare e installare il pacchetto dal sito [di download.](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en)
    2.  Come con Windows SDK, se non si installa il pacchetto nel percorso predefinito o se non si sta installando nell'unità di sistema, che in genere è l'unità C, prendere nota del percorso di installazione.
    3.  Se la piattaforma di sviluppo Windows XP o Windows Server 2003, verificare che Nlsdl.dll installato e registrato correttamente.

        1.  Passare alla cartella "redist" nel percorso di installazione.
        2.  Eseguire il file Nlsdl ridistribuibile appropriato. \*.exe, ad esempio nlsdl.x86.exe. Questo passaggio installa e registra Nlsdl.dll.

    > [!Note]  
    > Se si sviluppa un'applicazione che usa MUI e che deve essere eseguita Windows versioni precedenti Windows Vista, Nlsdl.dll deve essere presente nella piattaforma Windows di destinazione. Nella maggior parte dei casi, ciò significa che l'applicazione deve portare e installare il programma di installazione Nlsdl ridistribuibile (e non semplicemente copiare Nlsdl.dll se stessa).

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a>Passaggio 0: Creazione di Hello MUI hard-coded

Questa esercitazione inizia con la versione monolingue dell'applicazione Hello MUI. L'applicazione presuppone l'uso del linguaggio di programmazione C++, delle stringhe di caratteri wide e della [**funzione MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) per l'output.

Per iniziare, creare l'applicazione GuiStep 0 iniziale e la soluzione HelloMUI, che contiene tutte le \_ applicazioni di questa esercitazione.

1.  In Visual Studio 2008 creare un nuovo progetto. Usare le impostazioni e i valori seguenti:

    1.  Project tipo: in Visual C++ selezionare Win32 e quindi in Visual Studio modelli installati selezionare Win32 Project.
    2.  Nome: GuiStep \_ 0.
    3.  Percorso: *ProjectRootDirectory (i* passaggi successivi fanno riferimento a questa directory).
    4.  Nome soluzione: HelloMUI.
    5.  Selezionare Crea directory per soluzione.
    6.  Nella Creazione guidata applicazione Win32 selezionare il tipo di applicazione predefinito: Windows applicazione.

2.  Configurare il modello di threading del progetto:

    1.  Nella finestra Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto GuiStep \_ 0 e quindi scegliere Proprietà.
    2.  Nella finestra di dialogo Pagine delle proprietà del progetto:

        1.  Nell'elenco a discesa in alto a sinistra impostare Configurazione su Tutte le configurazioni.
        2.  In Proprietà di configurazione espandere C/C++, selezionare Generazione di codice e impostare Libreria di runtime: Debug multi-thread (/MTd).

3.  Sostituire il contenuto di GuiStep \_ 0.cpp con il codice seguente:
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  Compilare ed eseguire l'applicazione.

Il codice sorgente semplice precedente consente di scegliere la progettazione semplicistica della codifica hard-code o dell'incorporamento, tutto l'output visualizzato dall'utente, in questo caso il testo "Hello MUI". Questa scelta limita l'utilità dell'applicazione per gli utenti che non riconoscono la parola inglese "Hello". Poiché MUI è un acronimo inglese basato sulla tecnologia, per questa esercitazione si presuppone che la stringa rimanga "MUI" per tutte le lingue.

## <a name="step-1-implementing-the-basic-resource-module"></a>Passaggio 1: Implementazione del modulo delle risorse di base

Microsoft Win32 ha esposto da tempo la possibilità per gli sviluppatori di applicazioni di separare i dati delle risorse dell'interfaccia utente dal codice sorgente dell'applicazione. Questa separazione si presenta sotto forma di modello di risorsa Win32, in cui stringhe, bitmap, icone, messaggi e altri elementi normalmente visualizzati a un utente vengono compressi in una sezione distinta del file eseguibile, separato dal codice eseguibile.

Per illustrare questa separazione tra il codice eseguibile e la creazione di pacchetti di dati delle risorse, in questo passaggio l'esercitazione inserisce la stringa "Hello" (la risorsa "en-US" precedentemente hard-coded) nella sezione delle risorse di un modulo DLL nel progetto HelloModule \_ en \_ us.

Questa DLL Win32 può contenere anche funzionalità eseguibili di tipo libreria (come qualsiasi altra DLL). Tuttavia, per concentrarsi sugli aspetti relativi alle risorse Win32, il codice DLL di run-time viene lasciato in stubb in dllmain.cpp. Le sezioni successive di questa esercitazione usano i dati delle risorse HelloModule compilati qui e presentano anche il codice di runtime appropriato.

Per costruire un modulo di risorsa Win32, iniziare creando una DLL con una dllmain stubbed:

1.  Aggiungere un nuovo progetto alla soluzione HelloMUI:

    1.  Scegliere Aggiungi dal menu File e quindi Nuovo Project.
    2.  Project tipo: Win32 Project.
    3.  Nome: HelloModule \_ en \_ us.
    4.  Percorso: *ProjectRootDirectory* \\ HelloMUI.
    5.  Nella Creazione guidata applicazione Win32 selezionare Tipo di applicazione: DLL.

2.  Configurare il modello di threading di questo progetto:

    1.  Nella finestra Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto HelloModule \_ en us e scegliere \_ Proprietà.
    2.  Nella finestra di dialogo Pagine delle proprietà del progetto:

        1.  Nell'elenco a discesa in alto a sinistra impostare Configurazione su Tutte le configurazioni.
        2.  In Proprietà di configurazione espandere C/C++, selezionare Generazione di codice e impostare Libreria di runtime: Debug multi-thread (/MTd).

3.  Esaminare dllmain.cpp. Può essere necessario aggiungere UNREFERENCED \_ Macro PARAMETER per il codice generato, come qui, per consentire la compilazione al livello di avviso 4.
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  Aggiungere un file di definizione delle risorse HelloModule.rc al progetto:

    1.  Nel progetto HelloModule en us fare clic con il pulsante destro del mouse sulla cartella File di risorse e scegliere \_ Aggiungi e quindi Nuovo \_ elemento.
    2.  Nella finestra di dialogo Aggiungi nuovo elemento scegliere quanto segue:

        1.  Categorie: in Visual C++ selezionare Risorsa e quindi in "Visual Studio modelli installati" selezionare File di risorse (.rc).
        2.  Nome: HelloModule.
        3.  Località: accettare il valore predefinito.
        4.  Fare clic su Aggiungi.

    3.  Specificare che il nuovo file HelloModule.rc deve essere salvato come Unicode:

        1.  Nella finestra Esplora soluzioni fare clic con il pulsante destro del mouse su HelloModule.rc e scegliere Visualizza codice.
        2.  Se viene visualizzato un messaggio che indica che il file è già aperto e chiede se si vuole chiuderlo, fare clic su Sì.
        3.  Con il file visualizzato come testo, selezionare file dal menu e quindi Opzioni di salvataggio avanzate.
        4.  In Codifica specificare Unicode - Tabella codici 1200.
        5.  Fare clic su OK.
        6.  Salvare e chiudere HelloModule.rc.

    4.  Aggiungere una tabella di stringhe contenente la stringa "Hello":

        1.  Nella finestra Visualizzazione risorse fare clic con il pulsante destro del mouse su HelloModule.rc e scegliere Aggiungi risorsa.
        2.  Selezionare Tabella di stringhe.
        3.  Fare clic su New.
        4.  Aggiungere una stringa alla tabella di stringhe:

            1.  ID: HELLO \_ MUI \_ STR \_ 0.
            2.  Valore: 0
            3.  Didascalia: Hello.

        Se si visualizza HelloModule.rc come testo, verranno visualizzate varie parti di codice sorgente specifiche della risorsa. Quella di maggiore interesse è la sezione che descrive la stringa "Hello":

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        Questa stringa "Hello" è la risorsa che deve essere localizzata (ovvero tradotta) in ogni lingua che l'applicazione spera di supportare. Ad esempio, helloModule ta nel progetto (che verrà creato nel passaggio successivo) conterrà la propria versione localizzata di \_ \_ HelloModule.rc per "ta-IN":

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  Compilare il progetto HelloModule \_ en us per assicurarsi che non siano presenti \_ errori.

5.  Creare altri sei progetti nella soluzione HelloMUI (o il numero desiderato) per creare altre sei DLL di risorse per linguaggi aggiuntivi. Usare i valori in questa tabella:

    | Project name (Nome progetto)        | Nome del file RC | ID stringa          | Valore stringa | Didascalia della stringa |
    |---------------------|------------------|--------------------|--------------|----------------|
    | HelloModule \_ de \_ de | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | Hallo          |
    | HelloModule \_ \_ es es | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | Hola           |
    | HelloModule \_ fr \_ fr | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | Bonjour        |
    | HelloModule \_ hi \_ in | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | नमस्           |
    | HelloModule \_ ru \_ ru | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | Здравствуйте   |
    | HelloModule \_ ta \_ in | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | வணக்கம்        |

    

     

Per altre informazioni sulla sintassi e sulla struttura dei file RC, vedere [Informazioni sui file di risorse](../menurc/about-resource-files.md).

## <a name="step-2-building-the-basic-resource-module"></a>Passaggio 2: Compilazione del modulo delle risorse di base

Usando i modelli di risorse precedenti, la compilazione di uno dei sette progetti HelloModule comporta sette DLL separate. Ogni DLL conterrà una sezione di risorse con una singola stringa localizzata nella lingua appropriata. Anche se appropriata per lo storico modello di risorse Win32, questa progettazione non sfrutta MUI.

In Vista SDK Windows e versioni successive, MUI offre la possibilità di suddividere i file eseguibili in moduli di codice sorgente e contenuto localizzabile. Con l'ulteriore personalizzazione trattata più avanti nel passaggio 5, le applicazioni possono essere abilitate per il supporto multilingue per l'esecuzione nelle versioni precedenti a Windows Vista.

I meccanismi principali disponibili per suddividere le risorse dal codice eseguibile, a partire Windows Vista, sono:

-   Uso rc.exe (compilatore RC) con opzioni specifiche o
-   Uso di uno strumento di suddivisione dello stile post-compilazione denominato muirct.exe.

Per [altre informazioni, vedere Utilità](resource-utilities.md) risorse.

Per motivi di semplicità, questa esercitazione usa muirct.exe per dividere il file eseguibile "Hello MUI".

### <a name="splitting-the-various-language-resource-modules-an-overview"></a>Suddivisione dei vari moduli delle risorse linguistiche: panoramica

Un processo in più parti è coinvolto nella suddivisione delle DLL in un unico HelloModule.dll eseguibile, oltre a HelloModule.dll.mui per ognuna delle sette lingue supportate in questa esercitazione. Questa panoramica descrive i passaggi necessari. La sezione successiva presenta un file di comando che esegue questi passaggi.

Per prima cosa, dividere il modulo solo inglese HelloModule.dll usando il comando :


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



La riga di comando precedente usa il file di configurazione DoReverseMuiLoc.rcconfig. Questo tipo di file di configurazione viene in genere usato da muirct.exe per dividere le risorse tra la DLL indipendente dalla lingua (LN) e i file mui dipendenti dalla lingua. In questo caso, il file xml DoReverseMuiLoc.rcconfig (elencato nella sezione successiva) indica molti tipi di risorse, ma rientrano tutti nella categoria di file "localizedResources" o .mui e non sono presenti risorse nella categoria indipendente dalla lingua. Per altre informazioni su come preparare un file di configurazione delle risorse, vedere [Preparazione di un file di configurazione delle risorse](preparing-a-resource-configuration-file.md).

Oltre a creare un file HelloModule.dll.mui che contiene la stringa inglese "Hello", muirct.exe incorpora anche una risorsa MUI nel modulo HelloModule.dll durante la suddivisione. Per caricare correttamente in fase di esecuzione le risorse appropriate dai moduli HelloModule.dll.mui specifici del linguaggio, ogni file mui deve avere i checksum corretti in modo che corrispondano ai checksum nel modulo LN indipendente dal linguaggio di base. Questa operazione viene eseguita da un comando come:


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



Analogamente, muirct.exe viene richiamato per creare un file HelloModule.dll.mui per ognuna delle altre lingue. In questi casi, tuttavia, la DLL indipendente dalla lingua viene eliminata, perché sarà necessaria solo la prima creata. I comandi che elaborano le risorse spagnolo e francese sono simili ai seguenti:


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



Uno degli aspetti più importanti da notare nelle righe muirct.exe comando precedenti è che il flag -x viene usato per specificare un ID lingua di destinazione. Il valore fornito a muirct.exe è diverso per ogni modulo specifico HelloModule.dll linguaggio. Questo valore di lingua è centrale e viene usato dal muirct.exe per contrassegnare in modo appropriato il file mui durante la suddivisione. Un valore non corretto genera errori di caricamento delle risorse per quel particolare file mui in fase di esecuzione. Per [altre informazioni sul](language-identifier-constants-and-strings.md) mapping del nome della lingua a LCID, vedere Costanti e stringhe dell'identificatore di lingua.

Ogni file con estensione mui suddiviso viene inserito in una directory corrispondente al nome della lingua, immediatamente sotto la directory in cui risiederà l'HelloModule.dll indipendente dalla lingua. Per altre informazioni sul posizionamento dei file con estensione mui, vedere [Distribuzione di applicazioni](application-deployment.md).

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a>Suddivisione dei vari moduli di risorse linguistici: creazione dei file

Per questa esercitazione si crea un file di comando contenente i comandi per suddividere le varie DLL e lo si richiama manualmente. Si noti che nel lavoro di sviluppo effettivo è possibile ridurre il potenziale di errori di compilazione includendo questi comandi come eventi di pre-compilazione o post-compilazione nella soluzione HelloMUI, ma questo non è compreso nell'ambito di questa esercitazione.

Creare i file per la build di debug:

1.  Creare un file di comando DoReverseMuiLoc.cmd contenente i comandi seguenti:
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  Creare un file xml DoReverseMuiLoc.rcconfig contenente le righe seguenti:
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  Copiare DoReverseMuiLoc.cmd e DoReverseMuiLoc.rcconfig in *ProjectRootDirectory* \\ HelloMUI \\ Debug.
4.  Aprire il Visual Studio prompt dei comandi di Visual Studio 2008 e passare alla directory Debug.
5.  Eseguire DoReverseMuiLoc.cmd.

Quando si crea una build di versione, copiare gli stessi file DoReverseMuiLoc.cmd e DoReverseMuiLoc.rcconfig nella directory Release ed eseguire il file di comando.

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a>Passaggio 3: Creazione di un Resource-Savvy "Hello MUI"

Sulla base dell'esempio iniziale hard-coded GuiStep0.exe riportato sopra, è possibile estendere la portata dell'applicazione a più utenti del linguaggio scegliendo di incorporare il modello di risorsa \_ Win32. Il nuovo run-time code presentato in questo passaggio include la logica di caricamento del modulo ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) e il recupero di stringhe ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)).

1.  Aggiungere un nuovo progetto alla soluzione HelloMUI (usando la selezione di menu File, Aggiungi e Nuovo Project) con le impostazioni e i valori seguenti:

    1.  Project tipo: Win32 Project.
    2.  Nome: GuiStep \_ 1.
    3.  Località: accettare il valore predefinito.
    4.  Nella Creazione guidata applicazione Win32 selezionare il tipo di applicazione predefinito: Windows applicazione.

2.  Impostare questo progetto per l'esecuzione dall'Visual Studio e configurare il relativo modello di threading:

    1.  Nella finestra Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto GuiStep 1 e scegliere \_ Imposta come avvio Project.
    2.  Fare di nuovo clic con il pulsante destro del mouse e scegliere Proprietà.
    3.  Nella finestra di dialogo Pagine delle proprietà del progetto:

        1.  Nell'elenco a discesa in alto a sinistra impostare Configurazione su Tutte le configurazioni.
        2.  In Proprietà di configurazione espandere C/C++, selezionare Generazione di codice e impostare Libreria di runtime: Debug multi-thread (/MTd).

3.  Sostituire il contenuto di GuiStep \_ 1.cpp con il codice seguente:
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  Compilare ed eseguire l'applicazione. L'output verrà visualizzato nella lingua attualmente impostata come lingua di visualizzazione del computer (purché sia una delle sette lingue compilate).

## <a name="step-4-globalizing-hello-mui"></a>Passaggio 4: Globalizzazione di "Hello MUI"

Anche se l'esempio precedente è in grado di visualizzare l'output in lingue diverse, non rientra in una serie di aree. La cosa più evidente è che l'applicazione è disponibile solo in un piccolo subset di lingue rispetto al Windows sistema operativo stesso. Se, ad esempio, l'applicazione GuiStep 1 del passaggio precedente fosse installata in una build giapponese di Windows, è probabile che si siano verificati errori di posizione \_ delle risorse.

Per risolvere questa situazione, sono disponibili due opzioni principali:

-   Assicurarsi che le risorse in un linguaggio di fallback finale predeterminato siano incluse.
-   Consente all'utente finale di configurare le preferenze di lingua tra il subset di lingue specificamente supportate dall'applicazione.

Tra queste opzioni, quella che fornisce un linguaggio di fallback finale è altamente consigliabile e viene implementata in questa esercitazione passando il flag -g a muirct.exe, come illustrato in precedenza. Questo flag indica muirct.exe di rendere una lingua specifica (de-DE/0x0407) la lingua di fallback finale associata al modulo dll indipendente dalla lingua (HelloModule.dll). In fase di esecuzione questo parametro viene usato come ultima risorsa per generare testo da visualizzare all'utente. Se non viene trovata una lingua di fallback finale e non è disponibile alcuna risorsa appropriata nel file binario indipendente dalla lingua, il caricamento della risorsa ha esito negativo. È quindi necessario determinare con attenzione gli scenari che l'applicazione potrebbe incontrare e pianificare di conseguenza il linguaggio di fallback finale.

L'altra opzione che consente preferenze linguistiche configurabili e il caricamento delle risorse in base a questa gerarchia definita dall'utente può aumentare notevolmente la soddisfazione dei clienti. Sfortunatamente, complica anche le funzionalità necessarie all'interno dell'applicazione.

Questo passaggio dell'esercitazione usa un meccanismo di file di testo semplificato per abilitare la configurazione personalizzata della lingua utente. Il file di testo viene analizzato in fase di esecuzione dall'applicazione e l'elenco di linguaggi analizzato e convalidato viene usato per stabilire un elenco di fallback personalizzato. Dopo aver stabilito l'elenco di fallback personalizzato, le API Windows caricano le risorse in base alla precedenza della lingua specificata in questo elenco. Il resto del codice è simile a quello trovato nel passaggio precedente.

1.  Aggiungere un nuovo progetto alla soluzione HelloMUI (usando la selezione di menu File, Aggiungi e Nuovo Project) con le impostazioni e i valori seguenti:

    1.  Project tipo: Win32 Project.
    2.  Nome: GuiStep \_ 2.
    3.  Località: accettare il valore predefinito.
    4.  Nella Creazione guidata applicazione Win32 selezionare il tipo di applicazione predefinito: Windows applicazione.

2.  Impostare questo progetto per l'esecuzione dall'Visual Studio e configurare il relativo modello di threading:

    1.  Nella finestra Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto GuiStep 2 e scegliere \_ Imposta come avvio Project.
    2.  Fare di nuovo clic con il pulsante destro del mouse e scegliere Proprietà.
    3.  Nella finestra di dialogo Pagine delle proprietà del progetto:

        1.  Nell'elenco a discesa in alto a sinistra impostare Configurazione su Tutte le configurazioni.
        2.  In Proprietà di configurazione espandere C/C++, selezionare Generazione di codice e impostare Libreria di runtime: Debug multi-thread (/MTd).

3.  Sostituire il contenuto di GuiStep \_ 2.cpp con il codice seguente:
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  Creare un file di testo Unicode langs.txt contenente la riga seguente:

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > Assicurarsi di salvare il file come Unicode.

     

    Copiare langs.txt nella directory da cui verrà eseguito il programma:

    -   Se viene eseguito dall'Visual Studio, copiarlo in *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2.
    -   Se è in esecuzione Windows Explorer, copiarlo nella stessa directory di GuiStep \_2.exe.

5.  Compilare ed eseguire il progetto. Provare a langs.txt in modo che lingue diverse vengano visualizzate all'inizio dell'elenco.

## <a name="step-5-customizing-hello-mui"></a>Passaggio 5: Personalizzazione di "Hello MUI"

Alcune delle funzionalità di run-time indicate finora in questa esercitazione sono disponibili solo in Windows Vista e versioni successive. È possibile usare di nuovo lo sforzo investito per la localizzazione e la suddivisione delle risorse rendendo l'applicazione di livello inferiore Windows versioni del sistema operativo, ad esempio Windows XP. Questo processo comporta la modifica dell'esempio precedente in due aree chiave:

-   Le funzioni di caricamento delle risorse Windows Vista di pre-installazione (ad esempio [**LoadString,**](/windows/win32/api/winuser/nf-winuser-loadstringa) [**LoadIcon,**](/windows/win32/api/winuser/nf-winuser-loadicona) [**LoadBitmap,**](/windows/win32/api/winuser/nf-winuser-loadbitmapa) [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)e altre) non sono compatibili con MUI. Le applicazioni che vengono distribuite con risorse suddivise (file LN e mui) devono caricare moduli di risorse usando una di queste due funzioni:

    -   Se l'applicazione deve essere eseguita solo in Windows Vista e versioni successive, deve caricare i moduli di risorse [**con LoadLibraryEx.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)
    -   Se l'applicazione deve essere eseguita in versioni precedenti a Windows Vista e Windows Vista o versioni successive, deve usare [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), che è una funzione di livello inferiore specifica fornita in Windows 7 SDK.

-   Il supporto per la gestione della lingua e l'ordine di fallback della lingua offerti nelle versioni precedenti Windows Vista del sistema operativo Windows è significativamente diverso da quello in Windows Vista e versioni successive. Per questo motivo, le applicazioni che consentono il fallback della lingua configurato dall'utente devono modificare le procedure di gestione della lingua:

    -   Se l'applicazione deve essere eseguita solo Windows Vista e versioni successive, è sufficiente impostare l'elenco delle lingue usando [**SetThreadPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)
    -   Se l'applicazione deve essere eseguita in tutte le versioni Windows, è necessario costruire codice che verrà eseguito su piattaforme di livello inferiore per scorrere l'elenco di lingue configurato dall'utente e il probe per il modulo di risorse desiderato. Questa operazione può essere illustrata nelle sezioni 1c e 2 del codice fornito più avanti in questo passaggio.

Creare un progetto in grado di usare i moduli di risorse localizzati in qualsiasi versione di Windows:

1.  Aggiungere un nuovo progetto alla soluzione HelloMUI (usando la selezione di menu File, Aggiungi e Nuovo Project) con le impostazioni e i valori seguenti:

    1.  Project tipo: Win32 Project.
    2.  Nome: GuiStep \_ 3.
    3.  Località: accettare il valore predefinito.
    4.  Nella Creazione guidata applicazione Win32 selezionare il tipo di applicazione predefinito: Windows applicazione.

2.  Impostare questo progetto per l'esecuzione dall'Visual Studio e configurare il relativo modello di threading. Configurarlo anche per aggiungere le intestazioni e le librerie necessarie.

    > [!Note]  
    > I percorsi usati in questa esercitazione presuppongono che l'SDK Windows 7 e il pacchetto di API di livello inferiore Microsoft NLS siano stati installati nelle directory predefinite. In caso contrario, modificare i percorsi in modo appropriato.

     

    1.  Nella finestra Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto GuiStep 3 e scegliere Imposta come avvio \_ Project.
    2.  Fare di nuovo clic con il pulsante destro del mouse e scegliere Proprietà.
    3.  Nella finestra di dialogo Pagine delle proprietà del progetto:

        1.  Nell'elenco a discesa in alto a sinistra impostare Configurazione su Tutte le configurazioni.
        2.  In Proprietà di configurazione espandere C/C++, selezionare Generazione di codice e impostare Libreria di runtime: Debug multi-thread (/MTd).
        3.  Selezionare Generale e aggiungere ad Altre directory di inclusione:

            -   "C: \\ Microsoft NLS Downlevel APIs \\ Include".

        4.  Selezionare Lingua e impostare Considera wchar \_ t come tipo predefinito: No (/Zc:wchar \_ t-).
        5.  Selezionare Avanzate e impostare Convenzione di chiamata: \_ stdcall (/Gz).
        6.  In Proprietà di configurazione espandere Linker, selezionare Input e aggiungere ad Dipendenze aggiuntive:

            -   "C: \\ Programmi \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Lib \\ MUILoad.lib".
            -   "C: \\ Microsoft NLS Downlevel APIs \\ Lib \\ x86 \\ Nlsdl.lib".

3.  Sostituire il contenuto di GuiStep \_ 3.cpp con il codice seguente:
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  Creare o copiare langs.txt nella directory appropriata, come descritto in precedenza in [Passaggio 4: Globalizzazione di "Hello MUI".](#step-4-globalizing-hello-mui)
5.  Compilare ed eseguire il progetto.

> [!Note]  
> Se l'applicazione deve essere eseguita in versioni di Windows precedenti a Windows Vista, assicurarsi di leggere i documenti disponibili con il pacchetto di API di livello inferiore [Microsoft NLS](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) per informazioni su come ridistribuire Nlsdl.dll.

 

## <a name="additional-considerations-for-mui"></a>Considerazioni aggiuntive per MUI

### <a name="support-for-console-applications"></a>Supporto per le applicazioni console

Le tecniche illustrate in questa esercitazione possono essere usate anche nelle applicazioni console. Tuttavia, a differenza della maggior parte dei controlli GUI standard, la Windows di comando non può visualizzare caratteri per tutte le lingue. Per questo motivo, le applicazioni console multilingue richiedono particolare attenzione.

Se si chiamano le API [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) o [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) con flag di filtro specifici, le funzioni di caricamento delle risorse rimuovono i probe delle risorse della lingua per lingue specifiche che normalmente non vengono visualizzate all'interno di una finestra di comando. Quando questi flag sono impostati, gli algoritmi di impostazione della lingua consentono solo alle lingue che verranno visualizzate correttamente nella finestra di comando di essere nell'elenco di fallback.

Per altre informazioni sull'uso di queste API per compilare un'applicazione console multilingue, vedere le sezioni note di [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) e [**SetThreadPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)

### <a name="determination-of-languages-to-support-at-run-time"></a>Determinazione delle lingue da supportare in Run-Time

È possibile adottare uno dei suggerimenti di progettazione seguenti per determinare i linguaggi che l'applicazione deve supportare in fase di esecuzione:

-   **Durante l'installazione, consentire all'utente finale di selezionare la lingua preferita da un elenco di lingue supportate**

-   **Leggere un elenco di lingue da un file di configurazione**

    Alcuni progetti di questa esercitazione contengono una funzione usata per analizzare un file di langs.txt, che contiene un elenco di lingue.

    Poiché questa funzione accetta input esterno, convalidare le lingue fornite come input. Per altri dettagli sull'esecuzione della convalida, vedere le funzioni [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) o [**DownLevelLocaleNameToLCID.**](downlevellocalenametolcid.md)

-   **Eseguire query sul sistema operativo per determinare le lingue installate**

    Questo approccio consente all'applicazione di usare la stessa lingua del sistema operativo. Anche se questa operazione non richiede la richiesta dell'utente, se si sceglie questa opzione, tenere presente che le lingue del sistema operativo possono essere aggiunte o rimosse in qualsiasi momento e possono cambiare dopo l'installazione dell'applicazione da parte dell'utente. Tenere inoltre presente che in alcuni casi il sistema operativo viene installato con un supporto limitato per la lingua e l'applicazione offre più valore se supporta lingue non supportate dal sistema operativo.

    Per altre informazioni su come determinare le lingue attualmente installate nel sistema operativo, vedere la [**funzione EnumUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa)

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a>Supporto di script complessi nelle versioni precedenti Windows Vista

Quando un'applicazione che supporta determinati script complessi viene eseguita in una versione di Windows precedente a Windows Vista, il testo in tale script potrebbe non essere visualizzato correttamente nei componenti GUI. Nel progetto di livello inferiore in questa esercitazione, ad esempio, gli script hi-IN e ta-IN potrebbero non essere visualizzati nella finestra di messaggio a causa di problemi con l'elaborazione di script complessi e la mancanza di tipi di carattere correlati. In genere, problemi di questo tipo si presentano come caselle quadrate nel componente GUI.

Per altre informazioni su come abilitare l'elaborazione di script complessi, vedere Supporto di script e tipi di [carattere in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).

## <a name="summary"></a>Riepilogo

Questa esercitazione ha globalizzato un'applicazione monolingue e ha illustrato le procedure consigliate seguenti.

-   Progettare l'applicazione per sfruttare i vantaggi del modello di risorsa Win32.
-   Utilizzare la suddivisione MUI delle risorse in file binari satellite (file con estensione mui).
-   Assicurarsi che il processo di localizzazione abiliti le risorse nei file con estensione mui in modo che siano appropriate per la lingua di destinazione.
-   Assicurarsi che la creazione di pacchetti e la distribuzione dell'applicazione, dei file mui associati e del contenuto di configurazione vengano eseguite correttamente per consentire alle API di caricamento delle risorse di trovare il contenuto localizzato.
-   Fornire all'utente finale un meccanismo per modificare la configurazione della lingua dell'applicazione.
-   Modificare le impostazioni di time code per sfruttare i vantaggi della configurazione del linguaggio, per rendere l'applicazione più reattiva alle esigenze degli utenti finali.

 

 
