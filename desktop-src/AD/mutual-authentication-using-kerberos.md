---
title: Autenticazione reciproca tramite Kerberos
description: L'autenticazione reciproca è una funzionalità di sicurezza in cui un processo client deve dimostrare la propria identità a un servizio e il servizio deve dimostrare la propria identità al client, prima che il traffico dell'applicazione venga trasmesso attraverso la connessione client/servizio.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, uso dell'autenticazione reciproca
- Active Directory, utilizzo, sicurezza, autenticazione reciproca
- ANNUNCIO sulla sicurezza
- Active Directory di sicurezza, autenticazione reciproca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299566"
---
# <a name="mutual-authentication-using-kerberos"></a>Autenticazione reciproca tramite Kerberos

L'autenticazione reciproca è una funzionalità di sicurezza in cui un processo client deve dimostrare la propria identità a un servizio e il servizio deve dimostrare la propria identità al client, prima che il traffico dell'applicazione venga trasmesso attraverso la connessione client/servizio.

Active Directory Domain Services e Windows forniscono supporto per i nomi dell'entità servizio (SPN), che costituiscono un componente chiave del meccanismo Kerberos mediante il quale un client autentica un servizio. Un SPN è un nome univoco che identifica un'istanza di un servizio ed è associato all'account di accesso con cui viene eseguita l'istanza del servizio. I componenti di un nome SPN sono tali che un client può comporre un nome SPN per un servizio senza l'account di accesso del servizio. Ciò consente al client di richiedere al servizio di autenticare l'account anche se il client non ha il nome dell'account.

Questa sezione include una panoramica di:

-   Autenticazione reciproca tramite Kerberos.
-   Composizione di un nome SPN univoco.
-   Come un programma di installazione del servizio registra i nomi SPN nell'oggetto account associato a un'istanza del servizio.
-   Il modo in cui un'applicazione client utilizza l'oggetto punto di connessione del servizio (SCP) di un'istanza di servizio in Active Directory Domain Services per recuperare i dati da cui comporre un nome SPN per il servizio.
-   In che modo un'applicazione client utilizza un SPN del servizio in combinazione con Security Support Provider Interface (SSPI) per autenticare il servizio.
-   Esempio di codice per un'applicazione client/servizio Windows Sockets che utilizza SCP e SSPI per eseguire l'autenticazione reciproca.
-   Un esempio di codice per un client/servizio RPC che esegue l'autenticazione reciproca usando il servizio nome RPC e l'autenticazione RPC.
-   Il modo in cui un servizio di registrazione e risoluzione (RnR) di Windows Socket usa nomi SPN per eseguire l'autenticazione reciproca.

Questa sezione illustra l'uso di Dominio di Active Directory servizio per l'autenticazione reciproca, in particolare lo scopo dei punti di connessione del servizio e i nomi dell'entità servizio nell'autenticazione reciproca. Non è una spiegazione completa di come utilizzare SSPI per l'autenticazione reciproca o il supporto per l'autenticazione e la sicurezza disponibili per le applicazioni RPC e Windows Sockets.

Per altre informazioni, vedere:

-   [Pubblicazione con i punti di connessione del servizio](publishing-with-service-connection-points.md)
-   [SSPI](/windows/desktop/SecAuthN/sspi)
-   [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [RPC](/windows/desktop/Rpc/rpc-start-page)

 

 