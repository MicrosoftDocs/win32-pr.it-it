---
description: Elenca e descrive i tipi di accesso dell'oggetto criteri.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Diritti di accesso agli oggetti Criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5c762955a4c53015241086b2249c5edbc4f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306434"
---
# <a name="policy-object-access-rights"></a>Diritti di accesso agli oggetti Criteri

L'oggetto [**policy**](policy-object.md) dispone dei seguenti tipi di accesso specifici per gli oggetti:



| Tipo di accesso                         | Descrizione                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ informazioni locali visualizzazione \_ criteri    | Questo tipo di accesso è necessario per leggere le varie informazioni sui criteri di sicurezza del sistema di destinazione. Sono incluse la quota predefinita, il controllo, lo stato del server e le informazioni sui ruoli e le informazioni sull'attendibilità. Questo tipo di accesso è necessario anche per enumerare domini, account e [*privilegi*](/windows/desktop/SecGloss/p-gly)attendibili. |
| \_ottenere \_ informazioni private \_ sui criteri   | Questo tipo di accesso è necessario per visualizzare informazioni riservate, ad esempio i nomi degli account stabiliti per le relazioni di dominio trusted.                                                                                                                                                                                                                              |
| \_amministratore attendibilità criteri \_                | Questo tipo di accesso è necessario per modificare le informazioni sul dominio dell'account o sul dominio primario.                                                                                                                                                                                                                                                                             |
| \_limiti di \_ \_ quota predefiniti impostati dal \_ criterio | Impostare le quote di sistema predefinite che vengono applicate agli account utente.                                                                                                                                                                                                                                                                                                   |
| creazione di un \_ \_ segreto criterio              | Questo tipo di accesso è necessario per creare un nuovo oggetto dati privato.                                                                                                                                                                                                                                                                                                    |
| \_account creazione \_ criteri             | Questo tipo di accesso è necessario per creare un nuovo oggetto [**account**](account-object.md) .                                                                                                                                                                                                                                                                               |
| \_requisiti di \_ controllo per set di criteri \_    | Questo tipo di accesso è necessario per aggiornare i requisiti di controllo del sistema.                                                                                                                                                                                                                                                                                      |
| \_ \_ Amministrazione log di controllo dei criteri \_           | Questo tipo di accesso è necessario per modificare le caratteristiche del audit trail, ad esempio le dimensioni massime o il periodo di conservazione per i record di controllo, oppure per cancellare il log.                                                                                                                                                                                               |
| \_informazioni di \_ controllo \_ visualizzazione criteri    | Questo tipo di accesso è necessario per visualizzare le informazioni sui requisiti di audit trail o controllo.                                                                                                                                                                                                                                                                                  |
| \_amministratore server dei criteri \_               | Questo tipo di accesso è necessario per modificare le informazioni sullo stato del server o sul ruolo (Master/replica). È anche necessario modificare le informazioni relative all'origine e al nome dell'account di replica.                                                                                                                                                                                           |
| \_nomi di ricerca criteri \_               | Questo tipo di accesso è necessario per la conversione tra nomi e SID.                                                                                                                                                                                                                                                                                                    |
| \_privilegio Creazione \_ criteri           | Non ancora supportato.                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a>Maschere di accesso generico

L'oggetto [**policy**](policy-object.md) pubblica i mapping seguenti dai tipi di accesso generici ai tipi di accesso specifici:

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

Questo oggetto non supporta il tipo di accesso standard (facoltativo) SYNCHRONIZE. Sono supportati tutti i tipi di accesso necessari. La maschera di tutti i tipi di accesso supportati per questo tipo di oggetto è:

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

 

 
