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
# <a name="ticket-granting-service-exchange"></a><span data-ttu-id="d93a4-103">Scambio del servizio di concessione ticket</span><span class="sxs-lookup"><span data-stu-id="d93a4-103">Ticket-Granting Service Exchange</span></span>

<span data-ttu-id="d93a4-104">Dopo aver stabilito un ticket di concessione ticket (TGT) e una [*chiave di sessione*](../secgloss/s-gly.md) per il client, il client può richiedere una chiave di sessione separata e un ticket per il servizio.</span><span class="sxs-lookup"><span data-stu-id="d93a4-104">After a ticket-granting ticket (TGT) and [*session key*](../secgloss/s-gly.md) have been established for the client, the client can request a separate session key and ticket for the service.</span></span>

<span data-ttu-id="d93a4-105">**Per richiedere un ticket per un altro servizio**</span><span class="sxs-lookup"><span data-stu-id="d93a4-105">**To request a ticket for another service**</span></span>

1.  <span data-ttu-id="d93a4-106">Il client Kerberos nella workstation dell'utente richiede le [*credenziali*](../secgloss/c-gly.md) per il servizio inviando al [*centro distribuzione chiavi*](../secgloss/k-gly.md) (KDC) un messaggio di tipo KRB \_ TGS \_ req (richiesta di servizio Ticket-Granting Kerberos).</span><span class="sxs-lookup"><span data-stu-id="d93a4-106">The Kerberos client on the user's workstation requests [*credentials*](../secgloss/c-gly.md) for the service by sending, to the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC), a message of type KRB\_TGS\_REQ (Kerberos Ticket-Granting Service Request).</span></span> <span data-ttu-id="d93a4-107">Questo messaggio è costituito dall'identità del servizio per il quale il client richiede le credenziali, un messaggio di autenticazione crittografato con la nuova chiave della [*sessione*](../secgloss/s-gly.md)di accesso dell'utente e il TGT ottenuto dallo [scambio del servizio di autenticazione](authentication-service-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="d93a4-107">This message consists of the identity of the service for which the client is requesting credentials, an authenticator message encrypted with the user's new logon [*session key*](../secgloss/s-gly.md), and the TGT obtained from the [Authentication Service Exchange](authentication-service-exchange.md).</span></span>
2.  <span data-ttu-id="d93a4-108">Quando il KDC riceve un \_ req KRB TGS \_ , il KDC DECRITTOGRAFA il TGT con la relativa chiave privata ed estrae la chiave della sessione di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d93a4-108">When the KDC receives a KRB\_TGS\_REQ, the KDC decrypts the TGT with its secret key and extracts the user's logon session key.</span></span>
3.  <span data-ttu-id="d93a4-109">Il KDC usa la [*chiave della sessione*](../secgloss/s-gly.md) di accesso per decrittografare il messaggio di autenticazione dell'utente e lo valuta.</span><span class="sxs-lookup"><span data-stu-id="d93a4-109">The KDC uses the logon [*session key*](../secgloss/s-gly.md) to decrypt the user's authenticator message and evaluates it.</span></span> <span data-ttu-id="d93a4-110">Se l'autenticatore supera il test, il KDC estrae i dati di autorizzazione dell'utente dal TGT e inventa una chiave di sessione per l'utente da condividere con il server richiesto.</span><span class="sxs-lookup"><span data-stu-id="d93a4-110">If the authenticator passes the test, the KDC extracts the user's authorization data from the TGT and invents a session key for the user to share with the requested server.</span></span>
4.  <span data-ttu-id="d93a4-111">Il KDC crittografa una copia della chiave della sessione del servizio con la chiave della sessione di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d93a4-111">The KDC encrypts one copy of the service session key with the user's logon session key.</span></span>
5.  <span data-ttu-id="d93a4-112">Il KDC incorpora un'altra copia della chiave della sessione del servizio in un ticket, insieme ai dati di autorizzazione dell'utente, e crittografa il ticket con la [*chiave master*](../secgloss/m-gly.md)del server.</span><span class="sxs-lookup"><span data-stu-id="d93a4-112">The KDC embeds another copy of the service session key in a ticket, along with the user's authorization data, and encrypts the ticket with the server's [*master key*](../secgloss/m-gly.md).</span></span>
6.  <span data-ttu-id="d93a4-113">Il KDC invia le credenziali al client rispondendo con un messaggio di tipo KRB \_ TGS \_ Rep (Kerberos Ticket-Granting servizio di risposta).</span><span class="sxs-lookup"><span data-stu-id="d93a4-113">The KDC sends these credentials back to the client by replying with a message of type KRB\_TGS\_REP (Kerberos Ticket-Granting Service Reply).</span></span>
7.  <span data-ttu-id="d93a4-114">Quando il client riceve la risposta, decrittografa la chiave della sessione del servizio con la chiave della sessione di accesso dell'utente e archivia la chiave della sessione del servizio nella cache dei ticket.</span><span class="sxs-lookup"><span data-stu-id="d93a4-114">When the client receives the reply, it decrypts the service session key with the user's logon session key and stores the service session key in its ticket cache.</span></span>
8.  <span data-ttu-id="d93a4-115">Il client estrae il ticket al server e lo archivia nella cache dei ticket.</span><span class="sxs-lookup"><span data-stu-id="d93a4-115">The client extracts the ticket to the server and stores that in its ticket cache.</span></span>

 

 
