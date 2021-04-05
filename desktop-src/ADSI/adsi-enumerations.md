---
title: Enumerazioni ADSI
description: Le interfacce ADSI (Active Directory Service Interfaces) definiscono e utilizzano le enumerazioni elencate nella tabella seguente.
ms.assetid: f0ad5ce5-742d-40dc-ac5a-31d779e40bfd
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, riferimento, enumerazioni
- Enumerazioni ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459aa59bc0f7907f59a4cd5a7e5fcb4f1b2630d8
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/27/2020
ms.locfileid: "104046391"
---
# <a name="adsi-enumerations"></a>Enumerazioni ADSI

Le interfacce ADSI (Active Directory Service Interfaces) definiscono e utilizzano le enumerazioni elencate nella tabella seguente.



| Enumerazione                                                           | Descrizione                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_enumerazione ACEFLAG \_ ADS**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum)                        | Specifica il modo in cui la sicurezza viene propagata per le voci di controllo di accesso (ACE) ereditate e i tipi di controllo per una voce ACE di sistema.                                                                                                                                             |
| [**\_enumerazione ACETYPE \_ ADS**](/windows/win32/api/iads/ne-iads-ads_acetype_enum)                        | Specifica il tipo ACE.                                                                                                                                                                                                                                           |
| [**\_enumerazione di autenticazione Ads \_**](/windows/win32/api/iads/ne-iads-ads_authentication_enum)          | Specifica il livello di sicurezza usato per l'autenticazione di un client.                                                                                                                                                                                                     |
| [**\_enumerazione riferimenti inseguiti Ads \_ \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)       | Specifica il comportamento dell'inseguimento dei riferimenti.                                                                                                                                                                                                                       |
| [**\_DEREFENUM ADS**](/windows/win32/api/iads/ne-iads-ads_derefenum)                               | Specifica il comportamento della dereferenziazione dell'alias.                                                                                                                                                                                                                    |
| [**\_enumerazione visualizzazione \_ annunci**](/windows/win32/api/iads/ne-iads-ads_display_enum)                        | Specifica la modalità di visualizzazione di un percorso.                                                                                                                                                                                                                                |
| [**\_enumerazione della \_ modalità di escape Ads \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)               | Specifica se i caratteri speciali sono preceduti da un carattere di escape, senza caratteri di escape o senza tocco.                                                                                                                                                                                        |
| [**\_enumerazione FLAGTYPE \_ ADS**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum)                      | Specifica la presenza dei campi **ObjectType** o **InheritedObjectType** in una voce ACE.                                                                                                                                                                         |
| [**\_enumerazione formato \_ ADS**](/windows/win32/api/iads/ne-iads-ads_format_enum)                          | Specifica il tipo di valori in un oggetto PathName.                                                                                                                                                                                                                |
| [**\_enumerazione del \_ tipo di gruppo Ads \_**](/windows/win32/api/iads/ne-iads-ads_group_type_enum)                 | Specifica il tipo di gruppo del membro.                                                                                                                                                                                                                           |
| [**\_nome Ads \_ INITTYPE \_ enum**](/windows/win32/api/iads/ne-iads-ads_name_inittype_enum)           | Specifica il tipo di inizializzazione da eseguire per un oggetto translate del nome.                                                                                                                                                                                  |
| [**\_tipo di nome Ads \_ \_ enum**](/windows/win32/api/iads/ne-iads-ads_name_type_enum)                   | Specifica il formato utilizzato per rappresentare nomi distinti.                                                                                                                                                                                                       |
| [**\_enumerazione delle opzioni Ads \_**](/windows/win32/api/iads/ne-iads-ads_option_enum)                          | Specifica le opzioni disponibili utilizzate dall'interfaccia [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) per la modifica degli oggetti directory.                                                                                                                        |
| [**\_ \_ enumerazione codifica password \_ ADS**](/windows/win32/api/iads/ne-iads-ads_password_encoding_enum)   | Usato per identificare il tipo di codifica delle password usato con l'opzione **Ads \_ \_ \_ metodo password metodo** nei metodi [**IADsObjectOptions:: GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) e [**IADsObjectOptions:: SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) . |
| [**\_enumerazione PATHTYPE \_ ADS**](/windows/win32/api/iads/ne-iads-ads_pathtype_enum)                      | Specifica il tipo di oggetto in cui viene modificato il descrittore di sicurezza.                                                                                                                                                                                        |
| [**\_enumerazione preferenze \_ ADS**](/windows/win32/api/iads/ne-iads-ads_preferences_enum)                | Specifica le preferenze di query del OLE DB per ADSI.                                                                                                                                                                                                           |
| [**\_ \_ enum operazione proprietà \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) | Specifica le modalità di aggiornamento dei valori delle proprietà nella cache delle proprietà.                                                                                                                                                                                               |
| [**\_enumerazione dei diritti Ads \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum)                          | Specifica i diritti di accesso a un oggetto servizio di directory.                                                                                                                                                                                                        |
| [**\_SCOPEENUM ADS**](/windows/win32/api/iads/ne-iads-ads_scopeenum)                               | Specifica l'ambito di una ricerca di directory.                                                                                                                                                                                                                        |
| [**\_enumerazione del \_ controllo ADS SD \_**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum)                 | Specifica che un elenco di controllo di accesso (ACL) deve essere protetto quando le nuove autorizzazioni vengono applicate in modo ricorsivo a un albero di directory.                                                                                                                                  |
| [**\_ \_ enum formato SD \_ ADS**](/windows/win32/api/iads/ne-iads-ads_sd_format_enum)                   | Specifica il formato per la conversione del descrittore di sicurezza.                                                                                                                                                                                                      |
| [**\_enumerazione di \_ Revisione \_ SD per ADS**](/windows/win32/api/iads/ne-iads-ads_sd_revision_enum)               | Specifica il numero di revisione di una voce ACE o ACL.                                                                                                                                                                                                                   |
| [**\_enumerazione SEARCHPREF \_ ADS**](/windows/win32/api/iads/ne-iads-ads_searchpref_enum)                  | Specifica le preferenze della ricerca.                                                                                                                                                                                                                              |
| [**\_ \_ enum info di sicurezza Ads \_**](/windows/win32/api/iads/ne-iads-ads_security_info_enum)           | Specifica le opzioni per l'analisi dei dati di sicurezza.                                                                                                                                                                                                                |
| [**\_enum di tipo \_ ADS**](/windows/win32/api/iads/ne-iads-ads_settype_enum)                        | Specifica il formato del percorso in [**IADsPathname:: set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set).                                                                                                                                                                                       |
| [**\_STATUSENUM ADS**](/windows/win32/api/iads/ne-iads-ads_statusenum)                             | Specifica lo stato delle preferenze di ricerca.                                                                                                                                                                                                                       |
| [**\_enumerazione SYSTEMFLAG \_ ADS**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)                  | Specifica i tipi di attributi rappresentati da un oggetto **attributeSchema** .                                                                                                                                                                                   |
| [**\_ \_ enumerazione flag utente \_ ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)                   | Specifica i flag utilizzati per la modifica delle proprietà utente.                                                                                                                                                                                                            |
| [**\_enum dialetto \_ ADSI**](/windows/win32/api/iads/ne-iads-adsi_dialect_enum)                      | Specifica i dialetti di query ADSI disponibili.                                                                                                                                                                                                                          |
| [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)                                    | Specifica i tipi di dati utilizzati per interpretare una stringa di sintassi estesa ADSI.                                                                                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Poiché le applicazioni di Visual Basic Scripting Edition non sono in grado di leggere dati da una libreria dei tipi, le applicazioni VBScript non sono in grado di riconoscere le costanti simboliche come definito nelle enumerazioni. Usare invece le costanti numeriche per impostare i flag appropriati in un'applicazione VBScript. Per usare le costanti simboliche come una procedura di programmazione efficace, scrivere dichiarazioni esplicite di tali costanti, come fatto in questo caso, nelle applicazioni VBScript.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
</dt> <dt>

[**IADsPathname:: set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)
</dt> </dl>

 

 




