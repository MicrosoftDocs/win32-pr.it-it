---
description: Dopo aver stabilito un ticket di concessione ticket (TGT) e una chiave di sessione per il client, il client può richiedere una chiave di sessione e un ticket separati per il servizio.
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: Scambio del servizio di concessione ticket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a691235b3e7f0faed68f38f0663c7792e381666f441399397f7e653bbb550080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786569"
---
# <a name="ticket-granting-service-exchange"></a>Scambio del servizio di concessione ticket

Dopo aver stabilito un ticket di concessione ticket (TGT) e una chiave di sessione per il client, il client può richiedere una chiave di sessione e un ticket separati per il servizio. [](../secgloss/s-gly.md)

**Per richiedere un ticket per un altro servizio**

1.  Il client Kerberos nella workstation [](../secgloss/c-gly.md) dell'utente richiede le credenziali per il servizio inviando, al [*Centro distribuzione chiavi*](../secgloss/k-gly.md) (KDC), un messaggio di tipo KRB \_ TGS \_ REQ (richiesta di servizio kerberos Ticket-Granting). Questo messaggio è costituito dall'identità del servizio per cui il client richiede le credenziali, da [](../secgloss/s-gly.md)un messaggio autenticatore crittografato con la nuova chiave di sessione di accesso dell'utente e dal TGT ottenuto dal servizio di autenticazione [Exchange](authentication-service-exchange.md).
2.  Quando il KDC riceve un TGS REQ KRB, il KDC decrittografa il TGT con la chiave privata ed estrae la chiave di sessione di accesso \_ \_ dell'utente.
3.  Il KDC usa la chiave [*di sessione di accesso*](../secgloss/s-gly.md) per decrittografare il messaggio dell'autenticatore dell'utente e valutarlo. Se l'autenticatore supera il test, il KDC estrae i dati di autorizzazione dell'utente dal TGT e inventa una chiave di sessione che l'utente deve condividere con il server richiesto.
4.  Il KDC crittografa una copia della chiave di sessione del servizio con la chiave di sessione di accesso dell'utente.
5.  Il KDC incorpora un'altra copia della chiave di sessione del servizio in un ticket, insieme ai dati di autorizzazione dell'utente, e crittografa il ticket con la [*chiave master del*](../secgloss/m-gly.md)server .
6.  Il KDC invia queste credenziali al client rispondendo con un messaggio di tipo KRB \_ TGS \_ REP (Kerberos Ticket-Granting Service Reply).
7.  Quando il client riceve la risposta, decrittografa la chiave di sessione del servizio con la chiave di sessione di accesso dell'utente e archivia la chiave di sessione del servizio nella relativa cache dei ticket.
8.  Il client estrae il ticket al server e lo archivia nella relativa cache dei ticket.

 

 
