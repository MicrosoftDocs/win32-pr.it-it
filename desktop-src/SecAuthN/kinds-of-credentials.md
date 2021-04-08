---
description: Vengono illustrati i due tipi di credenziali con cui funziona l'API di gestione delle credenziali.
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: Tipi di credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30968484b2cfc89b9238f624d9299fb75c72bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967671"
---
# <a name="kinds-of-credentials"></a>Tipi di credenziali

L'API di gestione delle credenziali funziona con due tipi di credenziali:

-   [Credenziali del dominio](#domain-credentials)
-   [Credenziali generiche](#generic-credentials)

## <a name="domain-credentials"></a>Credenziali del dominio

Le credenziali del dominio vengono utilizzate dal sistema operativo e autenticate dall'autorità di sicurezza locale (LSA). In genere, le credenziali di dominio vengono stabilite per un utente quando un pacchetto di sicurezza registrato, ad esempio il protocollo Kerberos, autentica i dati di accesso forniti dall'utente. Le credenziali di accesso vengono memorizzate nella cache dal sistema operativo in modo che un Single Sign-On fornisca all'utente l'accesso a molte risorse diverse. Ad esempio, le connessioni di rete possono essere eseguite in modo trasparente e l'accesso agli oggetti di sistema protetti può essere concesso in base alle credenziali di dominio memorizzate nella cache dell'utente.

Le funzioni di gestione delle credenziali forniscono un meccanismo che consente alle applicazioni di richiedere un utente per le credenziali di dominio dopo l'accesso dell'utente e per fare in modo che il sistema operativo autentichi le informazioni fornite dall'utente.

La parte segreta delle credenziali di dominio, ovvero la password, è protetta dal sistema operativo. Solo il codice eseguito in-process con LSA può leggere e scrivere le credenziali di dominio. Le applicazioni sono limitate alla scrittura di credenziali di dominio.

Windows supporta l'utilizzo espanso di smart card e credenziali del certificato. Per garantire la sicurezza, l'API di gestione delle credenziali non archivia mai il PIN della smart card nel computer.

## <a name="generic-credentials"></a>Credenziali generiche

Le credenziali generiche sono definite e autenticate da applicazioni che gestiscono direttamente l'autorizzazione e la sicurezza anziché delegare queste attività al sistema operativo. Ad esempio, un'applicazione può richiedere agli utenti di immettere un nome utente e una password forniti dall'applicazione o di produrre un [*certificato*](../secgloss/c-gly.md) per accedere a un sito Web.

Le applicazioni utilizzano le funzioni di gestione delle credenziali per richiedere agli utenti informazioni sulle credenziali definite dall'applicazione, generiche, ad esempio nome utente, certificato, smart card o password. Le informazioni immesse dall'utente vengono restituite all'applicazione per l'autenticazione.

Gestione delle credenziali offre la gestione della cache personalizzabile e l'archiviazione a lungo termine per le credenziali generiche. Le credenziali generiche possono essere lette e scritte dai processi utente.

 

 
