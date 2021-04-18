---
description: Cenni preliminari sull'API dei controlli padre
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Cenni preliminari sull'API dei controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0aa88592f2262b89f98cfd5baaac5ad2f35f959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318402"
---
# <a name="parental-controls-api-overview"></a>Cenni preliminari sull'API dei controlli padre

Le API usate per i controlli padre espongono i criteri e le impostazioni di restrizione predefinite e la funzionalità di registrazione.

## <a name="settings"></a>Impostazioni

Sono disponibili due API pubbliche:

-   Un'API di conformità minima basata su COM (denominata API di conformità) principalmente per le applicazioni per determinare se la registrazione deve essere attivata. Vengono inoltre forniti metodi semplici per:
    -   Recupero dello stato delle restrizioni per le restrizioni Web, i limiti di tempo, le restrizioni dei giochi e le restrizioni dell'applicazione.
    -   Recupero dell'ID del filtro contenuto Web attivo.
    -   Determinare se gli elementi dell'interfaccia utente del fornitore devono essere visualizzati, in modo coerente con il nascondiglio in box quando vengono aggiunti a un dominio.
    -   Recupero dell'Ultima modifica di un'impostazione per un utente.
    -   Il recupero del download dei file basati sul browser o di tipo browser deve essere bloccato per un utente e la possibilità di richiedere un URL da consentire in modo specifico al filtro contenuto Web per tale utente.
    -   Determinare se un determinato gioco è bloccato per un utente.
-   Accesso all'API Strumentazione gestione Windows (WMI) a uno spazio dei nomi dei controlli padre per l'accesso in lettura e scrittura completo a tutte le impostazioni esposte. I controlli padre distribuiscono un provider WMI per gestire le autorizzazioni di lettura/scrittura per l'archivio delle impostazioni sottostanti con l'imposizione corretta dei privilegi per gli amministratori e gli utenti controllati.

Agli ISV viene richiesto di utilizzare l'API di conformità e l'API WMI, se necessario, per controllare le restrizioni appropriate per la sicurezza figlio in base alle funzionalità dell'applicazione o della soluzione.

## <a name="logging"></a>Registrazione

-   Le API di pubblicazione e utilizzo di eventi standard di Windows vengono utilizzate per il monitoraggio delle attività dei controlli padre. Il sistema di segnalazione degli eventi e di traccia di Windows Vista ha migliorato le prestazioni rispetto alla funzionalità ETW (Previous Event Tracing for Windows). I controlli padre definiscono un canale univoco per i dati in ETW.
-   Agli ISV viene richiesto di utilizzare l'API di pubblicazione degli eventi per registrare l'attività utente come specificato nella sezione Utilizzo delle API dei controlli padre.

 

 



