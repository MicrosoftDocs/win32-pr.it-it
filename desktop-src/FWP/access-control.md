---
title: Controllo di accesso (Windows Filtering Platform)
description: In Windows Filtering Platform (WFP), il servizio Base Filtering Engine (BFE) implementa il modello di controllo di accesso Windows standard basato su token di accesso e descrittori di sicurezza.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad8d1cc292358b156a8853a8a141426fda638d64474d1413747e2ebdb59d7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901097"
---
# <a name="access-control-windows-filtering-platform"></a>Controllo di accesso (Windows Filtering Platform)

In Windows Filtering Platform (WFP), il servizio Base Filtering Engine (BFE) implementa il modello [di](/windows/desktop/SecAuthZ/access-control-model) controllo di accesso Windows standard basato su token di accesso e descrittori di sicurezza.

## <a name="access-control-model"></a>Modello di controllo di accesso

I descrittori di sicurezza possono essere specificati quando si aggiungono nuovi oggetti WFP, ad esempio filtri e livelli secondari. I descrittori di sicurezza vengono gestiti usando le funzioni di gestione di WFP **Fwpm \* GetSecurityInfo0** e **Fwpm \* SetSecurityInfo0**, dove * _ è l'acronimo del *\** nome dell'oggetto WFP. Queste funzioni sono semanticamente identiche alle funzioni Windows [_ *GetSecurityInfo* *](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) [**e SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

> [!Note]  
> Le **funzioni Fwpm \* SetSecurityInfo0 non** possono essere chiamate dall'interno di una transazione esplicita.

 

> [!Note]  
> Le **funzioni Fwpm \* SetSecurityInfo0** possono essere chiamate dall'interno di una sessione dinamica solo se vengono usate per gestire un oggetto dinamico creato all'interno della stessa sessione.

 

Il descrittore di sicurezza predefinito per il motore di filtro (l'oggetto motore radice nel diagramma seguente) è il seguente.

-   Concedere **diritti \_ di** accesso GENERIC ALL (GA) al gruppo Administrators predefinito.
-   Concedere **diritti di accesso GENERIC \_ READ** (GR) **GENERIC \_ WRITE** (GW) **GENERIC \_ EXECUTE** (GX) agli operatori di configurazione di rete.
-   Concedere i diritti di accesso **GRGWGX** agli identificatori di sicurezza del servizio (SSID) seguenti: MpsSvc (firewall Windows), NapAgent (agente protezione accesso alla rete), PolicyAgent (agente criteri IPsec), RpcSs (Remote Procedure Call) e WdiServiceHost (host del servizio di diagnostica).
-   Concedere **A tutti gli utenti FWPM \_ ACTRL \_ OPEN** e **FWPM \_ ACTRL \_ CLASSIFY.** Si tratta di diritti di accesso specifici di PAM, descritti nella tabella seguente.

I descrittori di sicurezza predefiniti rimanenti vengono derivati tramite ereditarietà.

Esistono alcuni controlli di accesso, ad esempio per **Fwpm \* Add0,** **Fwpm \* CreateEnumHandle0,** **Fwpm \* SubscribeChanges0** chiamate di funzione, che non possono essere eseguite a livello di singolo oggetto. Per queste funzioni sono disponibili oggetti contenitore per ogni tipo di oggetto. Per i tipi di oggetto standard (ad esempio, provider, callout, filtri), le funzioni **Fwpm \* GetSecurityInfo0** e **Fwpm \* SetSecurityInfo0** esistenti sono in overload, in modo che un parametro **GUID** Null identifichi il contenitore associato. Per gli altri tipi di oggetto, ad esempio eventi di rete e associazioni di sicurezza IPsec, sono disponibili funzioni esplicite per la gestione delle informazioni di sicurezza del contenitore.

BFE supporta l'ereditarietà automatica delle voci di controllo di accesso (ACE) elenco di controllo di accesso discrezionale (DACL). BFE non supporta ACE dell'elenco di controllo di accesso di sistema (SACL). Gli oggetti ereditano le voci ACE dal relativo contenitore. I contenitori ereditano le voci ACE dal motore di filtro. I percorsi di propagazione sono illustrati nel diagramma seguente.

![Diagramma che mostra i percorsi di propagazione ACE, a partire da 'Engine'.](images/access-control.jpg)

Per i tipi di oggetto standard, BFE applica tutti i diritti di accesso generici e standard. Inoltre, WFP definisce i diritti di accesso specifici seguenti.



| Diritto di accesso PAM                                                                                                                        | Descrizione                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ ADD**<br/>                                       | Obbligatorio per aggiungere un oggetto a un contenitore.<br/>                                                                                                                     |
| <span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ ADD \_ LINK**<br/>                       | Obbligatorio per creare un'associazione a un oggetto. Ad esempio, per aggiungere un filtro che fa riferimento a un callout, il chiamante deve avere accesso ADD \_ LINK al callout.<br/> |
| <span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN**<br/>    | Obbligatorio per avviare una transazione di lettura esplicita.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN**<br/> | Obbligatorio per iniziare una transazione di scrittura esplicita.<br/>                                                                                                              |
| <span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ CLASSIFY**<br/>                        | Obbligatorio per la classificazione in base a un livello in modalità utente.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**ENUMERAZIONE ACTRL FWPM \_ \_**<br/>                                    | Obbligatorio per enumerare gli oggetti in un contenitore. Tuttavia, l'enumeratore restituisce solo oggetti a cui il chiamante ha accesso FWPM \_ ACTRL \_ READ.<br/>              |
| <span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ OPEN**<br/>                                    | Obbligatorio per aprire una sessione con BFE.<br/>                                                                                                                          |
| <span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ READ**<br/>                                    | Obbligatorio per leggere le proprietà di un oggetto.<br/>                                                                                                                      |
| <span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**STATISTICHE LETTURA ACTRL FWPM \_ \_ \_**<br/>                 | Obbligatorio per leggere le statistiche.<br/>                                                                                                                                  |
| <span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ SUBSCRIBE**<br/>                     | Obbligatorio per sottoscrivere le notifiche. I Sottoscrittori riceveranno notifiche solo per gli oggetti a cui hanno accesso FWPM \_ ACTRL \_ READ.<br/>                 |
| <span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ WRITE**<br/>                                 | Obbligatorio per impostare le opzioni del motore.<br/>                                                                                                                               |



 

BFE ignora tutti i controlli di accesso per i chiamanti in modalità kernel.

Per impedire agli amministratori di bloccarsi da BFE, ai membri del gruppo administrators predefinito viene sempre concesso **FWPM \_ ACTRL \_ OPEN** all'oggetto motore. Di conseguenza, un amministratore può ottenere nuovamente l'accesso tramite la procedura seguente.

-   Abilitare il **privilegio edizione Standard \_ TAKE OWNERSHIP \_ \_ NAME.**
-   Chiamare [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). La chiamata ha esito positivo perché il chiamante è membro di Amministratori predefiniti.
-   Assumere la proprietà dell'oggetto motore. Questa operazione ha esito positivo perché il chiamante ha **edizione Standard \_ il privilegio TAKE OWNERSHIP \_ \_ NAME.**
-   Aggiornare l'elenco DACL. L'operazione ha esito positivo perché il proprietario ha sempre accesso **\_ all'applicazione livello dati WRITE**

Poiché BFE supporta il proprio controllo personalizzato, non genera controlli di accesso agli oggetti generici. Di conseguenza, l'elenco SACL viene ignorato.

## <a name="wfp-required-access-rights"></a>DIRITTI DI ACCESSO OBBLIGATORI

La tabella seguente illustra i diritti di accesso richiesti dalle funzioni WFP per accedere a vari oggetti della piattaforma di filtro. Le **funzioni FwpmFilter \* *_ sono elencate come esempio per l'accesso agli oggetti standard. Tutte le altre funzioni che accedono a oggetti standard seguono il modello di* accesso delle funzioni _ FwpmFilter. \***



Funzione

Object Checked

Accesso obbligatorio

[**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

Motore

**FWPM \_ ACTRL \_ OPEN**

[**FwpmEngineGetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

Motore

**FWPM \_ ACTRL \_ READ**

[**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

Motore

**FWPM \_ ACTRL \_ WRITE**

[**FwpmSessionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

Motore

**ENUMERAZIONE ACTRL FWPM \_ \_**

[**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

Motore

**FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN**  &  **FWPM \_ ACTRL BEGIN WRITE \_ \_ \_ TXN**

[**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Provider di contenitori<br/> Livello<br/> Sub-Layer<br/> Callout<br/> Contesto del provider<br/>

**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ ADD \_ LINK**<br/> **FWPM \_ ACTRL \_ ADD \_ LINK**<br/> **FWPM \_ ACTRL \_ ADD \_ LINK**<br/> **FWPM \_ ACTRL \_ ADD \_ LINK**<br/> **FWPM \_ ACTRL \_ ADD \_ LINK**<br/>

[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)<br/>

Filtra

**DELETE**

[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)<br/>

Filtra

**FWPM \_ ACTRL \_ READ**

[**FwpmFilterCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

Filtro contenitore<br/>

**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ READ**<br/>

[**FwpmFilterSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

Contenitore

**FWPM \_ ACTRL \_ SUBSCRIBE**

[**FwpmFilterSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

Contenitore

**FWPM \_ ACTRL \_ READ**

[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

DATABASE SA IPsec

**STATISTICHE DI LETTURA \_ FWPM ACTRL \_ \_**

[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)<br/> [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

DATABASE SA IPsec

**FWPM \_ ACTRL \_ ADD**

[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)<br/>

DATABASE SA IPsec

**DELETE**

[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

DATABASE SA IPsec

**FWPM \_ ACTRL \_ READ**

[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)<br/>

DATABASE SA IPsec

**FWPM \_ ACTRL \_ ENUM**  &  **FWPM \_ ACTRL \_ READ**

[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

Database sa IKE

**STATISTICHE DI LETTURA \_ FWPM ACTRL \_ \_**

[**IkeextSaDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

Database sa IKE

**DELETE**

[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

Database sa IKE

**FWPM \_ ACTRL \_ READ**

[**IkeextSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

Database sa IKE

**FWPM \_ ACTRL \_ ENUM**  &  **FWPM \_ ACTRL \_ READ**

[**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

Contenitore

**ENUMERAZIONE \_ ACTRL FWPM \_**

[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)<br/>

Nessun controllo di accesso aggiuntivo oltre a quelli per i singoli filtri e contesti del provider



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Diritti di accesso standard**](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Windows di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[**Windows Filtro degli identificatori dei diritti di accesso alla piattaforma**](access-right-identifiers.md)
</dt> </dl>

 

