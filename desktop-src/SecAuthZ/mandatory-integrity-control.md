---
description: Fornisce un meccanismo per controllare l'accesso agli oggetti a protezione diretta.
ms.assetid: 5923cb4c-f663-40d2-989a-07d71ac475db
title: Controllo di integrità delle credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1a39cfc1d1ab819181e37c17328d6015a884f9ae1cce546643480351341b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781494"
---
# <a name="mandatory-integrity-control"></a>Controllo di integrità delle credenziali

Controllo di integrità delle credenziali (MIC) fornisce un meccanismo per controllare l'accesso agli oggetti a protezione diretta. Questo meccanismo si aggiunge al controllo di accesso discrezionale e valuta [](/windows/desktop/SecGloss/d-gly) l'accesso prima che i controlli di accesso rispetto all'elenco di controllo di accesso discrezionale (DACL) di un oggetto siano valutati.

MIC usa i livelli di integrità e i criteri obbligatori per valutare l'accesso. [*Alle entità di sicurezza*](/windows/desktop/SecGloss/s-gly) e agli oggetti a protezione diretta vengono assegnati livelli di integrità che determinano i livelli di protezione o di accesso. Ad esempio, un'entità con un livello di integrità basso non può scrivere in un oggetto con un livello di integrità medio, anche se l'elenco DACL di tale oggetto consente l'accesso in scrittura all'entità.

Windows definisce quattro livelli di integrità: basso, medio, alto e sistema. Gli utenti standard ricevono utenti medi con privilegi elevati. I processi avviati e gli oggetti creati ricevono il livello di integrità (medio o alto) o basso se il livello del file eseguibile è basso; i servizi di sistema ricevono l'integrità del sistema. Gli oggetti che non dispongono di un'etichetta di integrità vengono considerati medi dal sistema operativo. ciò impedisce al codice a bassa integrità di modificare gli oggetti senza etichetta. Inoltre, Windows che i processi in esecuzione con un livello di integrità basso non siano in grado di ottenere l'accesso a un processo associato a un contenitore di app.

## <a name="integrity-labels"></a>Etichette di integrità

Le etichette di integrità specificano i livelli di integrità degli oggetti a protezione diretta e delle entità di sicurezza. Le etichette di integrità sono rappresentate [*da SID di integrità.*](/windows/desktop/SecGloss/i-gly) Il SID di integrità per un oggetto a protezione diretta viene archiviato nel relativo elenco [*di*](/windows/desktop/SecGloss/s-gly) controllo di accesso di sistema (SACL). L'elenco sacl contiene una voce di controllo di accesso [**\_ \_ \_ (ACE) SYSTEM MANDATORY LABEL**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) che a sua volta contiene il SID di integrità. [](/windows/desktop/SecGloss/a-gly) Qualsiasi oggetto senza UND di integrità viene considerato come se avesse un'integrità media.

Il SID di integrità per un'entità di sicurezza viene archiviato nel relativo token di accesso. Un token di accesso può contenere uno o più SID di integrità.

Per informazioni dettagliate sui SID di integrità definiti, vedere [SID noti](well-known-sids.md).

## <a name="process-creation"></a>Creazione del processo

Quando un utente tenta di avviare un file eseguibile, il nuovo processo viene creato con il livello minimo di integrità utente e il livello di integrità del file. Ciò significa che il nuovo processo non verrà mai eseguito con un'integrità superiore rispetto al file eseguibile. Se l'utente amministratore esegue un programma a bassa integrità, il token per il nuovo processo funziona con il livello di integrità basso. Ciò consente di proteggere un utente che avvia codice non attendibile da azioni dannose eseguite da tale codice. I dati utente, che si trova al livello di integrità utente tipico, sono protetti da scrittura rispetto a questo nuovo processo.

## <a name="mandatory-policy"></a>Criteri obbligatori

L'ACE SYSTEM [**\_ MANDATORY \_ LABEL \_**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) nel SACL di un oggetto a protezione diretta contiene una maschera di accesso che specifica l'accesso concesso alle entità con livelli di integrità inferiori a quelli dell'oggetto. I valori definiti per questa maschera di accesso sono **SYSTEM MANDATORY LABEL NO WRITE \_ \_ \_ \_ \_ UP,** **SYSTEM MANDATORY LABEL NO READ \_ \_ \_ \_ \_ UP** e **SYSTEM MANDATORY LABEL NO EXECUTE \_ \_ \_ \_ \_ UP**. Per impostazione predefinita, il sistema crea ogni oggetto con una maschera di accesso impostata su **SYSTEM MANDATORY LABEL NO WRITE \_ \_ \_ \_ \_ UP**.

Ogni token di accesso specifica anche un [](/windows/desktop/SecGloss/l-gly) criterio obbligatorio impostato dall'autorità di sicurezza locale (LSA) al momento della creazione del token. Questo criterio viene specificato da una [**struttura TOKEN \_ MANDATORY \_ POLICY**](/windows/desktop/api/Winnt/ns-winnt-token_mandatory_policy) associata al token. È possibile eseguire query su questa struttura chiamando la [**funzione GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con il valore del parametro *TokenInformationClass* impostato su **TokenMandatoryPolicy**.

 

 
