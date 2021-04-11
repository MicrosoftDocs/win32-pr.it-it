---
description: Per l'autenticazione HTTP con Microsoft Digest sono necessari tre buffer di input per generare una risposta di verifica. Nella tabella seguente vengono riepilogati i buffer.
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: Buffer di input per la risposta di verifica del digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128306"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a>Buffer di input per la risposta di verifica del digest

Per l'autenticazione HTTP con Microsoft Digest sono necessari tre buffer di input per generare una risposta di verifica. Nella tabella seguente vengono riepilogati i buffer.



| Numero buffer | Contiene                                                                                                                                             | Tipo di buffer                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| 0             | Richiesta di verifica ricevuta dal server                                                                                                                   | \_token SECBUFFER                                            |
| 1             | Metodo HTTP                                                                                                                                          | \_parametri SECBUFFER                                           |
| 2             | H (entità)                                                                                                                                            | \_parametri SECBUFFER                                           |
| 3             | [*Nome dell'entità servizio*](../secgloss/s-gly.md) (SPN) del server di destinazione. | **SECBUFFER \_ \_host di destinazione** \| **SECBUFFER \_ ReadOnly**      |
| 4             | Valori dei token delle associazioni di canale                                                                                                                        | **SECBUFFER \_ \_associazioni di canale** \| **SECBUFFER \_ ReadOnly** |



 

Il buffer zero contiene la richiesta digest ricevuta dal server in risposta alla richiesta iniziale di una risorsa protetta da Access.

Il buffer 1 contiene la rappresentazione di stringa del metodo, ad esempio "GET" o "POST". Il metodo viene usato nel calcolo di a2, come descritto in [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).

Buffer 2 è l'hash [*MD5*](../secgloss/m-gly.md) del corpo entità del messaggio, come descritto nella RFC 2617.

Il buffer 3 contiene il nome SPN del server di destinazione in formato UTF-8 quando il digest viene utilizzato con le associazioni di canale.

Il buffer 4 contiene il valore del token di associazione del canale quando il digest viene utilizzato con le associazioni di canale.

## <a name="input-buffers-for-sasl"></a>Buffer di input per SASL

Specificare solo il buffer zero. Per la compatibilità con altri SSP, è possibile chiamare [**InitializeSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) senza una richiesta server valida. In questo caso il parametro *Pinput* deve essere impostato su **null**.

 

 
