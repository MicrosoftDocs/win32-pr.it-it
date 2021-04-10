---
title: Richiamo delle DLL di estensione
description: Chiama queste funzioni per ogni pacchetto di autenticazione o Accounting valido ricevuto dal server di accesso alla rete (NAS).
ms.assetid: 6d738ad7-cce5-4835-97d6-c57173c79a16
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc96fab078a982f23f5f5dd86d51dbed46d5541
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963312"
---
# <a name="invoking-the-extension-dlls"></a>Richiamo delle DLL di estensione

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

Le DLL di estensione NPS devono esportare almeno una delle funzioni di callback seguenti: [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process), [*RadiusExtensionProcessEx*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)o [*RadiusExtensionProcess2*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2). NPS chiama queste funzioni per ogni pacchetto di autenticazione o Accounting valido che riceve dal server di accesso alla rete (NAS). NPS chiama queste funzioni in ognuna delle DLL elencate sotto la [chiave del registro di sistema dei parametri](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)del server dei criteri di server. Le dll vengono chiamate nell'ordine in cui sono elencate.

Se una DLL di estensione server dei criteri di rete Esporta più di una delle funzioni sopra elencate, il server dei criteri di rete richiama solo uno di essi: la funzione più recente supportata dal sistema operativo.

> [!Note]  
> IAS originariamente supportava solo [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process). IAS supporta anche [*RadiusExtensionProcessEx*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex). IAS (e versioni successive NPS) supporta anche [*RadiusExtensionProcess2*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2).

 

Le DLL di estensione NPS possono anche esportare le funzioni [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) e [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) . Se sono presenti, NPS chiama queste funzioni quando il servizio viene avviato e arrestato rispettivamente.

## <a name="radiusextensionprocess-callback-function"></a>Funzione di callback RadiusExtensionProcess

In una DLL di estensione di autenticazione, [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process) riceve tutti gli attributi ricevuti da NPS nella richiesta di autenticazione o di accounting. Usando questi attributi, la funzione può eseguire convalide aggiuntive, verificare le autorizzazioni dell'utente o inviare record di contabilità a un server di stato centrale.

In una DLL di estensione di autorizzazione, **RadiusExtensionProcess** riceve tutti gli attributi generati dal servizio di autorizzazione NPS. Questi sono gli attributi restituiti nel pacchetto di Access-Accept.

Dopo la chiamata a **RadiusExtensionProcess**, l'azione eseguita da NPS dipende dal valore restituito di **RadiusExtensionProcess** e dal valore restituito nel parametro *pfAction* . Questi valori sono elencati nella seguente tabella.



| *pfAction* | DLL dell'estensione di autenticazione                                                                                                                                            | DLL estensione di autorizzazione                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accetta     | Ignora eventuali altre DLL di estensione di autenticazione e ignora anche il meccanismo di autenticazione server dei criteri di server.                                                                  | Accept non consentito.                                                                                                                                         |
| Rifiuto     | Ignora eventuali altre DLL di estensione di autenticazione e ignora anche il meccanismo di autenticazione server dei criteri di server. Viene inviato Access-Reject pacchetto.                                    | Ignora eventuali altre DLL di estensione di autorizzazione.                                                                                                          |
| Continua   | Il pacchetto viene inviato alla DLL dell'estensione di autenticazione successiva o al meccanismo di autenticazione NPS se nel registro di sistema non sono elencate altre DLL di estensione per l'autenticazione. | Il pacchetto viene inviato alla successiva DLL dell'estensione di autorizzazione o al log di contabilità NPS se nel registro di sistema non sono elencate altre DLL di estensione di autorizzazione. |



 

Per tutte le DLL di estensione, se **RadiusExtensionProcess** restituisce un errore, il pacchetto viene ignorato. I pacchetti eliminati a causa di un errore non vengono elaborati dal registro contabilità server dei criteri di server.

Se si verifica un errore, NPS Invia un evento di errore generico al registro eventi. È consigliabile che la DLL di estensione fornisca la registrazione degli errori aggiuntiva.

Per ulteriori informazioni e un diagramma che rappresenta il processo precedente, vedere [informazioni sulle estensioni NPS](/windows/desktop/Nps/ias-about-internet-authentication-service).

**RadiusExtensionProcess** deve restituire un errore se non è in grado di verificare l'accettazione o il rifiuto del pacchetto. Questa situazione può verificarsi in caso di problemi di rete che impedisce a **RadiusExtensionProcess** di comunicare con il database di autenticazione utente.

Quando si elabora un pacchetto di contabilità, il parametro *pfAction* è **null**, pertanto non è possibile impostare *pfAction* . La restituzione di un errore dalla funzione **RadiusExtensionProcess** durante l'elaborazione di una richiesta di contabilità comporta l'eliminazione della richiesta da parte di NPS.

> [!Note]  
> Dopo aver ricevuto un'accettazione, NPS non chiama **RadiusExtensionProcess** nelle dll rimanenti della sequenza. Poiché alcune funzioni di autenticazione possono implementare anche le autorizzazioni, l'omissione di tali funzioni può causare l'omissione delle autorizzazioni. Se un'istanza di [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) restituisce Accept, è importante non creare presupposti sulle autorizzazioni recuperate.

 

Se viene restituito continue o Accept, il profilo corrispondente all'area di autenticazione viene inviato nuovamente nel pacchetto di Access-Accept.

Le DLL dell'estensione di autenticazione devono essere progettate per coesistere con i provider di autenticazione del server dei criteri di server predefiniti e con altre DLL di estensione. Se un'estensione è applicabile solo a un determinato database utente (ad esempio Windows Active Directory), deve verificare l'attributo [**ratProvider**](/windows/desktop/api/authif/ne-authif-radius_authentication_provider) passato *nel parametro di gestione dei dati* , prima di elaborare la richiesta. L'attributo ratProvider può essere uno di un elenco di attributi a cui punta il *parametro.*

Le DLL di estensione non devono rifiutare richieste perché mancano gli attributi obbligatori. Se, ad esempio, un'estensione di autenticazione richiede l'attributo User-Password, ratUserPassword e l'attributo non è presente, l'estensione deve restituire un'azione di raContinue per fornire ad altre estensioni e provider la possibilità di elaborare la richiesta.

NPS chiama la funzione [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) dopo la decisione di usare un determinato database di autenticazione, ma prima dell'autenticazione dell'utente. Pertanto, le informazioni sul database di autenticazione da utilizzare sono disponibili per la funzione, in modo che la funzione possa verificare le autorizzazioni dell'utente nel database di autenticazione appropriato. NPS supporta diversi database di autenticazione, tra cui Windows Active Directory.

## <a name="radiusextensionprocessex-callback-function"></a>Funzione di callback RadiusExtensionProcessEx

Le DLL di estensione NPS possono esportare [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) anziché o in aggiunta a [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process). Questa funzione consente alla DLL di accodare attributi di autorizzazione aggiuntivi alla risposta di autenticazione.

Le stesse informazioni descritte nella sezione *funzione di callback RadiusExtensionProcess* sono valide per la funzione [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) .

[**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) non è in grado di modificare o rimuovere gli attributi presenti. Se si verifica uno scenario in cui la DLL deve modificare o rimuovere gli attributi, l'unica opzione consiste nell'utilizzare l'interfaccia utente del server dei criteri di server per assicurarsi che gli attributi non siano presenti. Per impostazione predefinita, non sono presenti attributi di autorizzazione. Tutti i presenti presenti devono essere stati aggiunti tramite l'interfaccia utente.

Se vengono configurate più DLL di autorizzazione e alcune di queste DLL implementano [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), la funzione **RadiusExtensionProcess/ex** in una determinata dll non riceve gli attributi dalle DLL di autorizzazione denominate in precedenza. Riceve solo gli attributi generati dal servizio di autorizzazione NPS.

## <a name="radiusextensionprocess2-callback-function"></a>Funzione di callback RadiusExtensionProcess2

Le DLL di estensione NPS possono anche esportare [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) anziché o in aggiunta a [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) e **RadiusExtensionProcessEx**. Questa funzione consente alla DLL di aggiungere, modificare e rimuovere attributi da e verso la richiesta o la risposta di autenticazione.

Le stesse informazioni descritte nella sezione *funzione di callback RadiusExtensionProcessEx* sono valide per la funzione [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) , con le eccezioni seguenti:

-   In una DLL di autorizzazione, **RadiusExtensionProcess2** riceve sia gli attributi generati dal servizio di autorizzazione server dei criteri di server che gli attributi generati da precedentemente chiamate dll di autorizzazione.
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) non dispone di un parametro *pfAction* . **RadiusExtensionProcess2** imposta la disposizione finale della richiesta usando la funzione [**SetResponseType**](/previous-versions/ms688462(v=vs.85)) fornita nella struttura del [**\_ blocco di \_ controllo \_ dell'estensione RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .
-   NPS chiama sempre la funzione [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) in tutte le dll rimanenti, indipendentemente dal fatto che le funzioni nelle DLL precedenti restituissero Accept.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione delle DLL di estensione](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Attributi di identificazione utente](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 