---
description: Cenni preliminari sull'API Controllo genitori
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Cenni preliminari sull'API Controllo genitori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2dc1995db834aa206dea1a4f657565ac3e38b35766ca6a83ac495c4f1734af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712581"
---
# <a name="parental-controls-api-overview"></a>Cenni preliminari sull'API Controllo genitori

Le API usate per il controllo genitori espongono le impostazioni dei criteri e delle restrizioni predefinite e la funzionalità di registrazione.

## <a name="settings"></a>Impostazioni

Sono disponibili due API pubbliche:

-   Un'API leggera di conformità minima basata su COM ,denominata API di conformità, che consente principalmente alle applicazioni di determinare se la registrazione deve essere attivata. Vengono inoltre forniti metodi semplici per:
    -   Recupero dello stato delle restrizioni per restrizioni Web, limiti di tempo, restrizioni dei giochi e restrizioni dell'applicazione.
    -   Recupero dell'ID del filtro di contenuto Web attivo.
    -   Determinare se gli elementi dell'interfaccia utente del fornitore devono essere visualizzati, in modo coerente con la casella nascosta quando viene aggiunto a un dominio.
    -   Recupero dell'ultima modifica di un'impostazione per un utente.
    -   Recupero del fatto che i download di file basati su browser o simili a browser devono essere bloccati per un utente e la possibilità di richiedere che un URL sia consentito in modo specifico dal filtro contenuto Web per tale utente.
    -   Determinare se un determinato gioco è bloccato per un utente.
-   Windows Accesso dell'API Strumentazione gestione (WMI) a uno spazio dei nomi controllo genitori per l'accesso completo in scrittura e in lettura a tutte le impostazioni esposte. Controllo genitori distribuisce un provider WMI per gestire le autorizzazioni di lettura/scrittura nell'archivio delle impostazioni sottostante con l'applicazione corretta dei privilegi per gli amministratori e gli utenti controllati.

Agli ISV viene richiesto di usare l'API di conformità e l'API WMI, se necessario, per controllare le restrizioni in modo appropriato per la sicurezza dei figli in base alla funzionalità dell'applicazione o della soluzione.

## <a name="logging"></a>Registrazione

-   Windows per il monitoraggio delle attività di Controllo genitori vengono usate le API standard per la pubblicazione e l'utilizzo di eventi. Il Windows di creazione di report e traccia eventi di Vista ha migliorato le prestazioni rispetto alle precedenti funzionalità ETW (Event Tracing for Windows). Controllo genitori definisce un canale univoco per i dati in ETW.
-   Agli ISV viene richiesto di usare l'API di pubblicazione degli eventi per registrare l'attività utente come specificato nella sezione Using Parent Controls APIs (Uso delle API di controllo genitori).

 

 



