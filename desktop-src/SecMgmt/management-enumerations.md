---
description: Elenca le enumerazioni utilizzate dalle funzioni di gestione dei criteri LSA.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Enumerazioni di gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bec2cdd731e2a3befe75e543f692d93bc5d9ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231697"
---
# <a name="security-management-enumerations"></a>Enumerazioni di gestione della sicurezza

Di seguito sono riportate le enumerazioni di gestione della sicurezza:

-   [Enumerazioni dei criteri LSA](#lsa-policy-enumerations)
-   [Enumerazioni più sicure](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a>Enumerazioni dei criteri LSA

I tipi di enumerazione seguenti vengono utilizzati dalle funzioni di gestione dei criteri LSA.



| Enumerazione                                                                               | Descrizione                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo di \_ evento di controllo dei criteri \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | Definisce i tipi di eventi che il sistema è in grado di controllare.                                                                                     |
| [**\_classe di informazioni sui criteri \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | Definisce i tipi di informazioni che è possibile impostare o sottoporre a query per un oggetto [**criteri**](policy-object.md) .                             |
| [**\_ruolo del \_ server \_ LSA del criterio**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | Indica il ruolo di un server LSA.                                                                                                   |
| [**\_classe di \_ informazioni di notifica dei criteri \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | Definisce i tipi di informazioni sui criteri e informazioni sul dominio dei criteri per cui l'applicazione può richiedere la notifica delle modifiche. |
| [**\_stato di \_ Abilitazione del server dei criteri \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | Rappresenta lo stato del server LSA, ovvero se è abilitato o disabilitato.                                                   |
| [**\_classe di informazioni attendibili \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | Definisce i tipi di informazioni che è possibile impostare o sottoporre a query per un dominio trusted.                                                     |



 

## <a name="safer-enumerations"></a>Enumerazioni più sicure

[Safer](safer.md) utilizza i seguenti tipi enumerati.



| Nome                                                               | Descrizione                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipi di identificazione più sicuri \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | Tipo di enumerazione che definisce i possibili tipi di strutture della regola di identificazione che possono essere identificati dalla struttura dell' [**\_ \_ intestazione di identificazione più sicura**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) . |
| [**\_ \_ classe informazioni sugli oggetti più sicure \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | Tipo di enumerazione che definisce il tipo di informazioni richieste su un oggetto più sicuro.                                                                                                            |
| [**\_ \_ classe informazioni dei criteri più sicure \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | Tipo di enumerazione che definisce i modi in cui è possibile eseguire una query su un criterio.                                                                                                                         |



 

 

 



