---
title: Enumerazioni ADSI
description: Active Directory Service Interfaces (ADSI) definisce e usa le enumerazioni elencate nella tabella seguente.
ms.assetid: f0ad5ce5-742d-40dc-ac5a-31d779e40bfd
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , riferimenti, enumerazioni
- Enumerazioni ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10d5aed5688e7128a64a32dee2f83efa22ab5bf292231517026299ccb592886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023909"
---
# <a name="adsi-enumerations"></a>Enumerazioni ADSI

Active Directory Service Interfaces (ADSI) definisce e usa le enumerazioni elencate nella tabella seguente.



| Enumerazione                                                           | Descrizione                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ENUMERAZIONE \_ ADS ACEFLAG \_**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum)                        | Specifica la modalità di propagazione della sicurezza per le voci di controllo di accesso (ACE) ereditate e i tipi di controllo per una voce ACE di sistema.                                                                                                                                             |
| [**ENUMERAZIONE ADS \_ ACETYPE \_**](/windows/win32/api/iads/ne-iads-ads_acetype_enum)                        | Specifica il tipo ACE.                                                                                                                                                                                                                                           |
| [**ENUMERAZIONE DI ADS \_ AUTHENTICATION \_**](/windows/win32/api/iads/ne-iads-ads_authentication_enum)          | Specifica il livello di sicurezza utilizzato per l'autenticazione di un client.                                                                                                                                                                                                     |
| [**ENUMERAZIONE ADS \_ CHASE \_ REFERRALS \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)       | Specifica il comportamento della ricerca delle segnalazioni.                                                                                                                                                                                                                       |
| [**ADS \_ DEREFENUM**](/windows/win32/api/iads/ne-iads-ads_derefenum)                               | Specifica il comportamento della dereferenziazione degli alias.                                                                                                                                                                                                                    |
| [**ENUMERAZIONE DI \_ VISUALIZZAZIONE \_ DI ADS**](/windows/win32/api/iads/ne-iads-ads_display_enum)                        | Specifica la modalità di visualizzazione di un percorso.                                                                                                                                                                                                                                |
| [**ENUMERAZIONE ADS \_ ESCAPE \_ MODE \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)               | Specifica se i caratteri speciali sono preceduti da caratteri di escape, senza caratteri di escape o senza caratteri di escape.                                                                                                                                                                                        |
| [**ENUMERAZIONE ADS \_ FLAGTYPE \_**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum)                      | Specifica la presenza dei campi **ObjectType** **o InheritedObjectType** in una ACE.                                                                                                                                                                         |
| [**ENUMERAZIONE ADS \_ FORMAT \_**](/windows/win32/api/iads/ne-iads-ads_format_enum)                          | Specifica il tipo di valori in un oggetto pathname.                                                                                                                                                                                                                |
| [**ENUMERAZIONE DEL \_ TIPO DI \_ GRUPPO \_ ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum)                 | Specifica il tipo di gruppo del membro.                                                                                                                                                                                                                           |
| [**ENUMERAZIONE \_ ADS NAME \_ \_ INITTYPE**](/windows/win32/api/iads/ne-iads-ads_name_inittype_enum)           | Specifica il tipo di inizializzazione da eseguire su un oggetto di conversione del nome.                                                                                                                                                                                  |
| [**ENUMERAZIONE ADS \_ NAME \_ TYPE \_**](/windows/win32/api/iads/ne-iads-ads_name_type_enum)                   | Specifica il formato utilizzato per rappresentare i nomi distinti.                                                                                                                                                                                                       |
| [**ENUMERAZIONE DELL'OPZIONE ADS \_ \_**](/windows/win32/api/iads/ne-iads-ads_option_enum)                          | Specifica le opzioni disponibili utilizzate [**dall'interfaccia IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) per la modifica degli oggetti directory.                                                                                                                        |
| [**ENUMERAZIONE DI CODIFICA \_ \_ PASSWORD \_ DI ADS**](/windows/win32/api/iads/ne-iads-ads_password_encoding_enum)   | Usato per identificare il tipo di codifica della password usato con l'opzione **ADS \_ OPTION PASSWORD \_ \_ METHOD** nei metodi [**IADsObjectOptions::GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) e [**IADsObjectOptions::SetOption.**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) |
| [**ENUMERAZIONE ADS \_ PATHTYPE \_**](/windows/win32/api/iads/ne-iads-ads_pathtype_enum)                      | Specifica il tipo di oggetto in cui viene modificato il descrittore di sicurezza.                                                                                                                                                                                        |
| [**ENUMERAZIONE ADS \_ PREFERENCES \_**](/windows/win32/api/iads/ne-iads-ads_preferences_enum)                | Specifica le preferenze di query del OLE DB per ADSI.                                                                                                                                                                                                           |
| [**ENUMERAZIONE ADS \_ \_ PROPERTY OPERATION \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) | Specifica i modi per aggiornare i valori delle proprietà nella cache delle proprietà.                                                                                                                                                                                               |
| [**ENUMERAZIONE DEI DIRITTI DI ADS \_ \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum)                          | Specifica i diritti di accesso a un oggetto servizio directory.                                                                                                                                                                                                        |
| [**ADS \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum)                               | Specifica l'ambito di una ricerca di directory.                                                                                                                                                                                                                        |
| [**ENUMERAZIONE DI \_ CONTROLLO ADS SD \_ \_**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum)                 | Specifica che un elenco di controllo di accesso (ACL) deve essere protetto quando le nuove autorizzazioni vengono applicate in modo ricorsivo a un albero di directory.                                                                                                                                  |
| [**ENUMERAZIONE ADS \_ SD \_ FORMAT \_**](/windows/win32/api/iads/ne-iads-ads_sd_format_enum)                   | Specifica il formato per la conversione del descrittore di sicurezza.                                                                                                                                                                                                      |
| [**ENUMERAZIONE ADS \_ SD \_ REVISION \_**](/windows/win32/api/iads/ne-iads-ads_sd_revision_enum)               | Specifica il numero di revisione di una ACE o ACL.                                                                                                                                                                                                                   |
| [**ENUMERAZIONE ADS \_ \_ SEARCHPREF**](/windows/win32/api/iads/ne-iads-ads_searchpref_enum)                  | Specifica le preferenze della ricerca.                                                                                                                                                                                                                              |
| [**ENUMERAZIONE DELLE \_ INFORMAZIONI \_ DI SICUREZZA \_ DI ADS**](/windows/win32/api/iads/ne-iads-ads_security_info_enum)           | Specifica le opzioni per l'analisi dei dati di sicurezza.                                                                                                                                                                                                                |
| [**ENUMERAZIONE ADS \_ \_ SETTYPE**](/windows/win32/api/iads/ne-iads-ads_settype_enum)                        | Specifica il formato del percorso in [**IADsPathname::Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set).                                                                                                                                                                                       |
| [**ADS \_ STATUSENUM**](/windows/win32/api/iads/ne-iads-ads_statusenum)                             | Specifica lo stato delle preferenze di ricerca.                                                                                                                                                                                                                       |
| [**ENUMERAZIONE ADS \_ SYSTEMFLAG \_**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)                  | Specifica i tipi di attributi rappresentati da un **oggetto attributeSchema.**                                                                                                                                                                                   |
| [**ENUMERAZIONE DEL \_ FLAG UTENTE \_ \_ DI ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)                   | Specifica i flag utilizzati per la modifica delle proprietà utente.                                                                                                                                                                                                            |
| [**ENUMERAZIONE ADSI \_ DIALECT \_**](/windows/win32/api/iads/ne-iads-adsi_dialect_enum)                      | Specifica i dialetti di query ADSI disponibili.                                                                                                                                                                                                                          |
| [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)                                    | Specifica i tipi di dati utilizzati per interpretare una stringa di sintassi estesa ADSI.                                                                                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Poiché Visual Basic Scripting Edition non è in grado di leggere i dati da una libreria dei tipi, le applicazioni VBScript non possono riconoscere costanti simboliche come definito in queste enumerazioni. Usare invece le costanti numeriche per impostare i flag appropriati in un'applicazione VBScript. Per usare le costanti simboliche come buona procedura di programmazione, scrivere dichiarazioni esplicite di tali costanti, come fatto qui, nelle applicazioni VBScript.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
</dt> <dt>

[**IADsPathname::Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)
</dt> </dl>

 

 




