---
title: attributo ms-DS-REPL-Authentication-Mode
description: L'attributo ms-DS-REPL-Authentication-Mode viene usato per specificare il metodo di autenticazione usato per autenticare i partner di replica.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-REPL-Authentication-Mode
- attributo msDS-ReplAuthenticationMode-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b88c7e3223b946b56962b710b036ee6e0c36dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480360"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a>attributo ms-DS-REPL-Authentication-Mode

L'attributo **ms-DS-REPL-Authentication-Mode** viene usato per specificare il metodo di autenticazione usato per autenticare i partner di replica. Questo attributo si applica alla partizione di configurazione di un'istanza ADAM.

Di seguito sono riportati i valori possibili per questo attributo.

| Valore        | Metodo di autenticazione                          | Descrizione                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0<br/> | Negoziata pass-through<br/>             | Tutte le istanze di ADAM nel set di configurazione utilizzano un nome account e una password identici a quelli dell'account del servizio ADAM.<br/>                                                 |
| 1<br/> | Negoziata<br/>                          | Viene in primo luogo eseguita l'autenticazione Kerberos mediante SPN. Se l'autenticazione Kerberos non riesce, viene eseguita l'autenticazione NTLM. Se NTLM ha esito negativo, le istanze di ADAM non vengono replicate.<br/> |
| 2<br/> | Autenticazione manuale con Kerberos<br/> | È necessaria l'autenticazione Kerberos, tramite i nomi principali di servizio (SPN). Se l'autenticazione Kerberos ha esito negativo, le istanze di ADAM non vengono replicate.<br/>                |



 

La tabella seguente contiene gli identificatori programmatici per i valori di questo attributo.

| Valore        | Identificatore (da NTDSAPI. h)                                               |
|--------------|---------------------------------------------------------------------------|
| 0<br/> | **il \_ \_ pass- \_ \_ through Negotiate \_ \_ in modalità di autenticazione Adam repl**<br/> |
| 1<br/> | **\_ \_ negoziazione modalità di autenticazione Adam REPL \_ \_**<br/>                |
| 2<br/> | **ADAM \_ REPL \_ modalità di autenticazione \_ \_ reciproca-autenticazione \_ \_ obbligatoria**<br/>   |



 



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-REPL-Authentication-Mode       |
| LDAP-Display-Name | msDS-ReplAuthenticationMode          |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1861              |
| System-ID-GUID    | 6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50 |
| Sintassi            | [**Enumerazione**](s-enumeration.md) |



## <a name="implementations"></a>Implementazioni

-   [**ADAM**](#adam)

## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|-----------------------------------------------------|
| ID collegamento                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| È a valore singolo       | Vero                                                |
| Indicizzato             | Falso                                               |
| Nel catalogo globale      | Falso                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Classi utilizzate in        | [**Configurazione**](c-configuration.md)<br/> |



 

 





