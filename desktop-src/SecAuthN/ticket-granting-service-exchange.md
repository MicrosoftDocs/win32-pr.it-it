---
description: Dopo aver stabilito un ticket di concessione ticket (TGT) e una chiave di sessione per il client, il client può richiedere una chiave di sessione separata e un ticket per il servizio.
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: Scambio del servizio di concessione ticket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b227ee551d762abd145ca56c6cced110b6a2dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309985"
---
# <a name="ticket-granting-service-exchange"></a>Scambio del servizio di concessione ticket

Dopo aver stabilito un ticket di concessione ticket (TGT) e una [*chiave di sessione*](../secgloss/s-gly.md) per il client, il client può richiedere una chiave di sessione separata e un ticket per il servizio.

**Per richiedere un ticket per un altro servizio**

1.  Il client Kerberos nella workstation dell'utente richiede le [*credenziali*](../secgloss/c-gly.md) per il servizio inviando al [*centro distribuzione chiavi*](../secgloss/k-gly.md) (KDC) un messaggio di tipo KRB \_ TGS \_ req (richiesta di servizio Ticket-Granting Kerberos). Questo messaggio è costituito dall'identità del servizio per il quale il client richiede le credenziali, un messaggio di autenticazione crittografato con la nuova chiave della [*sessione*](../secgloss/s-gly.md)di accesso dell'utente e il TGT ottenuto dallo [scambio del servizio di autenticazione](authentication-service-exchange.md).
2.  Quando il KDC riceve un \_ req KRB TGS \_ , il KDC DECRITTOGRAFA il TGT con la relativa chiave privata ed estrae la chiave della sessione di accesso dell'utente.
3.  Il KDC usa la [*chiave della sessione*](../secgloss/s-gly.md) di accesso per decrittografare il messaggio di autenticazione dell'utente e lo valuta. Se l'autenticatore supera il test, il KDC estrae i dati di autorizzazione dell'utente dal TGT e inventa una chiave di sessione per l'utente da condividere con il server richiesto.
4.  Il KDC crittografa una copia della chiave della sessione del servizio con la chiave della sessione di accesso dell'utente.
5.  Il KDC incorpora un'altra copia della chiave della sessione del servizio in un ticket, insieme ai dati di autorizzazione dell'utente, e crittografa il ticket con la [*chiave master*](../secgloss/m-gly.md)del server.
6.  Il KDC invia le credenziali al client rispondendo con un messaggio di tipo KRB \_ TGS \_ Rep (Kerberos Ticket-Granting servizio di risposta).
7.  Quando il client riceve la risposta, decrittografa la chiave della sessione del servizio con la chiave della sessione di accesso dell'utente e archivia la chiave della sessione del servizio nella cache dei ticket.
8.  Il client estrae il ticket al server e lo archivia nella cache dei ticket.

 

 
