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
# <a name="kinds-of-credentials"></a><span data-ttu-id="1f9e8-103">Tipi di credenziali</span><span class="sxs-lookup"><span data-stu-id="1f9e8-103">Kinds of Credentials</span></span>

<span data-ttu-id="1f9e8-104">L'API di gestione delle credenziali funziona con due tipi di credenziali:</span><span class="sxs-lookup"><span data-stu-id="1f9e8-104">The Credentials Management API works with two kinds of credentials:</span></span>

-   [<span data-ttu-id="1f9e8-105">Credenziali del dominio</span><span class="sxs-lookup"><span data-stu-id="1f9e8-105">Domain Credentials</span></span>](#domain-credentials)
-   [<span data-ttu-id="1f9e8-106">Credenziali generiche</span><span class="sxs-lookup"><span data-stu-id="1f9e8-106">Generic Credentials</span></span>](#generic-credentials)

## <a name="domain-credentials"></a><span data-ttu-id="1f9e8-107">Credenziali del dominio</span><span class="sxs-lookup"><span data-stu-id="1f9e8-107">Domain Credentials</span></span>

<span data-ttu-id="1f9e8-108">Le credenziali del dominio vengono utilizzate dal sistema operativo e autenticate dall'autorità di sicurezza locale (LSA).</span><span class="sxs-lookup"><span data-stu-id="1f9e8-108">Domain credentials are used by the operating system and authenticated by the Local Security Authority (LSA).</span></span> <span data-ttu-id="1f9e8-109">In genere, le credenziali di dominio vengono stabilite per un utente quando un pacchetto di sicurezza registrato, ad esempio il protocollo Kerberos, autentica i dati di accesso forniti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-109">Typically, domain credentials are established for a user when a registered security package, such as the Kerberos protocol, authenticates logon data that is provided by the user.</span></span> <span data-ttu-id="1f9e8-110">Le credenziali di accesso vengono memorizzate nella cache dal sistema operativo in modo che un Single Sign-On fornisca all'utente l'accesso a molte risorse diverse.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-110">The logon credentials are cached by the operating system so that a single sign-on gives the user access to many different resources.</span></span> <span data-ttu-id="1f9e8-111">Ad esempio, le connessioni di rete possono essere eseguite in modo trasparente e l'accesso agli oggetti di sistema protetti può essere concesso in base alle credenziali di dominio memorizzate nella cache dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-111">For example, network connections can occur transparently, and access to protected system objects can be granted based on the user's cached domain credentials.</span></span>

<span data-ttu-id="1f9e8-112">Le funzioni di gestione delle credenziali forniscono un meccanismo che consente alle applicazioni di richiedere un utente per le credenziali di dominio dopo l'accesso dell'utente e per fare in modo che il sistema operativo autentichi le informazioni fornite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-112">Credentials Management functions provide a mechanism for applications to prompt a user for domain credentials after the user logs on, and to have the operating system authenticate the information that is provided by the user.</span></span>

<span data-ttu-id="1f9e8-113">La parte segreta delle credenziali di dominio, ovvero la password, è protetta dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-113">The secret part of domain credentials, the password, is protected by the operating system.</span></span> <span data-ttu-id="1f9e8-114">Solo il codice eseguito in-process con LSA può leggere e scrivere le credenziali di dominio.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-114">Only code running in-process with the LSA can read and write domain credentials.</span></span> <span data-ttu-id="1f9e8-115">Le applicazioni sono limitate alla scrittura di credenziali di dominio.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-115">Applications are limited to writing domain credentials.</span></span>

<span data-ttu-id="1f9e8-116">Windows supporta l'utilizzo espanso di smart card e credenziali del certificato.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-116">Windows supports expanded use of smart card and certificate credentials.</span></span> <span data-ttu-id="1f9e8-117">Per garantire la sicurezza, l'API di gestione delle credenziali non archivia mai il PIN della smart card nel computer.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-117">To help ensure security, the Credentials Management API never stores the smart card PIN on the computer.</span></span>

## <a name="generic-credentials"></a><span data-ttu-id="1f9e8-118">Credenziali generiche</span><span class="sxs-lookup"><span data-stu-id="1f9e8-118">Generic Credentials</span></span>

<span data-ttu-id="1f9e8-119">Le credenziali generiche sono definite e autenticate da applicazioni che gestiscono direttamente l'autorizzazione e la sicurezza anziché delegare queste attività al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-119">Generic credentials are defined and authenticated by applications that manage authorization and security directly instead of delegating these tasks to the operating system.</span></span> <span data-ttu-id="1f9e8-120">Ad esempio, un'applicazione può richiedere agli utenti di immettere un nome utente e una password forniti dall'applicazione o di produrre un [*certificato*](../secgloss/c-gly.md) per accedere a un sito Web.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-120">For example, an application can require users to enter a user name and password provided by the application or to produce a [*certificate*](../secgloss/c-gly.md) to access a website.</span></span>

<span data-ttu-id="1f9e8-121">Le applicazioni utilizzano le funzioni di gestione delle credenziali per richiedere agli utenti informazioni sulle credenziali definite dall'applicazione, generiche, ad esempio nome utente, certificato, smart card o password.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-121">Applications use Credentials Management functions to prompt users for application-defined, generic, credential information, such as user name, certificate, smart card, or password.</span></span> <span data-ttu-id="1f9e8-122">Le informazioni immesse dall'utente vengono restituite all'applicazione per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-122">The information entered by the user is returned to the application for authentication.</span></span>

<span data-ttu-id="1f9e8-123">Gestione delle credenziali offre la gestione della cache personalizzabile e l'archiviazione a lungo termine per le credenziali generiche.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-123">Credentials Management provides customizable cache management and long-term storage for generic credentials.</span></span> <span data-ttu-id="1f9e8-124">Le credenziali generiche possono essere lette e scritte dai processi utente.</span><span class="sxs-lookup"><span data-stu-id="1f9e8-124">Generic credentials can be read and written by user processes.</span></span>

 

 
