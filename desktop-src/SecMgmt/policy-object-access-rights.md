---
description: Elenca e descrive i tipi di accesso dell'oggetto Policy.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Diritti di accesso agli oggetti criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae22db51c28e76e7122a1f7baf781671d9cc445e253fb6df7d63f87e3f7e921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005099"
---
# <a name="policy-object-access-rights"></a>Diritti di accesso agli oggetti criteri

[**L'oggetto Policy**](policy-object.md) ha i tipi di accesso specifici dell'oggetto seguenti:



| Tipo di accesso                         | Descrizione                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CRITERI \_ VISUALIZZA \_ INFORMAZIONI \_ LOCALI    | Questo tipo di accesso è necessario per leggere le varie informazioni sui criteri di sicurezza del sistema di destinazione. Sono inclusi la quota predefinita, il controllo, lo stato del server e le informazioni sui ruoli e le informazioni sull'attendibilità. Questo tipo di accesso è necessario anche per enumerare domini, account e [*privilegi attendibili.*](/windows/desktop/SecGloss/p-gly) |
| POLICY \_ GET PRIVATE INFORMATION (OTTENERE INFORMAZIONI PRIVATE SUI \_ \_ CRITERI)   | Questo tipo di accesso è necessario per visualizzare informazioni riservate, ad esempio i nomi degli account stabiliti per le relazioni di dominio trusted.                                                                                                                                                                                                                              |
| AMMINISTRATORE \_ \_ DELL'ATTENDIBILITÀ DEI CRITERI                | Questo tipo di accesso è necessario per modificare le informazioni sul dominio dell'account o sul dominio primario.                                                                                                                                                                                                                                                                             |
| LIMITI \_ DI QUOTA PREDEFINITI DEL SET DI \_ \_ \_ CRITERI | Impostare le quote di sistema predefinite applicate agli account utente.                                                                                                                                                                                                                                                                                                   |
| CRITERIO \_ CREATE \_ SECRET              | Questo tipo di accesso è necessario per creare un nuovo oggetto Dati privati.                                                                                                                                                                                                                                                                                                    |
| ACCOUNT \_ DI CREAZIONE \_ CRITERI             | Questo tipo di accesso è necessario per creare un nuovo [**oggetto Account.**](account-object.md)                                                                                                                                                                                                                                                                               |
| REQUISITI DI \_ CONTROLLO DEL SET DI \_ \_ CRITERI    | Questo tipo di accesso è necessario per aggiornare i requisiti di controllo del sistema.                                                                                                                                                                                                                                                                                      |
| AMMINISTRATORE \_ DEL LOG DI CONTROLLO DEI \_ \_ CRITERI           | Questo tipo di accesso è necessario per modificare le caratteristiche del audit trail, ad esempio le dimensioni massime o il periodo di conservazione per i record di controllo o per cancellare il log.                                                                                                                                                                                               |
| INFORMAZIONI DI \_ CONTROLLO \_ VISUALIZZAZIONE \_ CRITERI    | Questo tipo di accesso è necessario per visualizzare audit trail informazioni sui requisiti di controllo.                                                                                                                                                                                                                                                                                  |
| AMMINISTRATORE \_ DEL SERVER DEI \_ CRITERI               | Questo tipo di accesso è necessario per modificare lo stato del server o le informazioni sul ruolo (master/replica). È anche necessario modificare l'origine della replica e le informazioni sul nome dell'account.                                                                                                                                                                                           |
| NOMI DI \_ RICERCA \_ DEI CRITERI               | Questo tipo di accesso è necessario per eseguire la conversione tra nomi e SID.                                                                                                                                                                                                                                                                                                    |
| PRIVILEGIO \_ DI CREAZIONE \_ CRITERI           | Non ancora supportato.                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a>Maschere di accesso generiche

[**L'oggetto**](policy-object.md) Policy pubblica i mapping seguenti da tipi di accesso generici a tipi di accesso specifici:

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a>Tipi di accesso standard

Questo oggetto non supporta il tipo di accesso standard SYNCHRONIZE (facoltativo). Sono supportati tutti i tipi di accesso necessari. La maschera di tutti i tipi di accesso supportati per questo tipo di oggetto è:

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 
