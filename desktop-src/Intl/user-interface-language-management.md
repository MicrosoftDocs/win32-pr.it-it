---
description: MUI consente alle applicazioni di gestire le lingue dell'interfaccia utente in due modi.
ms.assetid: ae8ab98f-dc3b-414d-85c9-6bf204c2f776
title: Interfaccia utente language management
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aaf20ca6183109f81572eeb706673812fc988eca87ea2522f437eafd22774b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631841"
---
# <a name="user-interface-language-management"></a>Interfaccia utente language management

MUI consente alle applicazioni di gestire le lingue dell'interfaccia utente in due modi. Un'applicazione può usare un approccio semplice alla gestione della lingua impostando per impostazione predefinita le impostazioni della lingua del sistema operativo. In alternativa, l'applicazione può supportare le proprie lingue da cui l'utente può selezionare. L'API MUI consente anche all'applicazione l'accesso diretto alle lingue e agli elenchi di lingue supportati dal sistema operativo e gestiti dal caricatore di risorse. Nella parte restante di questo argomento vengono definite le lingue supportate dal sistema e il meccanismo di fallback della lingua.

## <a name="languages-maintained-by-the-operating-system"></a>Lingue gestite dal sistema operativo

### <a name="system-default-ui-languageinstall-language"></a>Lingua dell'interfaccia utente predefinita del sistema/Lingua di installazione

La lingua predefinita dell'interfaccia utente di sistema è la lingua della versione localizzata usata per configurare Windows. Tutti i menu, le finestre di dialogo, i messaggi di errore e i file della Guida sono rappresentati in questa lingua, tranne quando l'utente seleziona una lingua diversa.

In Windows Vista e versioni successive, la lingua dell'interfaccia utente predefinita del sistema è nota come "lingua di installazione" e svolge un ruolo più limitato. Per la maggior parte degli scopi, viene sostituito dalle lingue dell'interfaccia utente preferite dal sistema. Tuttavia, in determinati contesti è utile avere un'unica lingua di installazione che sia sempre supportata completamente.

Non è disponibile alcuna funzione MUI per impostare la lingua dell'interfaccia utente predefinita del sistema. Per recuperare questa lingua, l'applicazione può chiamare [**GetSystemDefaultUILanguage.**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)

### <a name="system-ui-language"></a>Lingua dell'interfaccia utente di sistema

Il sistema operativo definisce la lingua dell'interfaccia utente del sistema come lingua dell'interfaccia utente che può essere impostata da un amministratore nella **scheda** Avanzate della parte relativa alle opzioni internazionali e della lingua Pannello di controllo. Il sistema operativo usa questa lingua se l'utente corrente non ha effettuato impostazioni specifiche per la lingua o se non è stato eseguito l'accesso ad alcun account attivo. La lingua può essere modificata solo se nel computer sono installate più lingue dell'interfaccia utente.

> [!Note]  
> Per visualizzare l'effetto della modifica della lingua, è necessario riavviare il sistema operativo per tutti gli utenti e i servizi.

 

Non è disponibile alcuna funzione MUI per impostare la lingua dell'interfaccia utente del sistema. Per recuperare questo valore, un'applicazione destinata a Windows Vista e versioni successive può chiamare [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) e ottenere la prima lingua nell'elenco delle lingue dell'interfaccia utente preferite del sistema. Le applicazioni destinate a sistemi operativi Precedenti Windows Vista non possono usare [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) e devono basarsi sul presupposto che la lingua dell'interfaccia utente del sistema sia sempre la stessa della lingua dell'interfaccia utente predefinita del sistema.

### <a name="user-ui-language"></a>Lingua dell'interfaccia utente

La lingua dell'interfaccia utente determina la lingua dell'interfaccia utente usata per menu, finestre di dialogo, file della Guida e così via. Può essere impostato dall'utente corrente nella scheda **Lingua** della parte relativa alle opzioni internazionali e della lingua Pannello di controllo. Questa lingua può essere modificata solo se nel computer sono installate più lingue dell'interfaccia utente. Si noti che l'utente dovrà disconnettersi e quindi accedere di nuovo per visualizzare l'effetto. Ad esempio, un'azienda multinazionale vuole distribuire Windows in tutte le filiali. La società crea un processo di installazione globale, che installa la versione in lingua inglese di Windows in tutti i client, indipendentemente dalla posizione. Allo stesso tempo, installa moduli linguistici specifici a seconda dell'unità organizzativa di cui un computer è membro. Quando l'utente accede per la prima volta a un sistema operativo appena installato, Windows viene visualizzato come versione localizzata.

In Windows Vista e versioni successive, la lingua dell'interfaccia utente è la prima lingua nell'elenco delle lingue preferite dell'utente. Si noti che le lingue di fallback possono essere usate se determinate risorse non sono disponibili in questa lingua.

Nei sistemi operativi precedenti Windows Vista, la lingua dell'interfaccia utente dell'utente è in genere la stessa della lingua dell'interfaccia utente predefinita del sistema. Tuttavia, per Windows MUI, le due lingue possono essere diverse.

Per recuperare la lingua dell'interfaccia utente, un'applicazione può chiamare [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage) o [**GetUserPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages) L'applicazione non può modificare la lingua dell'interfaccia utente, perché non esiste alcuna funzione per impostarla.

## <a name="language-lists-maintained-by-the-operating-system"></a>Elenchi di lingue gestiti dal sistema operativo

### <a name="system-preferred-ui-languages-list"></a>Elenco delle lingue preferite dell'interfaccia utente di sistema

Il caricatore di risorse gestisce un elenco di lingue dell'interfaccia utente preferite dal sistema. In questo elenco sono incluse le lingue preferite dal sistema operativo per le proprie risorse, ad esempio menu e finestre di dialogo, messaggi, file INF e file della Guida. L'elenco è costituito dalla lingua dell'interfaccia utente predefinita del sistema, dalla lingua dell'interfaccia utente di sistema e dai relativi fallback. Un'applicazione può recuperare le lingue dell'interfaccia utente preferite dal sistema chiamando [**GetSystemPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)

### <a name="user-preferred-ui-languages-list"></a>Elenco delle lingue preferite dell'interfaccia utente

Il caricatore di risorse usa un elenco di lingue preferite dell'interfaccia utente che include le lingue preferite dall'utente. Il caricatore di risorse usa le risorse corrispondenti alle lingue di questo elenco, se disponibili, per un particolare thread dell'applicazione. Queste lingue hanno la precedenza su qualsiasi preferenza di sistema. Per recuperare le lingue preferite dell'interfaccia utente, l'applicazione può [**chiamare GetUserPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)

### <a name="process-preferred-ui-languages-list"></a>Elaborare l'elenco delle lingue preferite dell'interfaccia utente

In Windows Vista e versioni successive, il caricatore di risorse gestisce un elenco di lingue dell'interfaccia utente preferite dal processo costituito da un massimo di cinque lingue valide impostate da un processo in esecuzione per un'applicazione MUI. Le lingue possono essere impostate dall'applicazione con una chiamata a [**SetProcessPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) L'applicazione può recuperare le lingue chiamando [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages).

### <a name="thread-preferred-ui-languages-list"></a>Elenco delle lingue preferite dell'interfaccia utente per i thread

In Windows Vista e versioni successive il caricatore di risorse usa un elenco di lingue dell'interfaccia utente preferite del thread costituito da un massimo di cinque lingue valide impostate da un thread in un processo in esecuzione per un'applicazione MUI. Queste lingue vengono usate per personalizzare le lingue dell'interfaccia utente dell'applicazione e renderle diverse dalla lingua del sistema operativo. L'elenco delle lingue preferite dell'interfaccia utente per i thread si basa sulle lingue dell'interfaccia utente preferite dall'utente, sulle lingue dell'interfaccia utente preferite dal sistema e sulla lingua dell'interfaccia utente predefinita del sistema.

Per impostare le lingue dell'interfaccia utente preferite del thread, l'applicazione deve [**chiamare SetThreadPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) Per recuperare queste lingue, l'applicazione chiama [**GetThreadPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)

## <a name="neutral-language-representation"></a>Rappresentazione della lingua neutra

Una lingua neutra è rappresentata solo come lingua, senza area o impostazioni locali. Ad esempio, la rappresentazione neutra della lingua inglese (Canada), en-CA, è rappresentata come "en". Anche se una lingua neutra non è associata agli aspetti di un'area o di impostazioni locali, è possibile associarla a un set di risorse. In genere, una risorsa lingua neutra si basa sull'uso nell'area più prevalente per la lingua.

Si supponga, ad esempio, che l'applicazione MUI localizzi le risorse della lingua tedesca (Svizzera) rappresentate come de-CH e il tedesco (Germania) rappresentato come de-AT, creando un set completo di risorse per il tedesco (Germania) rappresentato come de-DE. È necessario prendere decisioni per questa applicazione considerando interi file di risorse. Se l'applicazione duplica le risorse de-DE come risorse della lingua neutra, deve fornire una lingua di fallback per il caricatore di risorse. Se il caricatore non trova un file di risorse specifico della lingua specifico per de-CH o de-AT, esegue il falls back alle risorse "de" indipendenti dalla lingua. Queste risorse sono probabilmente più appropriate delle risorse per una lingua completamente diversa, ad esempio l'inglese (Stati Uniti), che sono gli unici altri fallback possibili.

Come altro esempio, un'applicazione potrebbe non essere affatto locale per Poiize. Tuttavia, il supporto di una preferenza di lingua dell'inglese (Sottotitolize), rappresentato come en-BZ, consente all'applicazione di eseguire il fall back alle risorse "en".

## <a name="language-fallback-in-the-resource-loader"></a>Fallback del linguaggio nel caricatore di risorse

Windows Vista e versioni successive dispongono le impostazioni della lingua dell'interfaccia utente in un elenco di lingue di fallback pre-ordinato usato dal caricatore di risorse. Per formare l'elenco, il sistema operativo combina diverse lingue, nell'ordine indicato:

-   Lingue dell'interfaccia utente preferite dei thread, costituite dalla lingua dell'interfaccia utente del thread e dalla relativa forma neutra. Ad esempio, fr-FR per il francese (Francia) e la forma neutra "fr" ed es-ES per lo spagnolo (Spagna) e la forma neutra "es".
-   Elaborare le lingue preferite dell'interfaccia utente, costituite dalla lingua dell'interfaccia utente del processo e dalla relativa forma neutra. Un esempio è de-DE per il tedesco (Germania) e la sua forma neutra "de".
-   Lingua dell'interfaccia utente e forma neutra. Un esempio è ja-JP per giapponese (Giappone) e la sua forma neutra "ja".
-   Lingua dell'interfaccia utente del sistema e forma neutra. Un esempio è it-IT per l'italiano (Italia) e la sua forma neutra "it".
    > [!Note]  
    > Questa lingua è inclusa nell'elenco di fallback solo quando la lingua dell'interfaccia utente non è impostata.

     

-   Lingua dell'interfaccia utente predefinita del sistema e forma neutra. Un esempio è es-ES per spagnolo (Spagna) e la sua forma neutra "es".

Di seguito viene illustrato l'elenco di fallback unito. Si noti che la duplicazione delle lingue, ad esempio es-ES ed es, viene eliminata. Poiché l'esempio imposta la lingua dell'interfaccia utente su ja-JP, la lingua dell'interfaccia utente di sistema non viene visualizzata nell'elenco di fallback unito.

fr-FR, fr, es-ES, es, de-DE, de, ja-JP, ja

Quando si caricano risorse per un'applicazione MUI, il caricatore di risorse tenta di selezionare uno dei file corrispondenti all'elenco delle lingue preferite dell'interfaccia utente per il thread dell'applicazione attualmente in esecuzione. Se il caricatore di risorse non riesce a trovare una corrispondenza diretta tra una lingua selezionata e la prima risorsa specifica della lingua nell'elenco di fallback unito, controlla le lingue successive nell'elenco finché non trova un fallback accettabile.

Se il caricatore di risorse non trova alcun file necessario, deve usare un linguaggio di fallback "valido" garantito. Per la tecnologia delle risorse MUI, il caricatore di risorse determina la lingua di fallback dai dati di configurazione delle risorse forniti. Per altre informazioni, vedere [MUI Resource Management](mui-resource-management.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni interfaccia utente multilingue](about-multilingual-user-interface.md)
</dt> <dt>

[Impostazioni locali e lingue](locales-and-languages.md)
</dt> <dt>

[Terminologia NLS](nls-terminology.md)
</dt> </dl>

 

 



