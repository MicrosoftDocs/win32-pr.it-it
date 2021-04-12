---
title: Controllo di accesso (piattaforma filtro Windows)
description: In Windows Filtering Platform (WFP), il servizio BFE (Base Filtering Engine) implementa il modello di controllo di accesso di Windows standard basato sui token di accesso e i descrittori di sicurezza.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104350986"
---
# <a name="access-control-windows-filtering-platform"></a>Controllo di accesso (piattaforma filtro Windows)

In Windows Filtering Platform (WFP), il servizio BFE (Base Filtering Engine) implementa il [modello di controllo di accesso di Windows](/windows/desktop/SecAuthZ/access-control-model) standard basato sui token di accesso e i descrittori di sicurezza.

## <a name="access-control-model"></a>Modello di controllo di accesso

I descrittori di sicurezza possono essere specificati quando si aggiungono nuovi oggetti WFP, ad esempio filtri e sottolivelli. I descrittori di sicurezza vengono gestiti tramite le funzioni di gestione PAM **Fwpm \* GetSecurityInfo0** e **Fwpm \* SetSecurityInfo0**, dove * *\** _ sta per il nome dell'oggetto WFP. Queste funzioni sono semanticamente identiche alle funzioni Windows [_ *GetSecurityInfo* *](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

> [!Note]  
> Non è possibile chiamare le funzioni **\* SetSecurityInfo0 di Fwpm** dall'interno di una transazione esplicita.

 

> [!Note]  
> Le funzioni **Fwpm \* SetSecurityInfo0** possono essere chiamate solo dall'interno di una sessione dinamica se vengono usate per gestire un oggetto dinamico creato all'interno della stessa sessione.

 

Il descrittore di sicurezza predefinito per il motore di filtro (l'oggetto motore radice nel diagramma seguente) è il seguente.

-   Concedere i diritti di accesso **generici \_ All** (GA) al gruppo Administrators predefinito.
-   Concedere i diritti di accesso generico di **\_ lettura** (gr) Generic **\_ Write** ( **GW) per \_** gli operatori di configurazione di rete.
-   Concedere i diritti di accesso **GRGWGX** ai seguenti identificatori di sicurezza del servizio (SSID): MpsSvc (Windows Firewall), napagent (agente protezione accesso alla rete), PolicyAgent (agente criteri IPSec), RPCSS (Remote Procedure Call) e WdiServiceHost (host del servizio di diagnostica).
-   Concedere a **FWPM \_ ACTRL \_ Open** e **FWPM \_ ACTRL \_ classificate** a tutti. Si tratta di diritti di accesso specifici di WFP, descritti nella tabella seguente.

I rimanenti descrittori di sicurezza predefiniti sono derivati tramite ereditarietà.

Sono disponibili alcuni controlli di accesso, ad esempio per le chiamate di funzione **Fwpm \* Add0**, **Fwpm \* CreateEnumHandle0**, **Fwpm \* SubscribeChanges0** , che non possono essere eseguite a livello di singolo oggetto. Per queste funzioni sono disponibili oggetti contenitore per ogni tipo di oggetto. Per i tipi di oggetto standard (ad esempio, provider, callout, filtri), le funzioni **Fwpm \* GetSecurityInfo0** e **Fwpm \* SetSecurityInfo0** esistenti sono in overload, in modo che un parametro **GUID** null identifichi il contenitore associato. Per gli altri tipi di oggetto (ad esempio, eventi di rete e associazioni di sicurezza IPsec), sono disponibili funzioni esplicite per la gestione delle informazioni di sicurezza del contenitore.

BFE supporta l'ereditarietà automatica delle voci di controllo di accesso (DACL) dell'elenco di controllo di accesso discrezionale (DACL). BFE non supporta le voci dell'elenco di controllo di accesso di sistema (SACL). Gli oggetti ereditano le voci ACE dal relativo contenitore. I contenitori ereditano le voci ACE dal motore di filtro. Il diagramma seguente illustra i percorsi di propagazione.

![Diagramma che mostra i percorsi di propagazione ACE, a partire da' Engine '.](images/access-control.jpg)

Per i tipi di oggetto standard, BFE impone tutti i diritti di accesso generici e standard. Inoltre, WFP definisce i seguenti diritti di accesso specifici.



| Diritto di accesso WFP                                                                                                                        | Descrizione                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**\_aggiunta FWPM ACTRL \_**<br/>                                       | Obbligatorio per aggiungere un oggetto a un contenitore.<br/>                                                                                                                     |
| <span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ Aggiungi \_ collegamento**<br/>                       | Obbligatorio per creare un'associazione a un oggetto. Per aggiungere, ad esempio, un filtro che fa riferimento a un callout, il chiamante deve disporre dell' \_ accesso Aggiungi collegamento al callout.<br/> |
| <span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Read \_ transazione**<br/>    | Obbligatorio per iniziare una transazione di lettura esplicita.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Write \_ transazione**<br/> | Obbligatorio per iniziare una transazione di scrittura esplicita.<br/>                                                                                                              |
| <span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_classificazione FWPM ACTRL \_**<br/>                        | Obbligatorio per la classificazione in base a un livello in modalità utente.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**\_enumerazione FWPM ACTRL \_**<br/>                                    | Obbligatorio per enumerare gli oggetti in un contenitore. Tuttavia, l'enumeratore restituisce solo gli oggetti a cui il chiamante \_ ha \_ accesso in lettura ACTRL FWPM.<br/>              |
| <span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ aperto**<br/>                                    | Obbligatorio per aprire una sessione con BFE.<br/>                                                                                                                          |
| <span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ Read**<br/>                                    | Obbligatorio per leggere le proprietà di un oggetto.<br/>                                                                                                                      |
| <span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**\_ \_ statistiche leggere FWPM \_ ACTRL**<br/>                 | Obbligatorio per leggere le statistiche.<br/>                                                                                                                                  |
| <span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**sottoscrizione di FWPM \_ ACTRL \_**<br/>                     | Obbligatorio per sottoscrivere le notifiche. I sottoscrittori riceveranno solo le notifiche per gli oggetti a cui hanno \_ accesso in lettura ACTRL FWPM \_ .<br/>                 |
| <span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**\_scrittura FWPM ACTRL \_**<br/>                                 | Obbligatorio per impostare le opzioni del motore.<br/>                                                                                                                               |



 

BFE ignora tutti i controlli di accesso per i chiamanti in modalità kernel.

Per impedire agli amministratori di bloccarsi da BFE, ai membri del gruppo Administrators predefinito viene sempre concesso **FWPM \_ ACTRL \_ aperto** all'oggetto motore. Pertanto, un amministratore può ottenere nuovamente l'accesso tramite i passaggi seguenti.

-   Abilitare il **privilegio \_ se \_ accetta \_ nome proprietà** .
-   Chiamare [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). La chiamata ha esito positivo perché il chiamante è un membro degli amministratori predefiniti.
-   Assumere la proprietà dell'oggetto motore. Questa operazione ha esito positivo perché il chiamante ha il privilegio **se \_ accetta il \_ \_ nome di proprietà** .
-   Aggiornare l'elenco DACL. Questa operazione ha esito positivo perché il proprietario ha sempre l'accesso a **\_ DAC in scrittura**

Poiché BFE supporta il proprio controllo personalizzato, non genera controlli di accesso agli oggetti generici. Quindi, il SACL viene ignorato.

## <a name="wfp-required-access-rights"></a>Diritti di accesso necessari per Pam

La tabella seguente illustra i diritti di accesso richiesti dalle funzioni PAM per accedere a vari oggetti della piattaforma di filtro. Le **\* *funzioni _ FwpmFilter sono elencate come esempio per l'accesso agli oggetti standard. Tutte le altre funzioni che accedono agli oggetti standard seguono il modello di* \*** accesso alle funzioni _ FwpmFilter.



Funzione

Oggetto selezionato

Accesso obbligatorio

[**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

Motore

**FWPM \_ ACTRL \_ aperto**

[**FwpmEngineGetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

Motore

**FWPM \_ ACTRL \_ Read**

[**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

Motore

**\_scrittura FWPM ACTRL \_**

[**FwpmSessionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

Motore

**\_enumerazione FWPM ACTRL \_**

[**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

Motore

**FWPM \_ ACTRL \_ Begin \_ Read \_ transazione**  &  **FWPM \_ ACTRL \_ Begin \_ Write \_ transazione**

[**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Provider di contenitori<br/> Livello<br/> Sub-Layer<br/> Callout<br/> Contesto del provider<br/>

**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ Aggiungi \_ collegamento**<br/> **FWPM \_ ACTRL \_ Aggiungi \_ collegamento**<br/> **FWPM \_ ACTRL \_ Aggiungi \_ collegamento**<br/> **FWPM \_ ACTRL \_ Aggiungi \_ collegamento**<br/> **FWPM \_ ACTRL \_ Aggiungi \_ collegamento**<br/>

[](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0** FwpmFilterDeleteById0](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)<br/>

Filtra

**DELETE**

[](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0** FwpmFilterGetById0](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)<br/>

Filtra

**FWPM \_ ACTRL \_ Read**

[**FwpmFilterCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

Filtro contenitore<br/>

**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ Read**<br/>

[**FwpmFilterSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

Contenitore

**sottoscrizione di FWPM \_ ACTRL \_**

[**FwpmFilterSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

Contenitore

**FWPM \_ ACTRL \_ Read**

[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

DB SA IPsec

**\_ \_ statistiche leggere FWPM \_ ACTRL**

[](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0** IPsecSaContextCreate0](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)<br/> [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

DB SA IPsec

**\_aggiunta FWPM ACTRL \_**

[](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0** IPsecSaContextDeleteById0](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)<br/>

DB SA IPsec

**DELETE**

[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

DB SA IPsec

**FWPM \_ ACTRL \_ Read**

[](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0** IPsecSaContextCreateEnumHandle0](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)<br/>

DB SA IPsec

**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ Read**

[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

DB SA IKE

**\_ \_ statistiche leggere FWPM \_ ACTRL**

[**IkeextSaDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

DB SA IKE

**DELETE**

[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

DB SA IKE

**FWPM \_ ACTRL \_ Read**

[**IkeextSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

DB SA IKE

**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ Read**

[**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

Contenitore

**\_enumerazione FWPM ACTRL \_**

[](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0** FwpmIPsecTunnelAdd0](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)<br/>

Nessun controllo di accesso aggiuntivo oltre a quelli per i singoli contesti di filtri e provider



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Diritti di accesso standard**](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Modello di controllo di accesso di Windows](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[**Identificatori dei diritti di accesso della piattaforma filtro Windows**](access-right-identifiers.md)
</dt> </dl>

 

