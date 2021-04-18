---
description: L'utente inizia ad accedere alla rete digitando un nome di accesso e una password. Il client Kerberos nella workstation dell'utente converte la password in una chiave di crittografia e salva il risultato in una variabile di programma.
ms.assetid: fcb3b601-9953-474c-9a08-1fa25706f3d7
title: Scambio del servizio di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c14121ed33ae0ac169c590b03dfb0b395306d11f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313752"
---
# <a name="authentication-service-exchange"></a>Scambio del servizio di autenticazione

L'utente inizia ad accedere alla rete digitando un nome di accesso e una password. Il client [*Kerberos*](/windows/desktop/SecGloss/k-gly) nella workstation dell'utente converte la password in una chiave di crittografia e salva il risultato in una variabile di programma.

Il client richiede quindi le [*credenziali*](/windows/desktop/SecGloss/c-gly) per il servizio di concessione ticket (TGS) del [*centro distribuzione chiavi*](/windows/desktop/SecGloss/k-gly) (KDC) inviando il servizio di autenticazione del KDC un messaggio di tipo KRB \_ come \_ req (richiesta del servizio di autenticazione Kerberos). La prima parte di questo messaggio identifica l'utente e il servizio TGS richiesto. La seconda parte di questo messaggio contiene i dati di preautenticazione destinati a dimostrare che l'utente conosce la password. Si tratta semplicemente di un messaggio di autenticazione crittografato con la [*chiave master*](/windows/desktop/SecGloss/m-gly) derivata dalla password di accesso dell'utente.

Quando il KDC riceve KRB \_ come \_ req, Cerca l'utente nel database, ottiene la chiave master dell'utente associato, decrittografa i dati di preautenticazione e valuta il timestamp all'interno. Se il timestamp è valido, è possibile garantire che i dati di preautenticazione siano stati crittografati con la chiave master dell'utente e che quindi il client sia autentico.

Una volta verificata l'identità dell'utente, il KDC crea le credenziali che il client può presentare al TGS, come indicato di seguito:

1.  Il KDC inventa una chiave della [*sessione*](/windows/desktop/SecGloss/s-gly) di accesso e crittografa una copia con la chiave master dell'utente.
2.  Il KDC incorpora un'altra copia della chiave della sessione di accesso e i dati di autorizzazione dell'utente in un ticket di concessione ticket (TGT) e crittografa il TGT con la chiave master del KDC.
3.  Il KDC invia le credenziali al client rispondendo con un messaggio di tipo KRB \_ come \_ Rep (risposta al servizio di autenticazione Kerberos).
4.  Quando il client riceve la risposta, usa la chiave derivata dalla password dell'utente per decrittografare la nuova chiave della sessione di accesso.
5.  Il client archivia la nuova chiave nella relativa cache di ticket.
6.  Il client estrae il TGT dal messaggio e lo archivia anche nella cache dei ticket.

 

 
