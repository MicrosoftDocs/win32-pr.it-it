---
title: Configurazione dell'autenticazione dinamica
description: Le applicazioni possono modificare le configurazioni di autenticazione in un gruppo di URL o in una sessione del server in qualsiasi momento.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c68daf04d870d4aa50596397f4f021ac1729af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328895"
---
# <a name="dynamic-authentication-configuration"></a><span data-ttu-id="3da57-103">Configurazione dell'autenticazione dinamica</span><span class="sxs-lookup"><span data-stu-id="3da57-103">Dynamic Authentication Configuration</span></span>

<span data-ttu-id="3da57-104">Per impostazione predefinita, l'API server HTTP non esegue l'autenticazione a meno che l'applicazione non lo consenta in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="3da57-104">By default, the HTTP Server API does not perform authentication unless the application specifically enables it.</span></span> <span data-ttu-id="3da57-105">Le applicazioni possono modificare le configurazioni di autenticazione in un gruppo di URL o in una sessione del server in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="3da57-105">Applications can change authentication configurations on a URL Group or server session at any time.</span></span> <span data-ttu-id="3da57-106">Le modifiche apportate alla configurazione dell'autenticazione non influiscono sulle richieste già autenticate o inviate all'applicazione</span><span class="sxs-lookup"><span data-stu-id="3da57-106">Changes to the authentication configuration do not affect requests that are already authenticated or being dispatched to the application</span></span>

<span data-ttu-id="3da57-107">Per gli schemi di autenticazione in cui sono necessari più cicli di handshake, l'API server HTTP elimina l'handshake di autenticazione se lo schema corrente non è più supportato a causa delle modifiche di configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3da57-107">For authentication schemes where multiple rounds of handshake are required, the HTTP Server API drops the authentication handshake if the current scheme is no longer supported due to configuration changes from the application.</span></span> <span data-ttu-id="3da57-108">Se, ad esempio, l'applicazione Abilita Negotiate e Disabilita NTLM e l'API del server HTTP è nell'handshake di autenticazione intermedia per NTLM, l'handshake per NTLM viene ignorato e la richiesta viene passata all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3da57-108">For example, if the application enables Negotiate and disables NTLM, and the HTTP Server API is in the intermediate authentication handshake for NTLM, the handshake for NTLM is discarded and the request is passed to the application.</span></span> <span data-ttu-id="3da57-109">L'applicazione invia una richiesta di autenticazione 401 con i nuovi tipi di autenticazione specificati nell'intestazione del WWW-Authenticate.</span><span class="sxs-lookup"><span data-stu-id="3da57-109">The application sends a 401 authentication challenge with the new authentication types specified in the WWW-Authenticate header.</span></span>

 

 




