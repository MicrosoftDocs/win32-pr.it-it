---
description: In Windows Vista e Windows Server 2008, i percorsi predefiniti per i dati utente e i dati di sistema sono stati modificati.
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: Punti di giunzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310704"
---
# <a name="junction-points"></a>Punti di giunzione

In Windows Vista e Windows Server 2008, i percorsi predefiniti per i dati utente e i dati di sistema sono stati modificati. Ad esempio, i dati utente archiviati in precedenza nella directory% SystemDrive% \\ Documents and Settings sono ora archiviati nella directory% SystemDrive% \\ Users. Per compatibilità con le versioni precedenti, i percorsi precedenti hanno punti di giunzione che puntano alle nuove posizioni. Ad esempio, C: \\ Documents and Settings è ora un punto di giunzione che punta a c: \\ Users. Le applicazioni di backup devono essere in grado di eseguire il backup e il ripristino dei punti di giunzione.

Questi punti di giunzione possono essere identificati come segue:

-   Hanno l'attributo file \_ \_ reparse \_ Point, l' \_ attributo file \_ Hidden e \_ \_ gli attributi file System attribute set.
-   Dispongono anche di elenchi di controllo di accesso (ACL) impostati per negare l'accesso in lettura a tutti.

Le applicazioni che chiamano un percorso specifico possono attraversare questi punti di giunzione se dispongono delle autorizzazioni necessarie. Tuttavia, i tentativi di enumerare il contenuto dei punti di giunzione provocheranno errori. È importante che le applicazioni di backup non attraversino questi punti di giunzione o tentino di eseguire il backup dei dati in essi contenuti, per due motivi:

-   In questo modo, l'applicazione di backup può eseguire il backup degli stessi dati più di una volta.
-   Può anche causare cicli (riferimenti circolari).

## <a name="per-user-junctions-and-system-junctions"></a>Giunzioni di Per-User e giunzioni di sistema

I punti di giunzione utilizzati per fornire la virtualizzazione di file e registro di sistema in Windows Vista e Windows Server 2008 possono essere divisi in due classi: giunzioni per utente e giunzioni di sistema.

Le giunzioni per utente vengono create all'interno del profilo di ogni singolo utente per garantire la compatibilità con le versioni precedenti per le applicazioni utente. Il punto di giunzione in C: \\ Users \\ *nomeutente* i \\ documenti che puntano a c: \\ utenti \\ *nomeutente* \\ documenti è un esempio di giunzione per utente. Le giunzioni per utente vengono create dal servizio profili quando viene creato il profilo dell'utente.

Le altre giunzioni sono giunzioni di sistema che non risiedono nella \\ directory *username* degli utenti. Esempi di giunzioni di sistema includono:

-   Documenti e impostazioni
-   Giunzioni nei profili utente tutti gli utenti, pubblici e predefiniti

Le giunzioni di sistema vengono create da userenv.dll quando viene richiamato da Windows Welcome (noto anche come Machine out-of-Box-Experience o mOOBE).

> [!Note]  
> Se l'utente modifica la lingua di sistema in una lingua diversa dall'inglese, i punti di giunzione per utente e sistema verranno creati con nomi localizzati.

 

 

 



