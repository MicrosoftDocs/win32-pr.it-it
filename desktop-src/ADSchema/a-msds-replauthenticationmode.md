---
title: Attributo ms-DS-Repl-Authentication-Mode
description: L'attributo ms-DS-Repl-Authentication-Mode viene usato per specificare il metodo di autenticazione usato per autenticare i partner di replica.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-Repl-Authentication-Mode
- Schema AD dell'attributo msDS-ReplAuthenticationMode
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff624a9b7a1d1f678c748f79d3193b0b4b287026de1a669896c3e25d69f27ab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803541"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a>Attributo ms-DS-Repl-Authentication-Mode

**L'attributo ms-DS-Repl-Authentication-Mode** viene usato per specificare il metodo di autenticazione usato per autenticare i partner di replica. Questo attributo si applica alla partizione di configurazione di un'istanza di ADAM.

I valori seguenti sono i valori possibili per questo attributo.

| Valore        | Metodo di autenticazione                          | Descrizione                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0<br/> | Negoziata pass-through<br/>             | Tutte le istanze ADAM nel set di configurazione usano un nome account e una password identici come account del servizio ADAM.<br/>                                                 |
| 1<br/> | Negoziata<br/>                          | Viene in primo luogo eseguita l'autenticazione Kerberos mediante SPN. Se l'autenticazione Kerberos non riesce, viene eseguita l'autenticazione NTLM. Se NTLM ha esito negativo, le istanze ADAM non verranno replicate.<br/> |
| 2<br/> | Autenticazione manuale con Kerberos<br/> | È necessaria l'autenticazione Kerberos, tramite i nomi principali di servizio (SPN). Se l'autenticazione Kerberos non riesce, le istanze ADAM non verranno replicate.<br/>                |



 

La tabella seguente contiene gli identificatori a livello di codice per i valori di questo attributo.

| Valore        | Identificatore (da Ntdsapi.h)                                               |
|--------------|---------------------------------------------------------------------------|
| 0<br/> | **MODALITÀ DI AUTENTICAZIONE ADAM \_ REPL \_ NEGOTIATE PASS \_ \_ \_ \_ THROUGH**<br/> |
| 1<br/> | **ADAM \_ REPL \_ AUTHENTICATION \_ MODE \_ NEGOTIATE**<br/>                |
| 2<br/> | **È \_ NECESSARIA \_ L'AUTENTICAZIONE \_ RECIPROCA IN \_ MODALITÀ \_ \_ DI AUTENTICAZIONE ADAM REPL**<br/>   |



 



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-Repl-Authentication-Mode       |
| Ldap-Display-Name | msDS-ReplAuthenticationMode          |
| Dimensione              | \-                                   |
| Privilegio di aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1861              |
| System-Id-Guid    | 6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50 |
| Sintassi            | [**Enumerazione**](s-enumeration.md) |



## <a name="implementations"></a>Implementazioni

-   [**Adam**](#adam)

## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|-----------------------------------------------------|
| ID collegamento                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| Is-Single-Valued       | Vero                                                |
| Indicizzato             | Falso                                               |
| Nel catalogo globale      | Falso                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Classi usate in        | [**Configurazione**](c-configuration.md)<br/> |



 

 





