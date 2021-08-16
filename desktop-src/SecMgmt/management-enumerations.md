---
description: Elenca le enumerazioni utilizzate dalle funzioni di gestione dei criteri LSA.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Enumerazioni di gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf87e6c41cb3e687a8927c294fe3bc1433a294aaf48991310b1c230f4741f299
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894457"
---
# <a name="security-management-enumerations"></a>Enumerazioni di gestione della sicurezza

Le enumerazioni di gestione della sicurezza includono quanto segue:

-   [Enumerazioni di criteri LSA](#lsa-policy-enumerations)
-   [Enumerazioni più sicure](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a>Enumerazioni di criteri LSA

I tipi di enumerazione seguenti vengono usati dalle funzioni di gestione dei criteri LSA.



| Enumerazione                                                                               | Descrizione                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO \_ DI EVENTO DI CONTROLLO DEI \_ \_ CRITERI**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | Definisce i tipi di eventi che il sistema può controllare.                                                                                     |
| [**CLASSE DI \_ INFORMAZIONI \_ SUI CRITERI**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | Definisce i tipi di informazioni che è possibile impostare o su cui è possibile eseguire query per un [**oggetto**](policy-object.md) Criteri.                             |
| [**RUOLO DEL SERVER POLICY \_ LSA \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | Indicare il ruolo di un server LSA.                                                                                                   |
| [**CLASSE DI \_ INFORMAZIONI SULLE NOTIFICHE DEI \_ \_ CRITERI**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | Definisce i tipi di informazioni sui criteri e le informazioni sul dominio dei criteri per cui l'applicazione può richiedere la notifica delle modifiche. |
| [**STATO \_ DI \_ ABILITAZIONE SERVER \_ CRITERI**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | Rappresenta lo stato del server LSA, indipendentemente dal fatto che sia abilitato o disabilitato.                                                   |
| [**CLASSE \_ DI INFORMAZIONI \_ ATTENDIBILI**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | Definisce i tipi di informazioni che è possibile impostare o su cui è possibile eseguire query per un dominio trusted.                                                     |



 

## <a name="safer-enumerations"></a>Enumerazioni più sicure

[Safer](safer.md) usa i tipi enumerati seguenti.



| Nome                                                               | Descrizione                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPI \_ DI IDENTIFICAZIONE PIÙ \_ SICURI**](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | Tipo di enumerazione che definisce i tipi possibili di strutture di regole di identificazione identificabili dalla [**struttura SAFER \_ IDENTIFICATION \_ HEADER.**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) |
| [**CLASSE SAFER \_ OBJECT \_ INFO \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | Tipo di enumerazione che definisce il tipo di informazioni richieste su un oggetto Safer.                                                                                                            |
| [**CLASSE \_ DI INFORMAZIONI SUI CRITERI PIÙ \_ \_ SICURI**](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | Tipo di enumerazione che definisce i modi in cui è possibile eseguire query su un criterio.                                                                                                                         |



 

 

 



