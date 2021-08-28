---
description: L'utente inizia ad accedere alla rete digitando un nome di accesso e una password. Il client Kerberos nella workstation dell'utente converte la password in una chiave di crittografia e salva il risultato in una variabile di programma.
ms.assetid: fcb3b601-9953-474c-9a08-1fa25706f3d7
title: Scambio del servizio di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480370dd9fe5d7c5fc10e7979de9d4e7f67f99db3e517e1ec6520a3274ef23c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073291"
---
# <a name="authentication-service-exchange"></a>Scambio del servizio di autenticazione

L'utente inizia ad accedere alla rete digitando un nome di accesso e una password. Il client [*Kerberos*](/windows/desktop/SecGloss/k-gly) nella workstation dell'utente converte la password in una chiave di crittografia e salva il risultato in una variabile di programma.

Il client [](/windows/desktop/SecGloss/c-gly) richiede quindi le credenziali per il servizio di concessione ticket (TGS) del [*Centro distribuzione chiavi*](/windows/desktop/SecGloss/k-gly) (KDC) inviando al servizio di autenticazione del KDC un messaggio di tipo KRB \_ AS REQ (richiesta del servizio di autenticazione \_ Kerberos). La prima parte di questo messaggio identifica l'utente e il servizio TGS richiesto. La seconda parte di questo messaggio contiene dati di preautenticazione destinati a dimostrare che l'utente conosce la password. Si tratta semplicemente di un messaggio di autenticazione crittografato con la [*chiave master*](/windows/desktop/SecGloss/m-gly) derivata dalla password di accesso dell'utente.

Quando il KDC riceve KRB AS REQ, cerca l'utente nel database, ottiene la chiave master dell'utente associato, decrittografa i dati di preautenticazione e valuta il timestamp \_ \_ all'interno. Se il timestamp è valido, il KDC può essere certo che i dati di preautenticazione sono stati crittografati con la chiave master dell'utente e quindi che il client è originale.

Dopo che il KDC ha verificato l'identità dell'utente, crea credenziali che il client può presentare al TGS, come indicato di seguito:

1.  Il KDC inventa una chiave [*di sessione di accesso*](/windows/desktop/SecGloss/s-gly) e crittografa una copia con la chiave master dell'utente.
2.  Il KDC incorpora un'altra copia della chiave di sessione di accesso e dei dati di autorizzazione dell'utente in un ticket di concessione ticket (TGT) e crittografa il TGT con la chiave master del KDC.
3.  Il KDC invia queste credenziali al client rispondendo con un messaggio di tipo KRB \_ AS \_ REP (Kerberos Authentication Service Reply).
4.  Quando il client riceve la risposta, usa la chiave derivata dalla password dell'utente per decrittografare la nuova chiave di sessione di accesso.
5.  Il client archivia la nuova chiave nella cache dei ticket.
6.  Il client estrae il TGT dal messaggio e lo archivia anche nella cache dei ticket.

 

 
