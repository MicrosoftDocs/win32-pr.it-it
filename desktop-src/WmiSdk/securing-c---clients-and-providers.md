---
description: Sia i provider C++ che le applicazioni client devono eseguire molte delle stesse operazioni per gestire la sicurezza di WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Protezione di client e provider C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac93ee88f710bf17a2b6199b3a9b2e89279b4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309892"
---
# <a name="securing-c-clients-and-providers"></a><span data-ttu-id="b2342-103">Protezione di client e provider C++</span><span class="sxs-lookup"><span data-stu-id="b2342-103">Securing C++ Clients and Providers</span></span>

<span data-ttu-id="b2342-104">Sia i provider C++ che le applicazioni client devono eseguire molte delle stesse operazioni per gestire la sicurezza di WMI.</span><span class="sxs-lookup"><span data-stu-id="b2342-104">Both C++ providers and client applications must perform many of the same operations to maintain WMI security.</span></span>

<span data-ttu-id="b2342-105">Per la connessione a WMI, le applicazioni client devono impostare correttamente la [rappresentazione](setting-the-default-process-security-level-using-c-.md) DCOM e i livelli di [autenticazione](setting-authentication-in-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="b2342-105">Client applications must set DCOM [impersonation](setting-the-default-process-security-level-using-c-.md) and [authentication](setting-authentication-in-wmi.md) levels correctly when connecting to WMI.</span></span> <span data-ttu-id="b2342-106">I callback da [chiamate asincrone](setting-security-on-an-asynchronous-call.md) presentano rischi per la sicurezza, quindi le applicazioni client devono [eseguire verifiche di accesso](performing-access-checks.md) per garantire che il callback provenga da un'origine attendibile.</span><span class="sxs-lookup"><span data-stu-id="b2342-106">Callbacks from [asynchronous calls](setting-security-on-an-asynchronous-call.md) have security risks, so client applications must [perform access checks](performing-access-checks.md) to ensure the callback is from a trusted source.</span></span> <span data-ttu-id="b2342-107">I client devono proteggere [i consumer di eventi temporanei e permanenti](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="b2342-107">Clients need to secure both [temporary and permanent event consumers](securing-wmi-events.md).</span></span>

<span data-ttu-id="b2342-108">Un provider può [eseguire verifiche di accesso](performing-access-checks.md) per assicurarsi che le risorse create siano accessibili solo ai client appropriati.</span><span class="sxs-lookup"><span data-stu-id="b2342-108">A provider may [perform access checks](performing-access-checks.md) to ensure that the resources it creates are only accessed by appropriate clients.</span></span>

<span data-ttu-id="b2342-109">Sia i provider che i client possono inoltre impostare la sicurezza in una connessione [proxy specifica](setting-the-security-on-iwbemservices-and-other-proxies.md) .</span><span class="sxs-lookup"><span data-stu-id="b2342-109">Both providers and clients also can set the security on a [specific proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) connection.</span></span> <span data-ttu-id="b2342-110">Entrambi possono anche abilitare i [privilegi](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="b2342-110">Both can also enable [privileges](executing-privileged-operations.md).</span></span> <span data-ttu-id="b2342-111">Un provider di eventi deve garantire che il consumer client disponga dei privilegi necessari per la [ricezione di un evento richiesto](providing-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="b2342-111">An event provider must ensure that the client consumer has privileges to [receive a requested event](providing-events-securely.md).</span></span>

<span data-ttu-id="b2342-112">Un client o un provider potrebbe dover effettuare una connessione remota che richiede un servizio di autenticazione diverso, ad esempio NTLM invece di Kerberos.</span><span class="sxs-lookup"><span data-stu-id="b2342-112">Either a client or provider may need to make a remote connection that requires a different authentication service, NTLM instead of Kerberos for example.</span></span>

 

 



