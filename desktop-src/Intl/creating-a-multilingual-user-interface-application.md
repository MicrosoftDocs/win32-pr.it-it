---
description: Questa esercitazione illustra come eseguire un'applicazione monolingua e prepararla per l'internazionalizzazione. Questa applicazione è costituita da una soluzione completa compilata in Microsoft Visual Studio.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Aggiunta del supporto dell'interfaccia utente multilingue a un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192d9053513a7fe915990c80deb32ffdb9114910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884589"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a>Aggiunta del supporto dell'interfaccia utente multilingue a un'applicazione

Questa esercitazione illustra come eseguire un'applicazione monolingua e prepararla per l'internazionalizzazione. Questa applicazione è costituita da una soluzione completa compilata in Microsoft Visual Studio.

-   [Overview](#splitting-the-various-language-resource-modules-an-overview)
    -   [L'idea alla base di Hello MUI](#the-idea-behind-hello-mui)
-   [Configurazione della soluzione Hello MUI](#setting-up-the-hello-mui-solution)
    -   [Requisiti della piattaforma](#platform-requirements)
    -   [Prerequisiti](#prerequisites)
-   [Passaggio 0: creazione di Hello MUI hardcoded](#step-0-creating-the-hard-coded-hello-mui)
-   [Passaggio 1: implementazione del modulo Resource di base](#step-1-implementing-the-basic-resource-module)
-   [Passaggio 2: compilazione del modulo Resource di base](#step-2-building-the-basic-resource-module)
    -   [Suddivisione dei diversi moduli di risorse della lingua: Panoramica](#splitting-the-various-language-resource-modules-an-overview)
    -   [Suddivisione dei diversi moduli di risorse della lingua: creazione dei file](#splitting-the-various-language-resource-modules-creating-the-files)
-   [Passaggio 3: creazione di un Resource-Savvy "Hello MUI"](#step-3-creating-a-resource-savvy-hello-mui)
-   [Passaggio 4: globalizzazione di "Hello MUI"](#step-4-globalizing-hello-mui)
-   [Passaggio 5: personalizzazione di "Hello MUI"](#step-5-customizing-hello-mui)
-   [Considerazioni aggiuntive per MUI](#additional-considerations-for-mui)
    -   [Supporto per le applicazioni console](#support-for-console-applications)
    -   [Determinazione delle lingue da supportare in fase di esecuzione](#determination-of-languages-to-support-at-run-time)
    -   [Supporto per script complessi nelle versioni precedenti a Windows Vista](#complex-script-support-in-versions-prior-to-windows-vista)
-   [Summary](#summary)

## <a name="overview"></a>Panoramica

A partire da Windows Vista, il sistema operativo Windows è stato creato da zero per essere una piattaforma multilingue, con supporto aggiuntivo che consente di creare applicazioni multilingue che usano il modello di risorse MUI di Windows.

In questa esercitazione viene illustrato questo nuovo supporto per le applicazioni multilingue, coprendo gli aspetti seguenti:

-   Usa il migliorato supporto della piattaforma MUI per abilitare facilmente le applicazioni multilingue.
-   Estende le applicazioni multilingue da eseguire nelle versioni di Windows precedenti a Windows Vista.
-   Vengono riportate le considerazioni aggiuntive relative allo sviluppo di applicazioni multilingue specializzate, ad esempio applicazioni console.

Questi collegamenti forniscono un breve aggiornamento sui concetti di internazionalizzazione e MUI:

-   [Panoramica rapida dell'internazionalizzazione](understanding-internationalization.md).
-   [Concetti di MUI](understanding-mui.md).
-   [Uso di MUI per lo sviluppo di applicazioni Win32](using-multilingual-user-interface.md).

### <a name="the-idea-behind-hello-mui"></a>L'idea alla base di Hello MUI

Probabilmente si ha familiarità con l'applicazione Hello World classica, che illustra i concetti di programmazione di base. Questa esercitazione usa un approccio simile per illustrare come usare il modello di risorse MUI per aggiornare un'applicazione monolingua per creare una versione multilingue denominata Hello MUI.

> [!Note]  
> Le attività di questa esercitazione sono descritte in passaggi dettagliati a causa della precisione con cui devono essere eseguite queste attività e della necessità di spiegare i dettagli agli sviluppatori che hanno poca esperienza con queste attività.

 

## <a name="setting-up-the-hello-mui-solution"></a>Configurazione della soluzione Hello MUI

Questi passaggi illustrano come preparare la creazione della soluzione Hello MUI.

### <a name="platform-requirements"></a>Requisiti della piattaforma

È necessario compilare gli esempi di codice in questa esercitazione utilizzando Windows Software Development Kit (SDK) per Windows 7 e Visual Studio 2008. Windows 7 SDK verrà installato in Windows XP, Windows Vista e Windows 7 e la soluzione di esempio può essere compilata in una qualsiasi di queste versioni del sistema operativo.

Tutti gli esempi di codice in questa esercitazione sono progettati per essere eseguiti in versioni x86 e x64 di Windows XP, Windows Vista e Windows 7. Le parti specifiche che non funzioneranno in Windows XP sono denominate laddove appropriato.

### <a name="prerequisites"></a>Prerequisiti

1.  Installare Visual Studio 2008.

    Per ulteriori informazioni, vedere il [centro per sviluppatori di Visual Studio](https://msdn.microsoft.com/vstudio/default.aspx).

2.  Installare la Windows SDK per Windows 7.

    È possibile installarlo dalla pagina Windows SDK del centro per [sviluppatori Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx). L'SDK include utilità per lo sviluppo di applicazioni per le versioni del sistema operativo a partire da Windows XP attraverso le versioni più recenti.

    > [!Note]  
    > Se il pacchetto non viene installato nel percorso predefinito o se non si sta eseguendo l'installazione nell'unità di sistema, che in genere è l'unità C, prendere nota del percorso di installazione.

     

3.  Configurare i parametri della riga di comando di Visual Studio.

    1.  Aprire una finestra di comando di Visual Studio.
    2.  Digitare **percorso set**.
    3.  Verificare che la variabile Path includa il percorso della cartella bin di Windows 7 SDK:... Microsoft SDK \\ Windows \\ v 7.0 \\ bin

4.  Installare il pacchetto aggiuntivo per le API NLS di livello inferiore Microsoft.
    > [!Note]  
    > Nel contesto di questa esercitazione, questo pacchetto è necessario solo se si intende personalizzare l'applicazione per l'esecuzione in versioni di Windows precedenti a Windows Vista. Vedere [passaggio 5: personalizzazione di Hello MUI](#step-5-customizing-hello-mui).

     

    1.  Scaricare e installare il pacchetto dal relativo [sito di download](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).
    2.  Come per il Windows SDK, se il pacchetto non viene installato nel percorso predefinito o se non si esegue l'installazione nell'unità di sistema, che è in genere l'unità C, prendere nota del percorso di installazione.
    3.  Se la piattaforma di sviluppo è Windows XP o Windows Server 2003, verificare che Nlsdl.dll sia installato e registrato correttamente.

        1.  Passare alla cartella "Redist" sotto il percorso di installazione.
        2.  Eseguire il nlsdl ridistribuibile \* appropriato. exe, ad esempio nlsdl.x86.exe. Questo passaggio consente di installare e registrare Nlsdl.dll.

    > [!Note]  
    > Se si sviluppa un'applicazione che utilizza MUI e che deve essere eseguita nelle versioni di Windows precedenti a Windows Vista, è necessario che Nlsdl.dll sia presente nella piattaforma Windows di destinazione. Nella maggior parte dei casi, ciò significa che l'applicazione deve portare e installare il programma di installazione di nlsdl ridistribuibile (e non solo copiare Nlsdl.dll).

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a>Passaggio 0: creazione di Hello MUI hardcoded

Questa esercitazione inizia con la versione monolingue dell'applicazione Hello MUI. L'applicazione presuppone l'uso del linguaggio di programmazione C++, delle stringhe di caratteri wide e della funzione [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) per l'output.

Per iniziare, creare l' \_ applicazione GuiStep 0 iniziale, nonché la soluzione HelloMUI, che contiene tutte le applicazioni in questa esercitazione.

1.  In Visual Studio 2008 creare un nuovo progetto. Usare le impostazioni e i valori seguenti:

    1.  Tipo di progetto: in Visual C++ selezionare Win32, quindi in modelli Visual Studio installati selezionare progetto Win32.
    2.  Nome: GuiStep \_ 0.
    3.  Percorso: *ProjectRootDirectory* (i passaggi successivi fanno riferimento a questa directory).
    4.  Nome soluzione: HelloMUI.
    5.  Selezionare Crea directory per soluzione.
    6.  Nella creazione guidata applicazione Win32 selezionare il tipo di applicazione predefinito: applicazione Windows.

2.  Configurare il modello di threading del progetto:

    1.  Nella Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto GuiStep \_ 0, quindi scegliere Proprietà.
    2.  Nella finestra di dialogo Pagine delle proprietà del progetto:

        1.  Nell'elenco a discesa in alto a sinistra impostare configurazione su tutte le configurazioni.
        2.  In proprietà di configurazione espandere C/C++, selezionare generazione codice e impostare libreria di runtime: debug multithread (/MTd).

3.  Sostituire il contenuto di GuiStep \_ 0. cpp con il codice seguente:
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

Il codice sorgente semplice precedente rende la scelta di progettazione semplicistica, o incorporare, tutto l'output visualizzato dall'utente, in questo caso il testo "Hello MUI". Questa scelta limita l'utilità dell'applicazione per gli utenti che non riconoscono la parola inglese "Hello". Poiché MUI è un acronimo di inglese basato su tecnologia, per questa esercitazione si presuppone che la stringa rimanga "MUI" per tutte le lingue.

## <a name="step-1-implementing-the-basic-resource-module"></a>Passaggio 1: implementazione del modulo Resource di base

Microsoft Win32 ha esposto a lungo la possibilità per gli sviluppatori di applicazioni di separare i dati delle risorse dell'interfaccia utente dal codice sorgente dell'applicazione. Questa separazione è costituita dal modello di risorsa Win32, in cui le stringhe, le bitmap, le icone, i messaggi e gli altri elementi normalmente visualizzati a un utente vengono inseriti in una sezione distinta del file eseguibile, separati dal codice eseguibile.

Per illustrare questa separazione tra il codice eseguibile e la creazione di pacchetti di dati delle risorse, in questo passaggio l'esercitazione posiziona la stringa "Hello" hardcoded in precedenza (la risorsa "en-US") nella sezione delle risorse di un modulo DLL nel \_ progetto HelloModule en \_ US.

Questa DLL Win32 può inoltre contenere la funzionalità eseguibile del tipo di libreria (come qualsiasi altra DLL). Tuttavia, per concentrarsi sugli aspetti correlati alle risorse Win32, il codice della DLL di run-time viene eliminato in DllMain. cpp. Nelle sezioni successive di questa esercitazione vengono usati i dati della risorsa HelloModule compilati in questo articolo e viene anche presentato il codice di runtime appropriato.

Per costruire un modulo di risorse Win32, iniziare creando una DLL con un valore DllMain eliminato:

1.  Aggiungere un nuovo progetto alla soluzione HelloMUI:

    1.  Scegliere Aggiungi dal menu file, quindi nuovo progetto.
    2.  Tipo di progetto: progetto Win32.
    3.  Nome: HelloModule \_ en \_ US.
    4.  Percorso: *ProjectRootDirectory* \\ HelloMUI.
    5.  Nella creazione guidata applicazione Win32 selezionare tipo di applicazione: DLL.

2.  Configurare il modello di threading del progetto:

    1.  Nel Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto HelloModule \_ en \_ US e scegliere Proprietà.
    2.  Nella finestra di dialogo Pagine delle proprietà del progetto:

        1.  Nell'elenco a discesa in alto a sinistra impostare configurazione su tutte le configurazioni.
        2.  In proprietà di configurazione espandere C/C++, selezionare generazione codice e impostare libreria di runtime: debug multithread (/MTd).

3.  Esaminare DllMain. cpp. (Potrebbe essere necessario aggiungere l'oggetto senza riferimenti \_ Macro di parametri per il codice generato, come in questo caso, per consentirne la compilazione a livello di avviso 4.
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

    

4.  Aggiungere un file di definizione delle risorse HelloModule. RC al progetto:

    1.  Nel progetto HelloModule \_ en \_ US, fare clic con il pulsante destro del mouse sulla cartella file di risorse e scegliere Aggiungi, quindi selezionare nuovo elemento.
    2.  Nella finestra di dialogo Aggiungi nuovo elemento scegliere gli elementi seguenti:

        1.  Categorie: in Visual C++ selezionare la risorsa e quindi in "modelli Visual Studio installati" selezionare file di risorse (. RC).
        2.  Nome: HelloModule.
        3.  Percorso: accettare il valore predefinito.
        4.  Fare clic su Aggiungi.

    3.  Specifica che il nuovo file HelloModule. RC deve essere salvato come Unicode:

        1.  Nella Esplora soluzioni fare clic con il pulsante destro del mouse su HelloModule. RC e selezionare Visualizza codice.
        2.  Se viene visualizzato un messaggio che indica che il file è già aperto e chiede se si desidera chiuderlo, fare clic su Sì.
        3.  Con il file visualizzato come testo, scegliere il file di selezione dei menu e quindi Opzioni di salvataggio avanzate.
        4.  In codifica specificare Unicode-codepage 1200.
        5.  Fare clic su OK.
        6.  Salvare e chiudere HelloModule. RC.

    4.  Aggiungere una tabella di stringhe contenente la stringa "Hello":

        1.  Nella Visualizzazione risorse fare clic con il pulsante destro del mouse su HelloModule. RC e scegliere Aggiungi risorsa.
        2.  Selezionare tabella di stringhe.
        3.  Fare clic su New.
        4.  Aggiungere una stringa alla tabella delle stringhe:

            1.  ID: Salve \_ MUI \_ Str \_ 0.
            2.  Valore: 0
            3.  Didascalia: Hello.

        Se si visualizza HelloModule. RC come testo ora, verranno visualizzate varie parti del codice sorgente specifico per le risorse. Il primo interesse è la sezione che descrive la stringa "Hello":

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

        

        Questa stringa "Hello" è la risorsa che deve essere localizzata, ovvero convertita, in ogni lingua che l'applicazione spera di supportare. Ad esempio, il HelloModule \_ TA \_ in Project (che verrà creato nel passaggio successivo) conterrà la propria versione localizzata di HelloModule. RC per "ta-in":

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

        

    5.  Compilare il \_ progetto HelloModule en \_ US per assicurarsi che non siano presenti errori.

5.  Creare sei altri progetti nella soluzione HelloMUI (o il numero desiderato) per creare sei altre DLL di risorse per altre lingue. Usare i valori in questa tabella:

    | Project name (Nome progetto)        | Nome del file RC | ID stringa          | Valore stringa | Didascalia stringa |
    |---------------------|------------------|--------------------|--------------|----------------|
    | HelloModule \_ de \_ de | HelloModule      | HELLo \_ MUI \_ Str \_ 0 | 0            | Hallo          |
    | HelloModule \_ es \_ es | HelloModule      | HELLo \_ MUI \_ Str \_ 0 | 0            | Hola           |
    | HelloModule \_ fr \_ fr | HelloModule      | HELLo \_ MUI \_ Str \_ 0 | 0            | Bonjour        |
    | HelloModule \_ Hi \_ in | HelloModule      | HELLo \_ MUI \_ Str \_ 0 | 0            | नमस्           |
    | HelloModule \_ ur \_ ur | HelloModule      | HELLo \_ MUI \_ Str \_ 0 | 0            | Здравствуйте   |
    | HelloModule \_ TA \_ in | HelloModule      | HELLo \_ MUI \_ Str \_ 0 | 0            | வணக்கம்        |

    

     

Per ulteriori informazioni sulla sintassi e la struttura dei file RC, vedere [informazioni sui file di risorse](../menurc/about-resource-files.md).

## <a name="step-2-building-the-basic-resource-module"></a>Passaggio 2: compilazione del modulo Resource di base

Usando i modelli di risorse precedenti, la compilazione di uno dei sette progetti HelloModule comporterebbe sette DLL separate. Ogni DLL conterrà una sezione delle risorse con una singola stringa localizzata nella lingua appropriata. Sebbene sia appropriato per il modello di risorse Win32 storico, questo progetto non sfrutta i vantaggi di MUI.

In Windows Vista SDK e versioni successive, MUI consente di suddividere i file eseguibili in codice sorgente e moduli di contenuto localizzabili. Con la personalizzazione aggiuntiva più avanti nel passaggio 5, le applicazioni possono essere abilitate per l'esecuzione del supporto multilingue nelle versioni precedenti a Windows Vista.

I meccanismi principali disponibili per suddividere le risorse dal codice eseguibile, a partire da Windows Vista, sono i seguenti:

-   Utilizzando rc.exe (il compilatore RC) con commutatori specifici o
-   Utilizzando uno strumento di suddivisione dello stile di post-compilazione denominato muirct.exe.

Per ulteriori informazioni, vedere [Utilità risorse](resource-utilities.md) .

Per semplicità, in questa esercitazione viene usato muirct.exe per suddividere il file eseguibile "Hello MUI".

### <a name="splitting-the-various-language-resource-modules-an-overview"></a>Suddivisione dei diversi moduli di risorse della lingua: Panoramica

Per suddividere le dll in un HelloModule.dll eseguibile, oltre a una HelloModule.dll. MUI per ognuna delle sette lingue supportate in questa esercitazione, è necessario un processo multiparte. In questa panoramica vengono descritti i passaggi necessari. la sezione successiva presenta un file di comando che esegue questi passaggi.

Per prima cosa, suddividere il modulo HelloModule.dll solo in lingua inglese usando il comando:


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



La riga di comando precedente usa il file di configurazione DoReverseMuiLoc. rcconfig. Questo tipo di file di configurazione viene in genere usato da muirct.exe per suddividere le risorse tra la DLL indipendente dalla lingua e i file con estensione MUI dipendenti dal linguaggio. In questo caso, il file XML DoReverseMuiLoc. rcconfig (elencato nella sezione successiva) indica molti tipi di risorse, ma tutti rientrano nella categoria di file "localizedResources" o MUI e non sono presenti risorse nella categoria indipendente dal linguaggio. Per altre informazioni su come preparare un file di configurazione delle risorse, vedere [preparazione di un file di configurazione delle risorse](preparing-a-resource-configuration-file.md).

Oltre a creare un file HelloModule.dll. MUI che contiene la stringa inglese "Hello", muirct.exe incorpora anche una risorsa MUI nel modulo HelloModule.dll durante la suddivisione. Per eseguire correttamente il caricamento in fase di esecuzione delle risorse appropriate dai moduli HelloModule.dll. mui specifici del linguaggio, è necessario che i checksum dei file con estensione mui siano corretti in modo che corrispondano ai valori di checksum nel modulo di base lingua-indipendente dalla lingua. Questa operazione viene eseguita tramite un comando, ad esempio:


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



Analogamente, viene richiamato muirct.exe per creare un file HelloModule.dll. MUI per ognuno degli altri linguaggi. In questi casi, tuttavia, la DLL indipendente dalla lingua viene eliminata, perché sarà necessaria solo la prima creazione. I comandi che elaborano le risorse spagnole e francesi hanno un aspetto simile al seguente:


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



Uno degli aspetti più importanti da notare nella muirct.exe righe di comando precedente è che il flag-x viene usato per specificare un ID lingua di destinazione. Il valore fornito per muirct.exe è diverso per ogni modulo di HelloModule.dll specifico della lingua. Il valore di questo linguaggio è Central e viene usato da muirct.exe per contrassegnare in modo appropriato il file con estensione MUI durante la suddivisione. Un valore non corretto produce errori di caricamento delle risorse per quel particolare file con estensione MUI in fase di esecuzione. Per ulteriori informazioni sul mapping tra nome del linguaggio e LCID, vedere [costanti e stringhe degli identificatori di lingua](language-identifier-constants-and-strings.md) .

Ogni file Split. MUI viene inserito in una directory corrispondente al nome della lingua, immediatamente sotto la directory in cui risiederà la HelloModule.dll indipendente dalla lingua. Per ulteriori informazioni sul posizionamento dei file con estensione MUI, vedere [distribuzione di applicazioni](application-deployment.md).

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a>Suddivisione dei diversi moduli di risorse della lingua: creazione dei file

Per questa esercitazione è possibile creare un file di comando contenente i comandi per suddividere le varie dll e richiamarlo manualmente. Si noti che durante il lavoro di sviluppo effettivo, è possibile ridurre il rischio di errori di compilazione includendo questi comandi come eventi di pre-compilazione o post-compilazione nella soluzione HelloMUI, ma questo esula dall'ambito di questa esercitazione.

Creare i file per la build di debug:

1.  Creare un file di comando DoReverseMuiLoc. cmd contenente i comandi seguenti:
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

    

2.  Creare un file XML DoReverseMuiLoc. rcconfig contenente le righe seguenti:
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

    

3.  Copiare DoReverseMuiLoc. cmd e DoReverseMuiLoc. rcconfig in *ProjectRootDirectory* \\ HelloMUI \\ debug.
4.  Aprire il prompt dei comandi di Visual Studio 2008 e passare alla directory di debug.
5.  Eseguire DoReverseMuiLoc. cmd.

Quando si crea una build di rilascio, si copiano gli stessi file DoReverseMuiLoc. cmd e DoReverseMuiLoc. rcconfig nella directory della versione ed eseguire il file di comando.

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a>Passaggio 3: creazione di un Resource-Savvy "Hello MUI"

Basandosi sull'GuiStep iniziale hardcoded \_0.exe esempio precedente, è possibile estendere la portata dell'applicazione a più utenti del linguaggio scegliendo di incorporare il modello di risorse Win32. Il nuovo codice di runtime presentato in questo passaggio include la logica di caricamento dei moduli ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) e il recupero di stringhe ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)).

1.  Aggiungere un nuovo progetto alla soluzione HelloMUI (usando il menu file di selezione, Aggiungi e nuovo progetto) con i valori e le impostazioni seguenti:

    1.  Tipo di progetto: progetto Win32.
    2.  Nome: GuiStep \_ 1.
    3.  Percorso: accettare il valore predefinito.
    4.  Nella creazione guidata applicazione Win32 selezionare il tipo di applicazione predefinito: applicazione Windows.

2.  Impostare questo progetto per l'esecuzione dall'interno di Visual Studio e configurarne il modello di threading:

    1.  Nella Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto GuiStep \_ 1 e selezionare Imposta come progetto di avvio.
    2.  Fare di nuovo clic con il pulsante destro del mouse e scegliere Proprietà.
    3.  Nella finestra di dialogo Pagine delle proprietà del progetto:

        1.  Nell'elenco a discesa in alto a sinistra impostare configurazione su tutte le configurazioni.
        2.  In proprietà di configurazione espandere C/C++, selezionare generazione codice e impostare libreria di runtime: debug multithread (/MTd).

3.  Sostituire il contenuto di GuiStep \_ 1. cpp con il codice seguente:
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

## <a name="step-4-globalizing-hello-mui"></a>Passaggio 4: globalizzazione di "Hello MUI"

Sebbene l'esempio precedente sia in grado di visualizzare l'output in lingue diverse, il numero di aree è ridotto. Probabilmente il più evidente è che l'applicazione è disponibile solo in un piccolo subset di linguaggi rispetto al sistema operativo Windows stesso. Se, ad esempio, l' \_ applicazione GuiStep 1 del passaggio precedente è stata installata in una build giapponese di Windows, è probabile che si verifichino errori nella posizione delle risorse.

Per risolvere questo problema, sono disponibili due opzioni principali:

-   Verificare che siano incluse le risorse in un linguaggio di fallback finale predeterminato.
-   Consente all'utente finale di configurare le preferenze di lingua da un sottoinsieme di linguaggi specificamente supportati dall'applicazione.

Di queste opzioni, l'unico che fornisce un linguaggio di fallback finale è altamente consigliato e viene implementato in questa esercitazione passando il flag-g a muirct.exe, come illustrato in precedenza. Questo flag indica muirct.exe di creare una lingua specifica (de-DE/0x0407) la lingua di fallback finale associata al modulo dll indipendente dalla lingua (HelloModule.dll). In fase di esecuzione questo parametro viene usato come ultima risorsa per generare il testo da visualizzare all'utente. Nel caso in cui non venga individuato un linguaggio di fallback finale e non siano disponibili risorse appropriate nel file binario indipendente dalla lingua, il caricamento della risorsa ha esito negativo. È pertanto necessario determinare con attenzione gli scenari che potrebbero verificarsi nell'applicazione e pianificare di conseguenza il linguaggio di fallback finale.

L'altra opzione di consentire le preferenze per la lingua configurabile e il caricamento delle risorse in base a questa gerarchia definita dall'utente può aumentare significativamente la soddisfazione dei clienti. Sfortunatamente, complica anche la funzionalità necessaria all'interno dell'applicazione.

Questo passaggio dell'esercitazione usa un meccanismo di file di testo semplificato per abilitare la configurazione della lingua utente personalizzata. Il file di testo viene analizzato in fase di esecuzione dall'applicazione e l'elenco di lingue analizzate e convalidate viene usato per stabilire un elenco di fallback personalizzato. Una volta stabilito l'elenco di fallback personalizzato, le API di Windows caricherà le risorse in base alla precedenza della lingua impostata in questo elenco. Il resto del codice è simile a quello riportato nel passaggio precedente.

1.  Aggiungere un nuovo progetto alla soluzione HelloMUI (usando il menu file di selezione, Aggiungi e nuovo progetto) con i valori e le impostazioni seguenti:

    1.  Tipo di progetto: progetto Win32.
    2.  Nome: GuiStep \_ 2.
    3.  Percorso: accettare il valore predefinito.
    4.  Nella creazione guidata applicazione Win32 selezionare il tipo di applicazione predefinito: applicazione Windows.

2.  Impostare questo progetto per l'esecuzione dall'interno di Visual Studio e configurarne il modello di threading:

    1.  Nella Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto GuiStep \_ 2 e selezionare Imposta come progetto di avvio.
    2.  Fare di nuovo clic con il pulsante destro del mouse e scegliere Proprietà.
    3.  Nella finestra di dialogo Pagine delle proprietà del progetto:

        1.  Nell'elenco a discesa in alto a sinistra impostare configurazione su tutte le configurazioni.
        2.  In proprietà di configurazione espandere C/C++, selezionare generazione codice e impostare libreria di runtime: debug multithread (/MTd).

3.  Sostituire il contenuto di GuiStep \_ 2. cpp con il codice seguente:
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

     

    Copiare langs.txt nella directory da cui viene eseguito il programma:

    -   Se eseguito da Visual Studio, copiarlo in *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2.
    -   Se eseguito da Esplora risorse, copiarlo nella stessa directory di GuiStep \_2.exe.

5.  Compilare ed eseguire il progetto. Provare a modificare langs.txt in modo che vengano visualizzate lingue diverse all'inizio dell'elenco.

## <a name="step-5-customizing-hello-mui"></a>Passaggio 5: personalizzazione di "Hello MUI"

Alcune delle funzionalità di run-time indicate finora in questa esercitazione sono disponibili solo in Windows Vista e versioni successive. Potrebbe essere necessario riutilizzare lo sforzo investito nella localizzazione e nella suddivisione delle risorse rendendo l'applicazione funzionante sulle versioni del sistema operativo Windows di livello inferiore, ad esempio Windows XP. Questo processo comporta la modifica dell'esempio precedente in due aree principali:

-   Le funzioni di caricamento delle risorse precedenti a Windows Vista, ad esempio [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)e altre, non sono compatibili con MUI. Le applicazioni fornite con le risorse divise (file in e MUI) devono caricare i moduli delle risorse usando una di queste due funzioni:

    -   Se l'applicazione deve essere eseguita solo in Windows Vista e versioni successive, dovrebbe caricare i moduli delle risorse con [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).
    -   Se l'applicazione deve essere eseguita nelle versioni precedenti a Windows Vista, oltre che in Windows Vista o versioni successive, è necessario utilizzare [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), che è una funzione di livello inferiore specificata in Windows 7 SDK.

-   Il supporto per la gestione delle lingue e gli ordini di fallback della lingua offerti nelle versioni precedenti a Windows Vista del sistema operativo Windows differisce significativamente da quello in Windows Vista e versioni successive. Per questo motivo, le applicazioni che consentono il fallback della lingua configurata dall'utente devono modificare le proprie procedure di gestione della lingua:

    -   Se l'applicazione deve essere eseguita solo in Windows Vista e versioni successive, è sufficiente impostare l'elenco di lingue utilizzando [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) .
    -   Se l'applicazione deve essere eseguita in tutte le versioni di Windows, è necessario costruire il codice che verrà eseguito su piattaforme di livello inferiore per scorrere l'elenco di lingue configurato dall'utente e verificare il modulo di risorse desiderato. Questo può essere visualizzato nelle sezioni 1C e 2 del codice fornito più avanti in questo passaggio.

Creare un progetto in grado di usare i moduli di risorse localizzati in qualsiasi versione di Windows:

1.  Aggiungere un nuovo progetto alla soluzione HelloMUI (usando il menu file di selezione, Aggiungi e nuovo progetto) con i valori e le impostazioni seguenti:

    1.  Tipo di progetto: progetto Win32.
    2.  Nome: GuiStep \_ 3.
    3.  Percorso: accettare il valore predefinito.
    4.  Nella creazione guidata applicazione Win32 selezionare il tipo di applicazione predefinito: applicazione Windows.

2.  Impostare questo progetto per l'esecuzione dall'interno di Visual Studio e configurarne il modello di Threading. Inoltre, configurarlo per aggiungere le intestazioni e le librerie necessarie.

    > [!Note]  
    > Nei percorsi usati in questa esercitazione si presuppone che il pacchetto Windows 7 SDK e le API NLS di livello inferiore siano stati installati nelle directory predefinite. In caso contrario, modificare i percorsi in modo appropriato.

     

    1.  Nella Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto GuiStep \_ 3 e selezionare Imposta come progetto di avvio.
    2.  Fare di nuovo clic con il pulsante destro del mouse e scegliere Proprietà.
    3.  Nella finestra di dialogo Pagine delle proprietà del progetto:

        1.  Nell'elenco a discesa in alto a sinistra impostare configurazione su tutte le configurazioni.
        2.  In proprietà di configurazione espandere C/C++, selezionare generazione codice e impostare libreria di runtime: debug multithread (/MTd).
        3.  Selezionare generale e aggiungere a directory di inclusione aggiuntive:

            -   "C: \\ API NLS di livello inferiore Microsoft \\ includono".

        4.  Selezionare la lingua e impostare considera WCHAR \_ t come tipo incorporato: No (/Zc: WCHAR \_ t-).
        5.  Selezionare Avanzate e impostare la convenzione di chiamata: \_ stdcall (/gz).
        6.  In proprietà di configurazione espandere linker, selezionare input e aggiungere a dipendenze aggiuntive:

            -   "C: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ lib \\ MUILoad. lib".
            -   "C: \\ API NLS di livello inferiore Microsoft \\ lib \\ x86 \\ nlsdl. lib".

3.  Sostituire il contenuto di GuiStep \_ 3. cpp con il codice seguente:
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

    

4.  Creare o copiare langs.txt nella directory appropriata, come descritto in precedenza in [Step 4: globalizzating "Hello MUI"](#step-4-globalizing-hello-mui).
5.  Compilare ed eseguire il progetto.

> [!Note]  
> Se l'applicazione deve essere eseguita nelle versioni di Windows precedenti a Windows Vista, assicurarsi di leggere i documenti forniti con il pacchetto di [API NLS](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) di livello inferiore di Microsoft per informazioni su come ridistribuire Nlsdl.dll.

 

## <a name="additional-considerations-for-mui"></a>Considerazioni aggiuntive per MUI

### <a name="support-for-console-applications"></a>Supporto per le applicazioni console

Le tecniche descritte in questa esercitazione possono anche essere usate nelle applicazioni console. Tuttavia, a differenza della maggior parte dei controlli GUI standard, la finestra di comando di Windows non può visualizzare caratteri per tutte le lingue. Per questo motivo, le applicazioni console multilingue richiedono particolare attenzione.

Chiamando le API [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) o [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) con flag di filtro specifici, le funzioni di caricamento delle risorse rimuovono i probe delle risorse della lingua per linguaggi specifici che in genere non sono visualizzati all'interno di una finestra di comando. Quando questi flag sono impostati, gli algoritmi di impostazione della lingua consentono solo le lingue che verranno visualizzate correttamente nella finestra di comando affinché si trovino nell'elenco di fallback.

Per altre informazioni sull'uso di queste API per compilare un'applicazione console multilingue, vedere le sezioni Note di [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) e [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).

### <a name="determination-of-languages-to-support-at-run-time"></a>Determinazione delle lingue da supportare in Run-Time

È possibile adottare uno dei seguenti suggerimenti di progettazione per determinare le lingue che l'applicazione deve supportare in fase di esecuzione:

-   **Durante l'installazione, consentire all'utente finale di selezionare la lingua preferita da un elenco di lingue supportate**

-   **Leggi un elenco di lingue da un file di configurazione**

    Alcuni dei progetti in questa esercitazione contengono una funzione utilizzata per analizzare un file di configurazione langs.txt, che contiene un elenco di lingue.

    Poiché questa funzione accetta input esterno, convalidare le lingue fornite come input. Per ulteriori informazioni sull'esecuzione di tale convalida, vedere le funzioni [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) o [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) .

-   **Eseguire una query sul sistema operativo per determinare quali lingue sono installate**

    Questo approccio consente all'applicazione di usare la stessa lingua del sistema operativo. Sebbene non richieda la richiesta dell'utente, se si sceglie questa opzione, tenere presente che le lingue del sistema operativo possono essere aggiunte o rimosse in qualsiasi momento e possono essere modificate dopo che l'utente ha installato l'applicazione. Tenere inoltre presente che in alcuni casi il sistema operativo viene installato con supporto di lingua limitato e l'applicazione offre un valore maggiore se supporta lingue non supportate dal sistema operativo.

    Per ulteriori informazioni su come determinare le lingue attualmente installate nel sistema operativo, vedere la funzione [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a>Supporto per script complessi nelle versioni precedenti a Windows Vista

Quando un'applicazione che supporta alcuni script complessi viene eseguita in una versione di Windows precedente a Windows Vista, il testo in tale script potrebbe non essere visualizzato correttamente nei componenti della GUI. Nel progetto di livello inferiore all'interno di questa esercitazione, ad esempio, gli script Hi-IN e TA-IN potrebbero non essere visualizzati nella finestra di messaggio a causa di problemi relativi all'elaborazione di script complessi e alla mancanza di tipi di carattere correlati. In genere, i problemi di questa natura si presentano come caselle quadrate nel componente GUI.

Per ulteriori informazioni su come abilitare l'elaborazione di script complessi, vedere [supporto di script e tipi di carattere in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).

## <a name="summary"></a>Riepilogo

Questa esercitazione ha globalizzato un'applicazione monolingua e ha illustrato le procedure consigliate seguenti.

-   Progettare l'applicazione per sfruttare il modello di risorse Win32.
-   Utilizzare la suddivisione MUI delle risorse in file binari satellite (file con estensione MUI).
-   Verificare che il processo di localizzazione aggiorni le risorse nei file con estensione MUI per adattarle alla lingua di destinazione.
-   Assicurarsi che la creazione di pacchetti e la distribuzione dell'applicazione, i file con estensione MUI associati e il contenuto della configurazione vengano eseguiti correttamente per consentire alle API di caricamento delle risorse di trovare il contenuto localizzato.
-   Fornire all'utente finale un meccanismo per modificare la configurazione della lingua dell'applicazione.
-   Modificare il codice di runtime per sfruttare i vantaggi della configurazione del linguaggio, in modo da rendere l'applicazione più rispondente alle esigenze degli utenti finali.

 

 
