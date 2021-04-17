---
title: Gestione finestre desktop è sempre attiva
description: Gestione finestre desktop è sempre attiva
ms.assetid: 36E2DD1B-E480-47A9-850B-3057119641C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f855635615dee734b9a719d4e51d3ead663d144e
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104339415"
---
# <a name="desktop-window-manager-is-always-on"></a>Gestione finestre desktop è sempre attiva

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

In Windows 8, Gestione finestre desktop (DWM) è sempre attivo e non può essere disabilitato dagli utenti finali e dalle app. Come in Windows 7, DWM viene usato per comporre il desktop. Oltre alle esperienze abilitate in Windows 7, la composizione desktop di DWM consente la composizione del desktop per tutti i temi, il supporto per 3D stereoscopico e la gestione, la separazione e la protezione dell'esperienza con le app di Windows Store.

**Composizione del desktop per tutti i temi**

In Windows Vista e Windows 7, la composizione del desktop è abilitata solo con il tema AERO Glass. Di conseguenza, gli utenti di temi di Windows classico e a contrasto elevato non possono usare le esperienze abilitate dalla composizione desktop, ad esempio Windows Flip, ridimensionamento automatico per la scalabilità ad alta risoluzione (DPI), anteprima anteprime e Magnifier schermo intero. Inoltre, in queste versioni precedenti di Windows, gli sviluppatori di app devono scrivere e gestire più percorsi di codice, uno in cui la composizione del desktop è abilitata e un'altra in cui la composizione del desktop è disabilitata.

Con Windows 8, la composizione del desktop è abilitata per tutti i temi. Gli utenti di temi di Windows classico e a contrasto elevato possono usare le esperienze abilitate dalla composizione desktop, ad esempio Windows Flip, ridimensionamento automatico per la scalabilità ad alta risoluzione (DPI), anteprime anteprime e lente di ingrandimento schermo intero. Inoltre, gli sviluppatori non devono scrivere e gestire più percorsi di codice, semplificando così lo sviluppo.

**Supporto per Stereoscopic 3D**

La composizione desktop di DWM supporta il rendering e la presentazione di contenuto di app 3D stereoscopico a schermo intero e con finestra.

**Gestione, separazione e protezione dell'esperienza con le app di Windows Store**

La composizione desktop di DWM consente la separazione e la protezione delle finestre delle app desktop dalle nuove finestre delle app di Windows Store gestendo e separando le finestre delle app desktop dalle finestre delle app di Windows Store. Poiché la composizione del desktop è responsabile della gestione di tutte le finestre delle app, la disabilitazione della composizione del desktop può causare un comportamento imprevisto. Inoltre, la composizione del desktop è responsabile della composizione del nuovo menu Start, nonché di animazioni finestra aggiuntive che costituiscono la personalità principale del nuovo sistema operativo Windows.

## <a name="controlling-desktop-composition"></a>Controllo della composizione del desktop

In Windows Vista e Windows 7, la composizione del desktop è disabilitata in diversi scenari. In Windows 8, la composizione desktop di DWM è un componente principale del sistema operativo e non può essere disabilitata. Con alcune eccezioni, la composizione del desktop è sempre attiva; viene avviato prima dell'accesso dell'utente e rimane attivo per la durata di una sessione. In questa sezione viene descritto in che modo Windows 8 considera gli scenari di Windows 7 in cui la composizione del desktop è disabilitata.

**SKU del server e alcuni SKU client**

In Windows 8 tutti gli SKU server e client hanno la composizione desktop abilitata. In questo modo si garantisce che gli amministratori del server e gli utenti possano trarre vantaggio dalle esperienze abilitate dalla composizione desktop.

**Requisiti fondamentali per la composizione del desktop**

Windows 8 garantisce che i requisiti della scheda grafica e della profondità dei colori del sistema vengano soddisfatti tramite il supporto del driver WDDM e la profondità dei colori del sistema.

**Supporto driver WDDM**

Se un sistema non dispone di un driver di grafica conforme a WDDM, Windows 8 utilizza la scheda di visualizzazione di Microsoft Basic come adattatore predefinito. Poiché DWM viene sempre eseguito sulla scheda predefinita, l'adapter di visualizzazione di Microsoft Basic verrà scelto per comporre il desktop quando il driver di grafica conforme a WDDM non è disponibile (se non è installato o disabilitato) nel sistema.

Microsoft Basic Display Adapter è un rasterizzatore software che utilizza la CPU anziché la GPU per eseguire tutto il disegno. Si noti che le prestazioni della composizione del desktop in una scheda di visualizzazione di base di Microsoft (in particolare animazioni) potrebbero non essere altrettanto semplici quando si esegue la composizione del desktop su una GPU.

**Profondità colore sistema**

La composizione del desktop non può essere eseguita a meno che la profondità di colore non sia impostata su 32 bit per pixel. In Windows 7 è possibile modificare la profondità dei colori del sistema in questi scenari:

-   Un utente finale usa il pannello di controllo di visualizzazione di Windows o un pannello di controllo di terze parti per modificare il colore di sistema
-   Un utente finale esegue un'app che modifica la profondità dei colori del sistema tramite un'API pubblica

Diversamente da Windows 7, Windows 8 non supporta la profondità di colore oltre 32 bit per pixel. L'utente non può più modificare la profondità dei colori del sistema tramite il pannello di controllo.

Inoltre, gli sviluppatori di app non possono usare le API per modificare la profondità del colore del sistema. Windows 8 rileverà le app che tentano di modificare la profondità dei colori del sistema a meno di 32 bit per pixel e informare l'utente che è necessario applicare uno shim di compatibilità delle app per eseguire le app. Dopo la conferma da parte dell'utente, viene applicato lo shim di compatibilità delle app e lo shim virtualizza la modalità di colore basso per l'app mantenendo il sistema in esecuzione a 32 bit per pixel.

**Strumento Valutazione sistema Windows**

In Windows 8, la composizione del desktop non dipende dai punteggi di WinSAT. Inoltre, WinSAT non include più la valutazione di DWM.

**Compatibilità delle app e azione dell'utente**

In Windows 8:

-   Tutte le opzioni per la disabilitazione della composizione del desktop presenti nella finestra 7 vengono rimosse
-   Composizione del desktop è responsabile della composizione di tutti i temi
-   Le app non possono usare DwmEnableComposition per disabilitare la composizione del desktop. Per mantenere la compatibilità con le versioni precedenti, una chiamata a questa API restituirà l'esito positivo; Tuttavia, la composizione del desktop non è disabilitata
-   Lo shim "Disabilita composizione desktop" è stato rimosso
-   L'opzione "Disabilita composizione desktop" dalla scheda compatibilità della finestra di dialogo Proprietà applicazione è stata rimossa

**Un'app utilizza un driver di mirroring per la comunicazione remota**

In Windows 8:

-   Non supporta i driver mirror per gli scenari di comunicazione remota; Sebbene la maggior parte delle app esistenti che utilizzano i driver mirror continui a funzionare, a causa della modifica dell'infrastruttura necessaria per supportare i driver mirror esistenti in Windows 8 con DWM, alcune funzionalità o app che utilizzano driver mirror potrebbero non funzionare
-   Supporta le API di duplicazione desktop per gli sviluppatori di app che usano driver mirror per gli scenari di comunicazione remota.
-   Non supporta driver mirror di accessibilità esistenti
-   Per assicurarsi che siano compatibili con Windows 8, è necessario aggiornare i driver mirror esistenti

**Connessione Desktop remoto**

In Windows 8, la composizione del desktop è sempre abilitata per una connessione Desktop remoto. Un computer client che si connette a un computer remoto Windows 8 otterrà sempre la composizione desktop abilitata per la sessione Desktop remoto indipendentemente dalla versione del client Windows. La composizione del desktop è supportata per più monitor nel computer client e per la sessione dell'app remota.

Inoltre, quando ci si connette a un computer remoto Windows 8, queste impostazioni nel client Connessione Desktop remoto non diventano effettive:

-   Profondità colore
-   Casella di controllo "Abilita composizione"

La profondità di colore della connessione è sempre impostata su 32 bit per pixel e la composizione del desktop è sempre abilitata.

 

 




