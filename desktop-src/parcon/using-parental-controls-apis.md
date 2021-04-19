---
description: Uso delle API dei controlli padre
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: Uso delle API dei controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311579"
---
# <a name="using-parental-controls-apis"></a>Uso delle API dei controlli padre

## <a name="api-selection"></a>Selezione API

Come indicato nella sezione Panoramica, lo sviluppo prevede l'uso di un massimo di tre API:

-   Accesso alle impostazioni di base: l'API COM per la conformità minima dei controlli padre (API di conformità) definita in Wpcapi. h per un accesso semplice a un subset chiave dello stato dei controlli padre.
-   Accesso in lettura/scrittura completo delle impostazioni: l'uso di un piccolo subset dell'API COM WMI per l'accesso completo è necessario solo se l'ISV deve modificare le impostazioni. L'aggiunta di un collegamento di estendibilità dell'interfaccia utente, la sostituzione del filtro contenuto Web o le aggiunte all'applicazione HTTP a livello di computer o agli elenchi di esenzione del filtro URL sono i motivi principali per usare l'API. Poiché l'utilizzo dello spazio dei nomi dei controlli padre WMI fornisce accesso non elaborato all'archivio delle impostazioni sottostante, gli ISV devono procedere con cautela nell'interpretazione dello stato dalle singole impostazioni che possono in realtà avere dipendenze di controllo da altre impostazioni. È quindi consigliabile usare l'API di conformità per leggere lo stato di tutti i valori esposti da tale API.
-   Registrazione: l'API di traccia eventi di Windows Vista e il sistema di creazione di report (noto anche come ETW) per la pubblicazione di eventi di attività nei log dei controlli padre, in combinazione con descrittori di evento ed enumerazioni di matrici definite in WpcEvent. h.

Tutte le API possono essere richiamate come utente standard. Per la registrazione, qualsiasi utente può eseguire eventi di log di origine. La chiamata a per recuperare o modificare le impostazioni per un altro utente avrà esito negativo se il chiamante non dispone dei privilegi di amministratore. In altre parole, un utente standard può accedere solo alle proprie impostazioni e solo per la lettura.

Le impostazioni e l'utilizzo dell'API di registrazione sono descritte in dettaglio nelle sezioni seguenti:

-   [Uso delle API delle impostazioni dei controlli padre](using-parental-controls-settings-apis.md)
-   [Uso delle API di registrazione per i controlli padre](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a>Ambiente di sviluppo

Per lo sviluppo di controlli padre è necessario l'accesso a tre file di intestazione: WPC. h, WpcApi. h e WpcEvent. h. WPC. h è un agente di raccolta che include le impostazioni API di conformità pubbliche e intestazioni di evento, quindi è sufficiente includere WPC. h nel codice dell'applicazione.

Le autorizzazioni di lettura/scrittura per l'API WMI sono specificate dal file Wpcsprov. mof. Questo file viene installato nella sottodirectory WBEM sotto la directory system32 di Windows.

Il Software Development Kit (SDK) di Microsoft Windows contiene codice di esempio per rafforzare il codice di esempio illustrato di seguito e fornire semplici strumenti basati su riga di comando per l'esplorazione API o il test di integrazione.

 

 



