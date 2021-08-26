---
description: DDE di rete usa condivisioni attendibili e descrittori di sicurezza per controllare l'accesso alle condivisioni.
ms.assetid: a22d9fc6-a0c9-442f-b278-1271cfbc636b
title: Condivisioni attendibili e sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bed3b520597f6cabe95929d2ee5bf9c29af6bb6c524d2aa136f4c86392cbb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014681"
---
# <a name="trusted-shares-and-security"></a>Condivisioni attendibili e sicurezza

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

DDE di rete usa condivisioni attendibili e descrittori di sicurezza per controllare l'accesso alle condivisioni.

## <a name="trusted-shares"></a>Condivisioni attendibili

Quando un utente client si connette a una condivisione DDE da un computer remoto, DDE di rete accetta la richiesta solo se le istruzioni seguenti sono vere:

-   L'utente che ha creato la condivisione ha concesso lo stato attendibile alla condivisione chiamando [**NDdeSetTrustedShare**](nddesettrustedshare.md). Solo l'autore della condivisione può concedere lo stato attendibile alla condivisione. Neanche un amministratore può concedere lo stato attendibile a una condivisione DDE creata da un altro utente.
-   L'utente che ha creato la condivisione è attualmente connesso al computer server.

Il processo di concessione dello stato attendibile a una condivisione aggiunge la condivisione all'elenco di condivisioni attendibili dell'utente connesso in DSDM. Verrà creata una relazione di trust tra il server e i relativi client. Una volta che una condivisione DDE ha lo stato attendibile, i client possono connettersi a essa purché l'utente che ha creato la condivisione sia connesso. Quando il client si connette alla condivisione da un computer remoto, DDE di rete accetta la richiesta solo se la condivisione è elencata nell'elenco condivisioni attendibili dell'utente connesso in DSDM.

## <a name="security"></a>Sicurezza

DDE di rete esegue un controllo di sicurezza aggiuntivo quando il client richiede dati o un collegamento. Verifica che il server abbia concesso all'utente remoto l'autorizzazione necessaria per l'operazione. Il server controlla l'accesso alla condivisione tramite il *parametro pSD* della [**funzione NDdeShareAdd.**](nddeshareadd.md) Questo parametro specifica il descrittore di sicurezza. Se questo parametro è **NULL,** la funzione crea un descrittore di sicurezza predefinito che concede l'accesso completo all'autore della condivisione e concede l'autorizzazione di lettura e collegamento a tutti gli altri utenti. Per concedere o negare autorizzazioni aggiuntive a singoli utenti o gruppi di utenti, creare e usare un descrittore di sicurezza. Per altre informazioni sui descrittori di sicurezza, vedere [**Controllo di accesso**](/windows/desktop/SecAuthZ/access-control).

Per ottenere il descrittore di sicurezza per una condivisione DDE esistente, chiamare la [**funzione NDdeGetShareSecurity.**](nddegetsharesecurity.md) È possibile modificare le informazioni e quindi aggiornare il descrittore di sicurezza per la condivisione usando la [**funzione NDdeSetShareSecurity.**](nddesetsharesecurity.md)

 

 
