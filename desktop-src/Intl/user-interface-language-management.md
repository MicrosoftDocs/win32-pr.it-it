---
description: MUI consente alle applicazioni di gestire le lingue dell'interfaccia utente in due modi.
ms.assetid: ae8ab98f-dc3b-414d-85c9-6bf204c2f776
title: Gestione della lingua dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852fe20d3edb9795c2c2a9d3ec45c1e8ffe053ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401791"
---
# <a name="user-interface-language-management"></a>Gestione della lingua dell'interfaccia utente

MUI consente alle applicazioni di gestire le lingue dell'interfaccia utente in due modi. Per impostazione predefinita, un'applicazione può usare un approccio semplice alla gestione del linguaggio per le impostazioni della lingua del sistema operativo. In alternativa, l'applicazione può supportare le proprie lingue da cui l'utente può selezionare. L'API MUI consente inoltre all'applicazione di accedere direttamente a linguaggi e elenchi di lingue supportati dal sistema operativo e gestiti dal caricatore di risorse. Nella parte restante di questo argomento vengono definiti i linguaggi supportati dal sistema e il meccanismo di fallback del linguaggio.

## <a name="languages-maintained-by-the-operating-system"></a>Lingue gestite dal sistema operativo

### <a name="system-default-ui-languageinstall-language"></a>Lingua dell'interfaccia utente predefinita del sistema/lingua di installazione

La lingua dell'interfaccia utente predefinita del sistema è la lingua della versione localizzata utilizzata per configurare Windows. Tutti i menu, le finestre di dialogo, i messaggi di errore e i file della guida sono rappresentati in questa lingua, tranne quando l'utente seleziona una lingua diversa.

In Windows Vista e versioni successive la lingua dell'interfaccia utente predefinita del sistema è nota come "lingua di installazione" e svolge un ruolo più limitato. Per la maggior parte degli scopi, viene sostituito dalle lingue dell'interfaccia utente preferite dal sistema. Tuttavia, in alcuni contesti è utile avere una sola lingua di installazione che è sempre nota come completamente supportata.

Non è disponibile alcuna funzione MUI per impostare la lingua dell'interfaccia utente predefinita del sistema. Per recuperare questa lingua, l'applicazione può chiamare [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage).

### <a name="system-ui-language"></a>Lingua dell'interfaccia utente del sistema

Il sistema operativo definisce la lingua dell'interfaccia utente del sistema come lingua dell'interfaccia utente che può essere impostata da un amministratore nella scheda **Avanzate** della parte opzioni internazionali e della lingua del pannello di controllo. Il sistema operativo usa questa lingua se l'utente corrente non ha apportato impostazioni della lingua specifiche o se non è stato effettuato l'accesso ad alcun account attivo. Il linguaggio può essere modificato solo se nel computer è installata più di una lingua dell'interfaccia utente.

> [!Note]  
> Il sistema operativo deve essere riavviato per tutti gli utenti e i servizi per vedere l'effetto della modifica della lingua.

 

Non è disponibile alcuna funzione MUI per impostare la lingua dell'interfaccia utente del sistema. Per recuperare questo valore, un'applicazione destinata a Windows Vista e versioni successive può chiamare [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) e ottenere la prima lingua nell'elenco delle lingue dell'interfaccia utente preferite dal sistema. Le applicazioni destinate ai sistemi operativi precedenti a Windows Vista non possono utilizzare [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) e devono basarsi sul presupposto che la lingua dell'interfaccia utente del sistema sia sempre identica alla lingua dell'interfaccia utente predefinita del sistema.

### <a name="user-ui-language"></a>Lingua dell'interfaccia utente

La lingua dell'interfaccia utente determina la lingua dell'interfaccia utente utilizzata per menu, finestre di dialogo, file della guida e così via. Può essere impostato dall'utente corrente nella scheda **lingua** della parte opzioni internazionali e della lingua del pannello di controllo. Questa lingua può essere modificata solo se nel computer è installata più di una lingua dell'interfaccia utente. Si noti che l'utente dovrà disconnettersi e quindi accedere di nuovo per vedere l'effetto. Ad esempio, un'azienda multinazionale vuole distribuire Windows in tutte le sue consociate. La società crea un processo di installazione globale, che installa la versione in lingua inglese di Windows in tutti i client, indipendentemente dalla posizione. Allo stesso tempo, installa moduli di linguaggio specifici in base all'unità organizzativa di cui un computer è membro. Quando l'utente accede per la prima volta a un sistema operativo appena installato, Windows viene visualizzato come versione localizzata.

In Windows Vista e versioni successive la lingua dell'interfaccia utente è la prima lingua nell'elenco lingue dell'interfaccia utente preferite dall'utente. Si noti che è possibile usare le lingue di fallback se determinate risorse non sono disponibili in questa lingua.

Nei sistemi operativi precedenti a Windows Vista la lingua dell'interfaccia utente è in genere identica alla lingua dell'interfaccia utente predefinita del sistema. Tuttavia, per Windows MUI, le due lingue possono essere diverse.

Per recuperare la lingua dell'interfaccia utente, un'applicazione può chiamare [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage) o [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages). L'applicazione non può modificare la lingua dell'interfaccia utente, perché non è disponibile alcuna funzione per impostarla.

## <a name="language-lists-maintained-by-the-operating-system"></a>Elenchi di lingue gestiti dal sistema operativo

### <a name="system-preferred-ui-languages-list"></a>Elenco lingue dell'interfaccia utente preferite dal sistema

Il caricatore di risorse gestisce un elenco di lingue dell'interfaccia utente preferito dal sistema. Sono incluse in questo elenco le lingue preferite dal sistema operativo per le proprie risorse, ad esempio menu e finestre di dialogo, messaggi, file INF e file della guida. L'elenco è costituito dalla lingua dell'interfaccia utente predefinita del sistema e dalla lingua dell'interfaccia utente del sistema e dai relativi fallback. Un'applicazione può recuperare le lingue dell'interfaccia utente preferite dal sistema chiamando [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages).

### <a name="user-preferred-ui-languages-list"></a>Elenco lingue UI preferite dall'utente

Il caricatore di risorse utilizza un elenco di lingue UI preferite dall'utente che include le lingue preferite dall'utente. Il caricatore di risorse usa le risorse corrispondenti alle lingue da questo elenco, se disponibili, per un particolare thread dell'applicazione. Questi linguaggi hanno la precedenza su tutte le preferenze di sistema. Per recuperare le lingue dell'interfaccia utente preferite dall'utente, l'applicazione può chiamare [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages).

### <a name="process-preferred-ui-languages-list"></a>Elenco delle lingue dell'interfaccia utente preferite del processo

In Windows Vista e versioni successive, il caricatore di risorse gestisce un elenco di linguaggi di interfaccia utente preferiti da un processo costituito da un massimo di cinque lingue valide impostate da un processo in esecuzione per un'applicazione MUI. Le lingue possono essere impostate dall'applicazione con una chiamata a [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages). L'applicazione può recuperare le lingue chiamando [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages).

### <a name="thread-preferred-ui-languages-list"></a>Elenco di lingue dell'interfaccia utente preferite dal thread

In Windows Vista e versioni successive, il caricatore di risorse utilizza un elenco di lingue dell'interfaccia utente preferite dal thread, costituito da un massimo di cinque lingue valide impostate da un thread in un processo in esecuzione per un'applicazione MUI. Questi linguaggi vengono usati per personalizzare le lingue dell'interfaccia utente dell'applicazione e renderli diversi dalla lingua del sistema operativo. L'elenco di lingue dell'interfaccia utente preferita dal thread si basa sulle lingue dell'interfaccia utente preferite dall'utente, le lingue dell'interfaccia utente preferite del sistema e la lingua dell'interfaccia utente predefinita del sistema.

Per impostare le lingue dell'interfaccia utente preferite per il thread, l'applicazione deve chiamare [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Per recuperare questi linguaggi, l'applicazione chiama [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages).

## <a name="neutral-language-representation"></a>Rappresentazione della lingua neutra

Una lingua neutra viene rappresentata solo come lingua, senza regione o impostazioni locali. Ad esempio, la rappresentazione neutra della lingua inglese (Canada), en-CA, viene rappresentata come "en". Anche se un linguaggio neutro non è associato agli aspetti di un'area o di impostazioni locali, è possibile associarlo a un set di risorse. In genere, una risorsa di lingua neutra è basata sull'uso nell'area più diffusa per la lingua.

Si supponga, ad esempio, che l'applicazione MUI localizza le risorse di lingua tedesca per la Germania (Svizzera) rappresentate come de-CH e la Germania (Austria) rappresentate come de-AT, durante la creazione di un set completo di risorse per la lingua tedesca (Germania) rappresentata come de-DE. È necessario prendere decisioni per questa applicazione considerando interi file di risorse. Se l'applicazione duplica le risorse de-DE come risorse della lingua neutra, deve fornire una lingua di fallback per il caricatore di risorse. Se il caricatore non trova un file di risorse specifico della lingua per de-CH o per de-AT, viene eseguito il fallback alle risorse "de" indipendenti dalla lingua. Queste risorse sono molto probabilmente più appropriate delle risorse per un linguaggio completamente diverso, ad esempio inglese (Stati Uniti), che sono gli unici altri possibili fallback.

Come altro esempio, un'applicazione potrebbe non essere localizzata per Belize. Tuttavia, il supporto di una preferenza per la lingua inglese (Belize), rappresentato come en-BZ, consente all'applicazione di eseguire il fallback alle risorse "en".

## <a name="language-fallback-in-the-resource-loader"></a>Fallback della lingua nel caricatore di risorse

Windows Vista e versioni successive dispongono di impostazioni della lingua dell'interfaccia utente in un elenco di linguaggi di fallback preordinato usato dal caricatore di risorse. Per creare l'elenco, il sistema operativo combina varie lingue nell'ordine indicato:

-   Lingue dell'interfaccia utente preferite dai thread, costituite dalla lingua dell'interfaccia utente del thread e dal relativo formato neutro. Gli esempi sono fr-FR per il francese (Francia) e il relativo formato neutro "fr" ed es-ES per spagnolo (Spagna) e il relativo formato neutro "es".
-   Elabora le lingue dell'interfaccia utente preferite, costituite dalla lingua dell'interfaccia utente del processo e dal relativo formato neutro. Un esempio è de-DE per il tedesco (Germania) e il relativo formato neutro "de".
-   Lingua dell'interfaccia utente e relativo formato neutro. Un esempio è ja-JP per il giapponese (Giappone) e il relativo formato neutro "ja".
-   Lingua dell'interfaccia utente del sistema e relativo formato neutro. Un esempio è it per l'italiano (Italia) e il suo formato neutro "it".
    > [!Note]  
    > Questa lingua è inclusa nell'elenco di fallback solo quando la lingua dell'interfaccia utente non è impostata.

     

-   Lingua dell'interfaccia utente predefinita del sistema e relativo formato neutro. Un esempio è es-ES per spagnolo (Spagna) e il relativo formato neutro "es".

Di seguito viene illustrato l'elenco di fallback Unito. Si noti che la duplicazione di linguaggi, ad esempio es-ES ed es, viene eliminata. Poiché l'esempio imposta la lingua dell'interfaccia utente su ja-JP, la lingua dell'interfaccia utente del sistema non viene visualizzata nell'elenco di fallback Unito.

fr-FR, fr, es-ES, es, de-DE, de, ja-JP, ja

Quando si caricano risorse per un'applicazione MUI, il caricatore di risorse tenta di selezionare uno dei file corrispondenti all'elenco di lingue dell'interfaccia utente preferito dal thread per il thread dell'applicazione attualmente in esecuzione. Se il caricatore di risorse non riesce a trovare una corrispondenza diretta tra una lingua selezionata e la prima risorsa specifica della lingua nell'elenco di fallback Unito, controlla le lingue successive nell'elenco fino a quando non trova un fallback accettabile.

Se il caricatore di risorse non trova alcun file necessario, deve usare un linguaggio di fallback "garantito valido". Per la tecnologia delle risorse MUI, il caricatore di risorse determina la lingua di fallback dai dati di configurazione delle risorse forniti. Per ulteriori informazioni, vedere [gestione delle risorse MUI](mui-resource-management.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'interfaccia utente multilingue](about-multilingual-user-interface.md)
</dt> <dt>

[Impostazioni locali e lingue](locales-and-languages.md)
</dt> <dt>

[Terminologia NLS](nls-terminology.md)
</dt> </dl>

 

 



