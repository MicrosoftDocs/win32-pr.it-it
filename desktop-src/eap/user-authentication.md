---
title: Autenticazione degli utenti
description: Il protocollo di autenticazione può autenticare l'utente tramite PEAP (Protected EAP).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "103719570"
---
# <a name="user-authentication"></a><span data-ttu-id="85c75-103">Autenticazione degli utenti</span><span class="sxs-lookup"><span data-stu-id="85c75-103">User Authentication</span></span>

<span data-ttu-id="85c75-104">Il protocollo di autenticazione può autenticare l'utente tramite PEAP (Protected EAP).</span><span class="sxs-lookup"><span data-stu-id="85c75-104">The authentication protocol itself can authenticate the user via Protected EAP (PEAP).</span></span> <span data-ttu-id="85c75-105">Sono inoltre disponibili due provider di autenticazione integrati nel sistema operativo: autenticazione del dominio di Windows (a cui si accede tramite servizi directory) e servizio di accesso remoto (RADIUS, Remote Access Dial-in User).</span><span class="sxs-lookup"><span data-stu-id="85c75-105">There are also two authentication providers built into the operating system: Windows domain authentication (accessed via Directory Services) and Remote Access Dial-In User Service (RADIUS).</span></span>

<span data-ttu-id="85c75-106">Nel caso in cui RADIUS sia il provider di autenticazione, il plug-in EAP viene installato nel server RADIUS anziché nel server punto di accesso wireless, ad esempio un server RAS.</span><span class="sxs-lookup"><span data-stu-id="85c75-106">In the case where RADIUS is the authentication provider, the EAP Plug-in is installed on the RADIUS server rather than on the wireless Access Point (AP) server, such as a RAS server.</span></span> <span data-ttu-id="85c75-107">Il server AP passa i pacchetti EAP direttamente dal client al servizio di autenticazione sul server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="85c75-107">The AP server passes EAP packets directly from the client to the authentication service on the RADIUS server.</span></span> <span data-ttu-id="85c75-108">Il server AP non elabora alcuna informazione nei pacchetti EAP, ma deve accettare le chiavi di crittografia generate dal lato server, complete (256 bit), per creare la connessione protetta.</span><span class="sxs-lookup"><span data-stu-id="85c75-108">The AP server does not process any of the information in the EAP packets, but it must accept the server-side, full strength (256 bit) PEAP generated encryption keys in order to create the secure connection.</span></span>

 

 




