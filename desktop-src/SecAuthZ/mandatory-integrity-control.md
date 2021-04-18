---
description: Fornisce un meccanismo per controllare l'accesso agli oggetti a protezione diretta.
ms.assetid: 5923cb4c-f663-40d2-989a-07d71ac475db
title: Controllo di integrità delle credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c184ba01da0a55309fcb27ace9b0fe156edd6425
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334035"
---
# <a name="mandatory-integrity-control"></a>Controllo di integrità delle credenziali

Controllo di integrità delle credenziali (MIC) fornisce un meccanismo per controllare l'accesso agli oggetti a protezione diretta. Questo meccanismo è in aggiunta al controllo di accesso discrezionale e valuta l'accesso prima che vengano valutati i controlli di accesso per l' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) di un oggetto.

MIC usa i livelli di integrità e i criteri obbligatori per valutare l'accesso. Alle [*entità di sicurezza*](/windows/desktop/SecGloss/s-gly) e agli oggetti a protezione diretta vengono assegnati livelli di integrità che ne determinano i livelli di protezione o di accesso. Ad esempio, un'entità con un livello di integrità basso non può scrivere in un oggetto con un livello di integrità medio, anche se il DACL dell'oggetto consente l'accesso in scrittura al server principale.

Windows definisce quattro livelli di integrità: bassa, media, alta e sistema. Gli utenti standard ricevono un elevato livello di supporto per gli utenti con privilegi elevati. I processi avviati e gli oggetti creati ricevono il livello di integrità (medio o alto) o basso se il livello del file eseguibile è basso. i servizi di sistema ricevono l'integrità del sistema. Gli oggetti che non dispongono di un'etichetta di integrità vengono considerati medi dal sistema operativo; in questo modo si impedisce che il codice a bassa integrità modifichi gli oggetti senza etichetta. Windows garantisce inoltre che i processi in esecuzione con un livello di integrità basso non possano ottenere l'accesso a un processo associato a un contenitore di app.

## <a name="integrity-labels"></a>Etichette di integrità

Le etichette di integrità specificano i livelli di integrità degli oggetti a protezione diretta e delle entità di sicurezza. Le etichette di integrità sono rappresentate da [*SID di integrità*](/windows/desktop/SecGloss/i-gly). Il SID di integrità per un oggetto a protezione diretta è archiviato nel relativo [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL). L'elenco di [*controllo di accesso*](/windows/desktop/SecGloss/a-gly) contiene un' [**\_ \_ etichetta obbligatoria \_ di sistema**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) ACE che a sua volta contiene il SID di integrità. Qualsiasi oggetto senza un SID di integrità viene considerato come se avesse una media integrità.

Il SID di integrità per un'entità di sicurezza viene archiviato nel relativo token di accesso. Un token di accesso può contenere uno o più SID di integrità.

Per informazioni dettagliate sui SID di integrità definiti, vedere [SID noti](well-known-sids.md).

## <a name="process-creation"></a>Creazione di processi

Quando un utente tenta di avviare un file eseguibile, il nuovo processo viene creato con il livello di integrità utente minimo e il livello di integrità del file. Ciò significa che il nuovo processo non verrà mai eseguito con un livello di integrità superiore rispetto a quello del file eseguibile. Se l'utente amministratore esegue un programma con integrità bassa, il token per il nuovo processo funziona con il livello di integrità basso. Ciò consente di proteggere un utente che avvia codice non attendibile da azioni dannose eseguite da tale codice. I dati utente, che si trova al livello di integrità utente tipico, sono protetti da scrittura per questo nuovo processo.

## <a name="mandatory-policy"></a>Criterio obbligatorio

La [**voce \_ \_ \_ ACE ACE obbligatoria del sistema**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) nell'elenco SACL di un oggetto a protezione diretta contiene una maschera di accesso che specifica l'accesso a cui vengono concesse le entità con livelli di integrità inferiori a quelli dell'oggetto. I valori definiti per questa maschera di accesso **sono \_ etichetta obbligatoria del sistema \_ \_ Nessuna \_ \_** operazione di scrittura, **\_ etichetta obbligatoria del sistema \_ \_ Nessuna \_ lettura \_** e **\_ etichetta obbligatoria del sistema \_ \_ Nessuna \_ esecuzione \_**. Per impostazione predefinita, il sistema crea ogni oggetto con una maschera di accesso dell' **etichetta del sistema \_ obbligatoria \_ \_ senza \_ scrittura \_**.

Ogni token di accesso specifica anche un criterio obbligatorio impostato dall'autorità di [*sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) al momento della creazione del token. Questo criterio è specificato da una struttura di [**\_ \_ criteri obbligatoria del token**](/windows/desktop/api/Winnt/ns-winnt-token_mandatory_policy) associata al token. È possibile eseguire una query su questa struttura chiamando la funzione [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con il valore del parametro *TokenInformationClass* impostato su **TokenMandatoryPolicy**.

 

 
