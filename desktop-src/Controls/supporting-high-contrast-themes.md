---
title: Supporto di Contrasto elevato temi
description: Questo argomento mette a confronto il supporto per i temi a contrasto elevato in Windows 8 a quello delle versioni precedenti di Windows e spiega come supportare i temi a contrasto elevato in un'applicazione Windows 8.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d64b585f302f578296c9e156895c23b9bce9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872990"
---
# <a name="supporting-high-contrast-themes"></a>Supporto di Contrasto elevato temi

Questo argomento mette a confronto il supporto per i temi a contrasto elevato in Windows 8 a quello delle versioni precedenti di Windows e spiega come supportare i temi a contrasto elevato in un'applicazione Windows 8.

Include le sezioni seguenti.

-   [Panoramica del supporto per temi Contrasto elevato](#overview-of-support-for-high-contrast-themes)
-   [Supporto di Contrasto elevato temi in Windows 8 e versioni successive](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [Aggiunta di una sezione di compatibilità al manifesto dell'applicazione](#adding-a-compatibility-section-to-your-application-manifest)
-   [Rilevamento Contrasto elevato nelle versioni precedenti di Windows](#detecting-high-contrast-in-previous-versions-of-windows)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a>Panoramica del supporto per temi Contrasto elevato

Windows 7 e versioni precedenti supportano due modelli di tema, tra cui il modello legacy di Windows classico e gli stili di visualizzazione correnti. Il modello di Windows classico è stato mantenuto attraverso Windows 7 principalmente per supportare i diversi temi a contrasto elevato. Tuttavia, il modello classico di Windows presenta diversi svantaggi:

-   Nessun supporto per i temi che utilizzano gli stili di visualizzazione, ad esempio Windows Aero. Gli utenti con temi a contrasto elevato devono usare l'interfaccia utente classica di Windows.
-   Nessun supporto per le funzionalità dell'interfaccia utente che si basano su Gestione finestre desktop (DWM) per l'esecuzione, ad esempio anteprime anteprime e la lente di ingrandimento schermo intero introdotta in Windows 7.
-   Gli sviluppatori devono mantenere due percorsi di codice distinti per supportare i due diversi modelli di tema.

In Windows 8 e versioni successive, le seguenti modifiche apportate al modello di tema hanno come indirizzo gli svantaggi precedenti:

-   Il modello di tema classico di Windows non è più supportato, consentendo agli sviluppatori di mantenere solo un percorso di codice per le applicazioni destinate solo a Windows 8.
-   Poiché gli stili visivi e DWM sono attivati in Windows 8, gli utenti a contrasto elevato possono accedere a funzionalità quali anteprime e l'ingrandimento a schermo intero.
-   Gli stili visivi supportano l'impostazione dei colori di diversi elementi dell'interfaccia utente, consentendo agli utenti a contrasto elevato di personalizzare l'interfaccia utente per soddisfare le esigenze e le preferenze specifiche.
-   Windows 8 include il supporto per la compatibilità per le applicazioni esistenti progettate per usare temi a contrasto elevato basati sul modello di tema classico di Windows.

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a>Supporto di Contrasto elevato temi in Windows 8 e versioni successive

In Windows 8, poiché gli stili visivi sono attivati in modalità a contrasto elevato, il supporto di temi a contrasto elevato è molto semplice purché si prestino le linee guida seguenti.

-   Dimensioni del tipo di carattere e del controllo. Per assicurarsi che l'interfaccia utente sia accessibile agli utenti con particolari esigenze, impostare le dimensioni dei caratteri in base alle impostazioni correnti del tema. Impostare la dimensione dei controlli su una dimensione di almeno quella predefinita.
-   Colori. Evitare l'uso di colori hardcoded. Usare invece i colori di sistema perché sono basati sul tema corrente. L'uso di colori personalizzati può interferire con ed eseguire l'override dei colori nei temi a contrasto elevato.
-   Manifesto dell'applicazione. Le applicazioni progettate per funzionare con i nuovi temi a contrasto elevato devono avere una sezione di compatibilità delle applicazioni definita nel manifesto che contiene i GUID di compatibilità di Windows 8. In caso contrario, Windows presuppone che l'applicazione sia progettata per una versione precedente di Windows ed esegua il rendering dell'interfaccia utente dell'applicazione simulando il modello di tema classico di Windows.

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a>Aggiunta di una sezione di compatibilità al manifesto dell'applicazione

Un manifesto dell'applicazione è un file XML che descrive i requisiti di un'applicazione. La sezione compatibilità del manifesto identifica le versioni di Windows supportate dall'applicazione. I GUID seguenti vengono utilizzati nella sezione compatibilità per identificare le diverse versioni di Windows.

| Versione       | GUID                                   |
|---------------|----------------------------------------|
| Windows Vista | {e2011457-1546-43c5-a5fe-008deee3d3f0} |
| Windows 7     | {35138b9a-5d96-4fbd-8e2d-a2440225f93a} |
| Windows 8     | {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} |



 

La sezione compatibilità può specificare più versioni di Windows, ma ognuna deve essere contenuta all'interno del proprio `<supportedOS/>` tag. Nell'esempio seguente viene illustrato un manifesto dell'applicazione che specifica Windows 7 e Windows 8 nella sezione compatibilità:


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!--The ID below indicates application support for Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>

            <!--The ID below indicates application support for Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        </application>
    </compatibility>
</assembly>
```



Se un'applicazione non dispone di un manifesto di compatibilità, si presuppone che si tratti di un'applicazione Windows Vista e non utilizza controlli con temi nell'area client quando è attivo un tema a contrasto elevato. Viene inoltre influenzato il comportamento di alcune funzioni degli stili di visualizzazione. Ad esempio, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)e [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) restituiscono false, mentre [**OPENTHEMEDATA**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) e [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) restituiscono un handle null. Questo è il supporto per la compatibilità, in modo che le applicazioni compilate prima di Windows 8 possano ancora eseguire il rendering della propria interfaccia utente nello stesso aspetto della modalità a contrasto elevato delle versioni precedenti di Windows, in cui gli stili di visualizzazione non sono disponibili.

In Windows 8, l'applicazione continua a ricevere i vantaggi della composizione desktop. Ciò significa, ad esempio, che le applicazioni di usabilità come la lente di ingrandimento a schermo intero non dipendono dallo stato del manifesto di un'applicazione singola. L'applicazione di usabilità continua a funzionare in modalità a contrasto elevato con un'applicazione che non si identifica come compatibile con Windows 8 nel manifesto.

Le immagini seguenti mostrano una semplice finestra di dialogo con un contrasto elevato in Windows 7.

![finestra di dialogo contrasto HIG](images/win7-high-contrast.png)

Questa immagine mostra la stessa finestra di dialogo a contrasto elevato in Windows 8, ma con la compatibilità con Windows 7 specificata nel manifesto dell'applicazione:

![finestra di dialogo contrasto elevato W8](images/win7-compat.png)

Questa immagine mostra la stessa finestra di dialogo a contrasto elevato in Windows 8, con Windows 8 specificato nel manifesto dell'applicazione:

![finestra di dialogo contrasto elevato W8 con manifesto](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a>Rilevamento Contrasto elevato nelle versioni precedenti di Windows

Le applicazioni in esecuzione nelle versioni precedenti di Windows non hanno accesso ai nuovi temi a contrasto elevato. Se l'applicazione deve essere eseguita nelle versioni precedenti di, è necessario includere il supporto per il rendering dell'interfaccia utente in contraWindowsst elevato nel modello di tema classico di Windows. L'applicazione può determinare se un tema a contrasto elevato è attivo chiamando la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con il **flag \_ GETHIGHCONTRAST SPI** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione degli stili di visualizzazione](cookbook-overview.md)
</dt> <dt>

[Stili di visualizzazione](themes-overview.md)
</dt> </dl>

 

 