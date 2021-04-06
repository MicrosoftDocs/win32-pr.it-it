---
title: Credenziali di autenticazione client
description: Ogni client autenticato deve fornire le credenziali di autenticazione al server.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3704663411fc33340a462d8e3b356041b6061468
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045291"
---
# <a name="client-authentication-credentials"></a><span data-ttu-id="33920-103">Credenziali di autenticazione client</span><span class="sxs-lookup"><span data-stu-id="33920-103">Client Authentication Credentials</span></span>

<span data-ttu-id="33920-104">Ogni client autenticato deve fornire le credenziali di autenticazione al server.</span><span class="sxs-lookup"><span data-stu-id="33920-104">Each authenticated client must provide authentication credentials to the server.</span></span> <span data-ttu-id="33920-105">In RPC il client archivia le proprie credenziali di autenticazione nell'associazione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="33920-105">Under RPC, the client stores its authentication credentials in the binding between the client and the server.</span></span> <span data-ttu-id="33920-106">A tale scopo, il client chiama [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).</span><span class="sxs-lookup"><span data-stu-id="33920-106">To do this, the client calls [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).</span></span>

<span data-ttu-id="33920-107">Esistono due tipi di credenziali, implicite ed esplicite:</span><span class="sxs-lookup"><span data-stu-id="33920-107">There are two types of credentials—implicit and explicit:</span></span>

-   <span data-ttu-id="33920-108">Le credenziali esplicite sono disponibili quando il client fornisce il nome utente, la password e il dominio.</span><span class="sxs-lookup"><span data-stu-id="33920-108">Explicit credentials exist when the client supplies username, password, and domain.</span></span>
-   <span data-ttu-id="33920-109">Le credenziali implicite sono disponibili quando il client utilizza le credenziali del thread o del token di processo chiamando le funzioni **RpcBindingSetAuthInfo** o **RpcBindingSetAuthInfoEx** .</span><span class="sxs-lookup"><span data-stu-id="33920-109">Implicit credentials exist when the client uses credentials from the thread or process token calling the **RpcBindingSetAuthInfo** or **RpcBindingSetAuthInfoEx** functions.</span></span>

<span data-ttu-id="33920-110">I client devono evitare di fornire credenziali esplicite perché l'archiviazione, la manipolazione e il recupero di una password utente possono introdurre una vulnerabilità di sicurezza in un sistema distribuito se vengono usate credenziali esplicite.</span><span class="sxs-lookup"><span data-stu-id="33920-110">Clients should refrain from supplying explicit credentials because storing, manipulating, and retrieving a user password can introduce a security vulnerability into a distributed system if explicit credentials are used.</span></span>

<span data-ttu-id="33920-111">Per usare le credenziali implicite, il client chiama **RpcBindingSetAuthInfo**(ad *esempio*).</span><span class="sxs-lookup"><span data-stu-id="33920-111">To use implicit credentials, the client calls **RpcBindingSetAuthInfo**(*Ex*).</span></span> <span data-ttu-id="33920-112">Il sistema di sicurezza e RPC ottengono le credenziali dal thread o dal token del processo per l'uso nella sessione di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="33920-112">The security system and RPC obtain credentials from the thread or process token for use in the authentication session.</span></span>

<span data-ttu-id="33920-113">Se il client usa credenziali esplicite, il quinto parametro di queste due funzioni è di [**tipo \_ \_ \_ handle di identità di autenticazione RPC**](rpc-auth-identity-handle.md).</span><span class="sxs-lookup"><span data-stu-id="33920-113">If the client uses explicit credentials, the fifth parameter of these two functions is of type [**RPC\_AUTH\_IDENTITY\_HANDLE**](rpc-auth-identity-handle.md).</span></span> <span data-ttu-id="33920-114">Si tratta di un tipo flessibile che rappresenta un puntatore a una struttura di dati.</span><span class="sxs-lookup"><span data-stu-id="33920-114">This is a flexible type that is a pointer to a data structure.</span></span> <span data-ttu-id="33920-115">Il contenuto della struttura dei dati può variare a seconda del servizio di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="33920-115">The contents of the data structure can differ with each authentication service.</span></span> <span data-ttu-id="33920-116">Attualmente, i SSP supportati da RPC richiedono che l'applicazione imposti l' **\_ handle di \_ identità \_ di autenticazione RPC** in modo che punti a una struttura di [**\_ \_ \_ identità di autenticazione WinNT sec**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) .</span><span class="sxs-lookup"><span data-stu-id="33920-116">Currently, the SSPs that RPC supports require that your application set **RPC\_AUTH\_IDENTITY\_HANDLE** to point to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) structure.</span></span> <span data-ttu-id="33920-117">La struttura di **\_ \_ \_ identità di autenticazione WinNT sec** contiene i campi relativi a nome utente, dominio e password.</span><span class="sxs-lookup"><span data-stu-id="33920-117">The **SEC\_WINNT\_AUTH\_IDENTITY** structure contains fields for a user name, domain, and password.</span></span>

 

 




