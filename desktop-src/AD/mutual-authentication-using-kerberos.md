---
title: Autenticazione reciproca tramite Kerberos
description: L'autenticazione reciproca è una funzionalità di sicurezza in cui un processo client deve dimostrare la propria identità a un servizio e il servizio deve dimostrare la propria identità al client, prima che il traffico dell'applicazione venga trasmesso tramite la connessione client/servizio.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, uso dell'autenticazione reciproca
- Active Directory, uso, sicurezza, autenticazione reciproca
- security AD
- security AD , autenticazione reciproca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e22a9f83712b15f22f9d9b05aee4219f3cbc892d88d0b44ba2d63fb9bbe2b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185951"
---
# <a name="mutual-authentication-using-kerberos"></a>Autenticazione reciproca tramite Kerberos

L'autenticazione reciproca è una funzionalità di sicurezza in cui un processo client deve dimostrare la propria identità a un servizio e il servizio deve dimostrare la propria identità al client, prima che il traffico dell'applicazione venga trasmesso tramite la connessione client/servizio.

Active Directory Domain Services e Windows supporto per i nomi dell'entità servizio (SPN), che sono un componente chiave nel meccanismo Kerberos tramite il quale un client autentica un servizio. Un nome SPN è un nome univoco che identifica un'istanza di un servizio ed è associato all'account di accesso con cui viene eseguita l'istanza del servizio. I componenti di un nome SPN sono tali che un client può comporre un nome SPN per un servizio senza l'account di accesso del servizio. In questo modo il client può richiedere al servizio di autenticare il proprio account anche se il client non ha il nome dell'account.

Questa sezione include una panoramica di:

-   Autenticazione reciproca tramite Kerberos.
-   Composizione di un nome SPN univoco.
-   Modalità di registrazione dei nomi SPN da parte di un programma di installazione del servizio nell'oggetto account associato a un'istanza del servizio.
-   Come un'applicazione client usa l'oggetto punto di connessione del servizio (SCP) di un'istanza del servizio in Active Directory Domain Services per recuperare i dati da cui comporre un nome SPN per il servizio.
-   Come un'applicazione client usa un nome SPN del servizio insieme all'interfaccia SSPI (Security Support Provider Interface) per autenticare il servizio.
-   Esempio di codice per un'Windows client/servizio Sockets che usa SCP e SSPI per eseguire l'autenticazione reciproca.
-   Esempio di codice per un client/servizio RPC che esegue l'autenticazione reciproca usando il servizio dei nomi RPC e l'autenticazione RPC.
-   Come un Windows registrazione e risoluzione socket (RnR) usa i nomi SPN per eseguire l'autenticazione reciproca.

In questa sezione viene illustrato l'Dominio di Active Directory per l'autenticazione reciproca, in particolare lo scopo dei punti di connessione del servizio e dei nomi delle entità servizio nell'autenticazione reciproca. Non si tratta di una discussione completa su come usare SSPI per l'autenticazione reciproca o sul supporto per l'autenticazione e la sicurezza disponibili per le applicazioni RPC e Windows Sockets.

Per altre informazioni, vedere:

-   [Pubblicazione con punti di connessione del servizio](publishing-with-service-connection-points.md)
-   [SSPI](/windows/desktop/SecAuthN/sspi)
-   [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [RPC](/windows/desktop/Rpc/rpc-start-page)

 

 