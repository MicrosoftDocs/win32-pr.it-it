---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: af511aed-88f5-4b12-ad44-317925297f70
title: I (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d3e727128c2494f313bdffc879b5c5e47a28ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057872"
---
# <a name="i-security-glossary"></a>I (Glossario sulla sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) i J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**
</dt> <dd>

Servizi software che supportano la creazione, la configurazione e la gestione del sito Web, oltre ad altre funzioni Internet. Internet Information Services includono NNTP (Network News Transfer Protocol), File Transfer Protocol (FTP) e Simple Mail Transfer Protocol (SMTP). IIS incorpora varie funzioni per la sicurezza, consente le applicazioni CGI e fornisce server gopher e FTP.

</dd> <dt>

<span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**rappresentazione**
</dt> <dd>

Meccanismo che consente l'esecuzione di un processo server utilizzando le credenziali di sicurezza del client o di un altro utente utilizzando le credenziali. Quando il server rappresenta il client, tutte le operazioni eseguite dal server vengono eseguite utilizzando le credenziali del client (rappresentazione utente). La rappresentazione non consente al server di accedere alle risorse remote per conto del client. Questa operazione richiede la delega.

</dd> <dt>

<span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**token di rappresentazione**
</dt> <dd>

Un token di accesso creato per acquisire le informazioni di sicurezza di un processo client, consentendo a un server di "rappresentare" il processo client in operazioni di sicurezza.

Vedere anche [*token di accesso*](a-gly.md) e [*token primario*](p-gly.md).

</dd> <dt>

<span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**vettore di inizializzazione**
</dt> <dd>

(IV) sequenza di byte casuali aggiunti all'inizio del testo non crittografato prima della crittografia tramite una crittografia a blocchi. Se si aggiunge il vettore di inizializzazione all'inizio del testo non crittografato, si evita la possibilità di bloccare il testo crittografato iniziale per due messaggi. Se, ad esempio, i messaggi iniziano sempre con un'intestazione comune, ovvero una riga intestata o "da", il testo crittografato iniziale sarà sempre lo stesso, supponendo che sia stato utilizzato lo stesso algoritmo crittografico e la stessa chiave simmetrica. L'aggiunta di un vettore di inizializzazione casuale Elimina questa situazione.

</dd> <dt>

<span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**dati interni**
</dt> <dd>

Qualsiasi dato codificato utilizzato come messaggio per un altro messaggio codificato. Un messaggio in busta e il relativo valore hash, ad esempio, possono essere i dati interni di un secondo messaggio.

</dd> <dt>

<span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**contenuto interno**
</dt> <dd>

Dati migliorati, ad esempio con una firma digitale. Questo termine viene usato principalmente quando si discutono i dati avanzati in un \# messaggio PKCS 7.

</dd> <dt>

<span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**integrità**
</dt> <dd>

Completezza e accuratezza di un messaggio dopo l'invio o l'archiviazione.

</dd> <dt>

<span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**SID integrità**
</dt> <dd>

Un [*ID di sicurezza*](s-gly.md) (SID) che rappresenta un livello di integrità. Un SID di integrità nell' [*elenco di controllo di accesso di sistema*](s-gly.md) (SACL) del descrittore di sicurezza di un oggetto specifica il livello di integrità dell'oggetto. I SID di integrità in un token di accesso specificano il livello di integrità del token.

</dd> <dt>

<span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**LIVELLO IRQL**
</dt> <dd>

Un livello di richiesta di interrupt (livello IRQL) definisce la priorità hardware a cui un processore opera in un determinato momento. Nel Windows Driver Model, un thread in esecuzione a un livello IRQL basso può essere interrotto per eseguire il codice in un livello IRQL superiore.

</dd> <dt>

<span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**IV**
</dt> <dd>

Vedere *vettore di inizializzazione*.

</dd> </dl>

 

 



