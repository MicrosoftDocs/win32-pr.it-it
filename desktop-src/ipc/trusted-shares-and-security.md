---
description: DDE di rete usa condivisioni attendibili e descrittori di sicurezza per controllare l'accesso alle condivisioni.
ms.assetid: a22d9fc6-a0c9-442f-b278-1271cfbc636b
title: Condivisioni attendibili e sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 899be51745b2b27c22212c3ceeaceea016fa8d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305703"
---
# <a name="trusted-shares-and-security"></a>Condivisioni attendibili e sicurezza

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

DDE di rete usa condivisioni attendibili e descrittori di sicurezza per controllare l'accesso alle condivisioni.

## <a name="trusted-shares"></a>Condivisioni attendibili

Quando un utente client si connette a una condivisione DDE da un computer remoto, il DDE di rete accetta la richiesta solo se le istruzioni seguenti sono vere:

-   L'utente che ha creato la condivisione ha concesso lo stato attendibile alla condivisione chiamando [**NDdeSetTrustedShare**](nddesettrustedshare.md). Solo l'autore della condivisione può concedere lo stato attendibile alla condivisione. Non anche un amministratore può concedere lo stato attendibile a una condivisione DDE creata da un altro utente.
-   L'utente che ha creato la condivisione è attualmente connesso al computer server.

Il processo di concessione dello stato attendibile a una condivisione aggiunge la condivisione all'elenco delle condivisioni attendibili dell'utente connesso in DSDM. Viene creata una relazione di trust tra il server e i relativi client. Una volta che una condivisione DDE ha stato attendibile, i client possono connettersi a tale condivisione a condizione che l'utente che ha creato la condivisione sia connesso. Quando il client si connette alla condivisione da un computer remoto, il DDE di rete accetta la richiesta solo se la condivisione è elencata nell'elenco delle condivisioni attendibili dell'utente connesso nella DSDM.

## <a name="security"></a>Sicurezza

DDE di rete esegue un controllo di sicurezza aggiuntivo quando il client richiede dati o un collegamento. Verifica che il server abbia concesso all'utente remoto l'autorizzazione necessaria per l'operazione. Il server controlla l'accesso alla condivisione tramite il parametro *PSD* della funzione [**NDDEShareAdd**](nddeshareadd.md) . Questo parametro specifica il descrittore di sicurezza. Se questo parametro è **null**, la funzione crea un descrittore di sicurezza predefinito che concede l'accesso completo al creatore della condivisione e concede l'autorizzazione di lettura e collegamento a tutti gli altri utenti. Per concedere o negare autorizzazioni aggiuntive a singoli utenti o gruppi di utenti, creare e utilizzare un descrittore di sicurezza. Per ulteriori informazioni sui descrittori di sicurezza, vedere [**controllo di accesso**](/windows/desktop/SecAuthZ/access-control).

Per ottenere il descrittore di sicurezza per una condivisione DDE esistente, chiamare la funzione [**NDdeGetShareSecurity**](nddegetsharesecurity.md) . È possibile modificare le informazioni e quindi aggiornare il descrittore di sicurezza per la condivisione usando la funzione [**NDdeSetShareSecurity**](nddesetsharesecurity.md) .

 

 
