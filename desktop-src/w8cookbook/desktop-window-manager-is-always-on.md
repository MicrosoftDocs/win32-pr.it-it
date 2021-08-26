---
title: Gestione finestre desktop è sempre on
description: Gestione finestre desktop è sempre on
ms.assetid: 36E2DD1B-E480-47A9-850B-3057119641C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b256b4270ab0bbeba588a4beff9bd1bd2bbe1c8166b40cd527f8b48a4f897df0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057361"
---
# <a name="desktop-window-manager-is-always-on"></a>Gestione finestre desktop è sempre on

## <a name="platforms"></a>Piattaforme

**Client** : Windows 8  
**Server** - Windows Server 2012  


## <a name="description"></a>Descrizione

In Windows 8, Gestione finestre desktop (DWM) è sempre ON e non può essere disabilitato dagli utenti finali e dalle app. Come nella Windows 7, DWM viene usato per comporre il desktop. Oltre alle esperienze abilitate in Windows 7, ora la composizione desktop DWM consente la composizione desktop per tutti i temi, il supporto per 3D stereoscopico e la gestione, la separazione e la protezione dell'esperienza con le app di Windows Store.

**Composizione del desktop per tutti i temi**

In Windows Vista e Windows 7, la composizione desktop è abilitata solo con il tema di cristallo AERO. Di conseguenza, gli utenti Windows temi classici e a contrasto elevato non possono usare esperienze abilitate dalla composizione desktop, ad esempio Windows Flip, scalabilità automatica per la scalabilità DPI (High Resolution), anteprima anteprima e lente di ingrandimento a schermo intero. Inoltre, in queste versioni precedenti di Windows, gli sviluppatori di app devono scrivere e gestire più percorsi di codice, uno in cui la composizione desktop è abilitata e l'altra in cui la composizione desktop è disabilitata.

Con Windows 8, la composizione del desktop è abilitata per tutti i temi. Gli utenti Windows temi classici e a contrasto elevato possono usare le esperienze abilitate dalla composizione desktop, ad esempio Windows Flip, ridimensionamento automatico per il ridimensionamento DPI (High Resolution), anteprime di anteprima e lente di ingrandimento a schermo intero. Inoltre, gli sviluppatori non devono scrivere e gestire più percorsi di codice, semplificando così lo sviluppo.

**Supporto per 3D stereoscopico**

La composizione desktop DWM supporta il rendering e la presentazione del contenuto dell'app 3D stereoscopica stereoscopica e a schermo intero.

**Gestione, separazione e protezione dell'esperienza con Windows Store**

La composizione desktop DWM consente la separazione e la protezione delle finestre delle app desktop dalle nuove finestre dell'app Windows Store gestendo e separando le finestre dell'app desktop dalle finestre dell'app Windows Store. Poiché la composizione desktop è responsabile della gestione di tutte le finestre dell'app, la disabilitazione della composizione desktop può comportare un comportamento imprevisto. Inoltre, la composizione del desktop è responsabile della composizione del nuovo menu Start nonché di animazioni di finestre aggiuntive che costituiscono la personalità principale del nuovo Windows operativo.

## <a name="controlling-desktop-composition"></a>Controllo della composizione del desktop

In Windows Vista e Windows 7, la composizione desktop è disabilitata in diversi scenari. In Windows 8, la composizione desktop DWM è un componente principale del sistema operativo e non può essere disabilitata. Con alcune eccezioni, la composizione del desktop è sempre on; viene avviato prima dell'accesso dell'utente e rimane attivo per la durata di una sessione. Questa sezione descrive come Windows 8 gli scenari in Windows 7 in cui la composizione desktop è disabilitata.

**SKU del server e alcuni SKU client**

In Windows 8, tutti gli SKU server e client hanno la composizione desktop abilitata. Ciò garantisce che gli amministratori e gli utenti del server possano trarre vantaggio dalle esperienze abilitate dalla composizione desktop.

**Requisiti fondamentali per la composizione desktop**

Windows 8 garantisce che i requisiti di profondità dei colori della scheda grafica e del sistema siano soddisfatti tramite il supporto del driver WDDM e la profondità del colore del sistema.

**Supporto dei driver WDDM**

Se un sistema non dispone di un driver di grafica conforme a WDDM, Windows 8 l'adattatore schermo Di base Microsoft come scheda predefinita. Poiché DWM viene sempre eseguito sulla scheda predefinita, sceglierà Microsoft Basic Display Adapter per comporre il desktop quando un driver di grafica conforme a WDDM non è disponibile (indipendentemente dal fatto che non sia installato o disabilitato) nel sistema.

Microsoft Basic Display Adapter è un rasterizzatore software che usa la CPU anziché la GPU per eseguire tutto il disegno. Si noti che le prestazioni della composizione del desktop nella scheda video Di base Microsoft (in particolare le animazioni) potrebbero non essere uniformi come quando si esegue la composizione del desktop in una GPU.

**Profondità del colore di sistema**

Composizione desktop non può essere eseguita a meno che la profondità del colore non sia impostata su 32 bit per pixel. In Windows 7 la profondità del colore del sistema può essere modificata in questi scenari:

-   Un utente finale usa il pannello di Windows display o un pannello di controllo di terze parti per modificare il colore del sistema
-   Un utente finale esegue un'app che modifica la profondità del colore del sistema tramite un'API pubblica

A Windows 7, Windows 8 non supporta una profondità di colore diversa da 32 bit per pixel. L'utente non può più modificare la profondità del colore del sistema usando il pannello di controllo.

Inoltre, gli sviluppatori di app non possono usare le API per modificare la profondità del colore del sistema. Windows 8 rileva le app che tentano di modificare la profondità del colore del sistema a meno di 32 bit per pixel e informano l'utente che è necessario applicare uno shim di compatibilità dell'app per eseguire le app. Dopo la conferma da parte dell'utente, viene applicato lo shim di compatibilità dell'app e lo shim virtualizza la modalità a colori bassa all'app mantenendo il sistema in esecuzione a 32 bit per pixel.

**Strumento Valutazione sistema Windows**

In Windows 8, la composizione del desktop non dipende dai punteggi di WinSAT. Inoltre, WinSAT non include più la valutazione DWM.

**Compatibilità delle app e azione dell'utente**

In Windows 8:

-   Tutte le opzioni per la disabilitazione della composizione desktop presenti in Window 7 vengono rimosse
-   La composizione del desktop è responsabile della composizione di tutti i temi
-   Le app non possono usare DwmEnableComposition per disabilitare la composizione del desktop. Per mantenere la compatibilità con le versioni precedenti, una chiamata a questa API restituirà l'esito positivo. Tuttavia, la composizione del desktop non è disabilitata
-   Lo shim "Disabilita composizione desktop" viene rimosso
-   L'opzione "Disabilita composizione desktop" dalla scheda Compatibilità della finestra di dialogo Proprietà applicazione viene rimossa

**Un'app usa un driver di mirroring per la comunicazione remota**

In Windows 8:

-   Non supporta i driver mirror per gli scenari remoti. mentre la maggior parte delle app esistenti che usano driver mirror dovrebbe continuare a funzionare, a causa della modifica infrastrutturale necessaria per supportare i driver mirror esistenti in Windows 8 con DWM ON, alcune funzionalità o app che usano driver mirror potrebbero non funzionare
-   Supporta le API di duplicazione desktop per gli sviluppatori di app che usano driver mirror per scenari remoti.
-   Non supporta i driver mirror di accessibilità esistenti
-   I driver mirror esistenti devono essere aggiornati per assicurarsi che siano compatibili con Windows 8

**Connessione desktop remoto**

In Windows 8 la composizione desktop è sempre abilitata per una connessione desktop remoto. Un computer client che si connette a Windows 8 computer remoto otterrà sempre la composizione desktop abilitata per la sessione desktop remoto indipendentemente dalla Windows client. La composizione desktop è supportata per più monitor nel computer client e per la sessione dell'app remota.

Inoltre, quando ci si connette a Windows 8 computer remoto, queste impostazioni nel client Connessione Desktop remoto non hanno effetto:

-   Profondità del colore
-   Casella di controllo "Abilita composizione"

La profondità del colore della connessione è sempre impostata su 32 bit per pixel e la composizione del desktop è sempre abilitata.

 

 




