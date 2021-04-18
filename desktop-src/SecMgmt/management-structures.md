---
description: Elenca le strutture usate con le API di gestione della sicurezza.
ms.assetid: 8df25095-a215-464a-abac-39a6ea05f6a3
title: Strutture di gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2212332b65d89a8d2c1f5a24601a59cca041ff42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316638"
---
# <a name="security-management-structures"></a>Strutture di gestione della sicurezza

Questa sezione contiene le pagine di riferimento per i gruppi di strutture seguenti:

-   [Strutture di gestione dei criteri LSA](#lsa-policy-management-structures)
-   [Strutture degli allegati](#attachment-structures)
-   [Strutture più sicure](#safer-structures)

## <a name="lsa-policy-management-structures"></a>Strutture di gestione dei criteri LSA

Le seguenti strutture sono utilizzate dalle funzioni di gestione dei criteri dell' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA).



| Struttura                                                                       | Descrizione                                                                                                                                   |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_informazioni di autenticazione LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_auth_information)                          | Contiene le informazioni di autenticazione per un dominio trusted.                                                                                     |
| [**\_informazioni enumerazione \_ LSA**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_enumeration_information)            | Contiene un puntatore a un [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID).    |
| [**\_attributi dell'oggetto LSA \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_object_attributes)                        | Specifica gli attributi di una connessione all'oggetto [**criteri**](policy-object.md) .                                                       |
| [**elenco di domini di \_ riferimento LSA \_ \_**](/windows/win32/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list)             | Contiene informazioni sui domini a cui viene fatto riferimento in un'operazione di ricerca.                                                                      |
| [**\_nome tradotto LSA \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_name)                            | Contiene informazioni sull'account identificato da un SID.                                                                                   |
| [**\_SID tradotto LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_translated_sid)                              | Contiene informazioni sul SID che identifica un account.                                                                                |
| [**\_SID2 tradotto LSA \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_sid2)                            | Contiene informazioni sul SID che identifica un account.                                                                                |
| [**\_informazioni di attendibilità LSA \_**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information)                        | Identifica un dominio.                                                                                                                          |
| [**\_stringa Unicode \_ LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string)                              | Contiene una stringa e le relative informazioni sulla lunghezza.                                                                                                 |
| [**\_informazioni sul \_ dominio dell'account del criterio \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_account_domain_info)             | Utilizzato per impostare ed eseguire una query sul nome e SID del dominio dell'account del sistema.                                                                        |
| [**\_ \_ informazioni sugli eventi di controllo dei criteri \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_audit_events_info)                 | Utilizzato per impostare ed eseguire query sulle regole di controllo del sistema.                                                                                            |
| [**\_informazioni sul \_ dominio \_ DNS del criterio**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info)                     | Utilizzato per impostare ed eseguire query Domain Name System informazioni (DNS) sul dominio primario associato a un oggetto [**criteri**](policy-object.md) . |
| [**\_informazioni sul \_ ruolo del server LSA \_ del criterio \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_lsa_server_role_info)          | Utilizzato per impostare ed eseguire una query sul ruolo di un server LSA.                                                                                              |
| [**\_informazioni sulla modifica dei criteri \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_modification_info)                  | Utilizzato per eseguire query sulle informazioni relative alla data e all'ora di creazione e all'Ultima modifica del database LSA.                                                  |
| [**\_ \_ informazioni account PD \_ criterio**](policy-pd-account-info.md)                     | Obsoleta. Le workstation usano il nome della workstation seguito da $ come nome dell'account.                                                          |
| [**\_informazioni sul \_ dominio \_ primario del criterio**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_primary_domain_info)             | Obsoleta. Usare invece **PolicyDnsDomainInformation** e la struttura di [**\_ \_ \_ informazioni sul dominio DNS del criterio**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info) .           |
| [**\_informazioni di \_ autenticazione del dominio trusted \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_auth_information)   | Utilizzato per recuperare le informazioni di autenticazione per un dominio trusted.                                                                             |
| [**\_ \_ informazioni complete sul dominio trusted \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_full_information)   | Utilizzato per recuperare informazioni complete su un dominio trusted.                                                                                 |
| [**\_informazioni di \_ base sul dominio \_ Trusted**](/previous-versions/windows/desktop/legacy/ms722475(v=vs.85)) | Informazioni su un dominio trusted. Questa struttura è identica alle [**\_ \_ informazioni di attendibilità LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information).                  |
| [**\_informazioni sul dominio trusted, ad \_ \_ esempio**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_information_ex)       | Utilizzato per recuperare informazioni estese su un dominio trusted.                                                                                 |
| [**\_informazioni sul \_ nome di dominio attendibile \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_name_info)                 | Utilizzato per eseguire una query o impostare il nome di un dominio trusted.                                                                                            |
| [**\_informazioni password attendibili \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_password_info)                        | Utilizzato per eseguire una query o impostare la password per un dominio trusted.                                                                                       |
| [**\_informazioni sull' \_ offset \_ POSIX attendibile**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_posix_offset_info)               | Utilizzato per eseguire una query o impostare il valore usato per generare gli identificatori di utenti e gruppi POSIX.                                                             |



 

I tipi di struttura seguenti sono obsoleti o sono riservati per utilizzi futuri:

-   **\_ \_ \_ informazioni query complete sul controllo dei criteri \_**
-   **\_informazioni sul \_ \_ set completo di controllo \_ dei criteri**
-   **\_informazioni sul \_ log di controllo dei criteri \_**
-   **\_ \_ informazioni quota predefinite \_ criteri**
-   **\_ \_ informazioni origine replica \_ criteri**
-   **\_informazioni sui controller attendibili \_**

## <a name="attachment-structures"></a>Strutture degli allegati

Le strutture seguenti vengono utilizzate dalle DLL allegati della configurazione di sicurezza e dalle relative funzioni di supporto. Queste strutture sono definite in Scesvc. h.



| Struttura                                                        | Descrizione                                                                                                                                     |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_informazioni di configurazione di SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info) | Contiene le informazioni di configurazione per un servizio.                                                                                               |
| [**\_linea di configurazione di SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_line) | Contiene informazioni su una riga di dati di configurazione.                                                                                        |
| [**\_informazioni sull'analisi SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info)           | Contiene le informazioni di analisi.                                                                                                              |
| [**\_linea di analisi SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_line)           | Contiene la chiave, il valore e la lunghezza del valore per una riga specifica specificata da una struttura di [**\_ \_ informazioni di analisi SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info) . |
| [**\_informazioni callback \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)           | Contiene un handle di database opaco e puntatori a funzione di callback per eseguire query, impostare e liberare informazioni.                                          |



 

## <a name="safer-structures"></a>Strutture più sicure

Le strutture e il tipo enumerato seguenti vengono usati più in sicurezza. Sono definite in WinSafer. h.



| Struttura                                                                | Descrizione                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_proprietà del codice più sicure \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_code_properties_v2)                 | Contiene informazioni sull'immagine del codice e criteri da controllare nell'immagine del codice. Una matrice di queste strutture viene passata alla funzione [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) .                                                                  |
| [**\_intestazione di identificazione più sicura \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header)     | Struttura di intestazione per l' [**\_ \_ Identificazione del percorso più sicura**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification), l' [**\_ \_ Identificazione hash più sicura**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)e strutture di [**\_ \_ Identificazione URLZONE più sicure**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification) . |
| [**\_Identificazione del percorso più sicuro \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification) | Include il nome del percorso di un'immagine del codice da verificare.                                                                                                                                                                                                      |
| [**\_Identificazione hash più sicura \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)         | Identifica un hash dell'immagine del codice da verificare.                                                                                                                                                                                                      |
| [**\_Identificazione URLZONE più sicura \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification)   | Identifica la zona dell'URL di origine dell'immagine del codice da verificare.                                                                                                                                                                                      |



 

 

 
