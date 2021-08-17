---
description: Vengono illustrati i due tipi di credenziali con cui funziona API Gestione credenziali.
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: Tipi di credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d0e067b3918496310f3244153864abbf7548e5367569f4f2fbd06de40f207c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140934"
---
# <a name="kinds-of-credentials"></a>Tipi di credenziali

L'API Gestione credenziali funziona con due tipi di credenziali:

-   [Credenziali del dominio](#domain-credentials)
-   [Credenziali generiche](#generic-credentials)

## <a name="domain-credentials"></a>Credenziali del dominio

Le credenziali di dominio vengono usate dal sistema operativo e autenticate dall'autorità di sicurezza locale (LSA). In genere, le credenziali di dominio vengono stabilite per un utente quando un pacchetto di sicurezza registrato, ad esempio il protocollo Kerberos, autentica i dati di accesso forniti dall'utente. Le credenziali di accesso vengono memorizzate nella cache dal sistema operativo in modo che un accesso Single Sign-On conservi l'accesso a molte risorse diverse. Ad esempio, le connessioni di rete possono verificarsi in modo trasparente e l'accesso agli oggetti di sistema protetti può essere concesso in base alle credenziali di dominio memorizzate nella cache dell'utente.

Le funzioni di gestione delle credenziali forniscono un meccanismo che consente alle applicazioni di richiedere le credenziali di dominio a un utente dopo l'accesso dell'utente e di fare in modo che il sistema operativo asezioni le informazioni fornite dall'utente.

La parte segreta delle credenziali di dominio, la password, è protetta dal sistema operativo. Solo il codice in esecuzione in-process con LSA può leggere e scrivere le credenziali di dominio. Le applicazioni sono limitate alla scrittura di credenziali di dominio.

Windows supporta l'uso esteso delle credenziali smart card e del certificato. Per garantire la sicurezza, l'API Gestione credenziali non archivia mai smart card PIN nel computer.

## <a name="generic-credentials"></a>Credenziali generiche

Le credenziali generiche vengono definite e autenticate dalle applicazioni che gestiscono direttamente l'autorizzazione e la sicurezza anziché delegare queste attività al sistema operativo. Ad esempio, un'applicazione può richiedere agli utenti di immettere un nome utente e una password forniti dall'applicazione o di produrre un certificato [*per*](../secgloss/c-gly.md) accedere a un sito Web.

Le applicazioni usano le funzioni di gestione delle credenziali per richiedere agli utenti informazioni generiche sulle credenziali definite dall'applicazione, ad esempio nome utente, certificato, smart card o password. Le informazioni immesse dall'utente vengono restituite all'applicazione per l'autenticazione.

Gestione credenziali offre la gestione della cache personalizzabile e l'archiviazione a lungo termine per le credenziali generiche. Le credenziali generiche possono essere lette e scritte dai processi utente.

 

 
