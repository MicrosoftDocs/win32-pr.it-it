---
title: Supporto dei Contrasto elevato personalizzati
description: In questo argomento viene confrontato il supporto per i temi a contrasto elevato in Windows 8 con quello delle versioni precedenti di Windows e viene illustrato come supportare i temi a contrasto elevato in un'applicazione Windows 8.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f32c89302daeb7190174a0d6b9e822e1c55d3e530ad29baedd00c5ffdefc97b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670646"
---
# <a name="supporting-high-contrast-themes"></a>Supporto dei Contrasto elevato personalizzati

In questo argomento viene confrontato il supporto per i temi a contrasto elevato in Windows 8 con quello delle versioni precedenti di Windows e viene illustrato come supportare i temi a contrasto elevato in un'applicazione Windows 8.

Include le sezioni seguenti.

-   [Panoramica del supporto per i Contrasto elevato personalizzati](#overview-of-support-for-high-contrast-themes)
-   [Supporto dei Contrasto elevato in Windows 8 e versioni successive](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [Aggiunta di una sezione di compatibilità al manifesto dell'applicazione](#adding-a-compatibility-section-to-your-application-manifest)
-   [Rilevamento Contrasto elevato nelle versioni precedenti di Windows](#detecting-high-contrast-in-previous-versions-of-windows)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a>Panoramica del supporto per i Contrasto elevato personalizzati

Windows 7 e versioni precedenti supportano due modelli di tema, tra cui il modello Windows classico legacy e gli stili di visualizzazione correnti. Il Windows modello classico è stato mantenuto tramite Windows 7 principalmente per supportare i vari temi a contrasto elevato. Tuttavia, il Windows modello classico presenta una serie di svantaggi:

-   Nessun supporto per i temi che usano stili di visualizzazione, ad esempio Windows Tema. Gli utenti di temi a contrasto elevato devono usare l'interfaccia Windows interfaccia utente classica.
-   Nessun supporto per le funzionalità dell'interfaccia utente che si basano su Gestione finestre desktop (DWM) per l'esecuzione, ad esempio anteprime di anteprima e lente di ingrandimento a schermo intero introdotte in Windows 7.
-   Gli sviluppatori devono mantenere due percorsi di codice separati per supportare i due diversi modelli di gestione dei colori.

In Windows 8 e versioni successive, le modifiche seguenti al modello di descrizione dei dati rilevano gli svantaggi precedenti:

-   Il Windows modello di tema classico non è più supportato, consentendo agli sviluppatori di mantenere un solo percorso di codice per le applicazioni che hanno come destinazione solo Windows 8.
-   Poiché gli stili di visualizzazione e DWM sono attivi in Windows 8, gli utenti a contrasto elevato hanno accesso a funzionalità quali anteprime e lente di ingrandimento a schermo intero.
-   Gli stili di visualizzazione supportano l'impostazione dei colori di vari elementi dell'interfaccia utente, consentendo agli utenti a contrasto elevato di personalizzare l'interfaccia utente in base alle singole esigenze e preferenze.
-   Windows 8 include il supporto della compatibilità per le applicazioni esistenti progettate per l'uso di temi a contrasto elevato basati Windows modello di tema classico.

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a>Supporto dei Contrasto elevato in Windows 8 e versioni successive

In Windows 8, poiché gli stili di visualizzazione sono in modalità a contrasto elevato, il supporto dei temi a contrasto elevato è semplice, purché siano state dirette le linee guida seguenti.

-   Dimensioni dei tipi di carattere e dei controlli. Per assicurarsi che l'interfaccia utente sia accessibile agli utenti con disabilità, impostare le dimensioni dei caratteri in base alle impostazioni correnti del tema. Impostare le dimensioni dei controlli in modo che siano almeno le dimensioni predefinite.
-   Colori. Evitare di usare colori hard coded. Usare invece i colori di sistema perché sono basati sul tema corrente. L'uso di colori personalizzati può interferire con i colori nei temi a contrasto elevato ed eseguirne l'override.
-   Manifesto dell'applicazione. Le applicazioni progettate per funzionare con i nuovi temi a contrasto elevato devono avere una sezione di compatibilità dell'applicazione definita nel manifesto che contiene i GUID di compatibilità Windows 8 compatibilità. In caso contrario, Windows presuppone che l'applicazione sia progettata per una versione precedente di Windows ed esegue il rendering dell'interfaccia utente dell'applicazione simulando il modello Windows tema classico.

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a>Aggiunta di una sezione di compatibilità al manifesto dell'applicazione

Un manifesto dell'applicazione è un file XML che descrive i requisiti per un'applicazione. La sezione relativa alla compatibilità del manifesto identifica le versioni Windows supportate dall'applicazione. I GUID seguenti vengono usati nella sezione relativa alla compatibilità per identificare le varie versioni di Windows.

| Versione       | GUID                                   |
|---------------|----------------------------------------|
| Windows Vista | {e2011457-1546-43c5-a5fe-008deee3d3f0} |
| Windows 7     | {35138b9a-5d96-4fbd-8e2d-a2440225f93a} |
| Windows 8     | {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} |



 

La sezione compatibility può specificare più versioni di Windows, ma ognuna deve essere contenuta all'interno del proprio `<supportedOS/>` tag. L'esempio seguente illustra un manifesto dell'applicazione che specifica Windows 7 e Windows 8 nella sezione relativa alla compatibilità:


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



Se un'applicazione non ha un manifesto di compatibilità, si presuppone che sia un'applicazione Windows Vista e non usa controlli con temi nell'area client quando è attivo un tema a contrasto elevato. Inoltre, il comportamento di alcune funzioni degli stili di visualizzazione è influenzato. Ad esempio, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)e [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) restituiscono FALSE, mentre [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) e [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) restituiscono un handle NULL. Ciò è necessario per il supporto della compatibilità, in modo che le applicazioni compilate prima di Windows 8 possano comunque eseguire il rendering dell'interfaccia utente nello stesso aspetto della modalità a contrasto elevato delle versioni precedenti di Windows in cui gli stili di visualizzazione non sono disponibili.

In Windows 8, l'applicazione riceve comunque i vantaggi della composizione desktop. Ciò significa, ad esempio, che le applicazioni di usabilità, ad esempio la lente di ingrandimento a schermo intero, non dipendono dello stato del manifesto di una singola applicazione. L'applicazione di usabilità continua a funzionare in modalità a contrasto elevato con un'applicazione che non si identifica come Windows 8 compatibile nel manifesto.

Le immagini seguenti mostrano una semplice finestra di dialogo a contrasto elevato Windows 7.

![Finestra di dialogo contrasto hig](images/win7-high-contrast.png)

Questa immagine mostra la stessa finestra di dialogo a contrasto elevato Windows 8, ma con la compatibilità Windows 7 specificata nel manifesto dell'applicazione:

![Finestra di dialogo a contrasto elevato w8](images/win7-compat.png)

Questa immagine mostra la stessa finestra di dialogo a contrasto elevato Windows 8, con Windows 8 specificato nel manifesto dell'applicazione:

![Finestra di dialogo a contrasto elevato w8 con manifesto](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a>Rilevamento Contrasto elevato nelle versioni precedenti di Windows

Le applicazioni in esecuzione in versioni precedenti Windows non hanno accesso ai nuovi temi a contrasto elevato. Se l'applicazione deve essere eseguita in versioni precedenti di , è necessario includere il supporto per il rendering dell'interfaccia utente in contraWindowsst elevato nel modello Windows tema classico. L'applicazione può determinare se un tema a contrasto elevato è attivo chiamando la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con il flag **SPI \_ GETHIGHCONTRAST.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione degli stili di visualizzazione](cookbook-overview.md)
</dt> <dt>

[Stili di visualizzazione](themes-overview.md)
</dt> </dl>

 

 