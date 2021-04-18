---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300546"
---
# <a name="ntlmssp"></a><span data-ttu-id="d3570-103">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="d3570-103">NTLMSSP</span></span>

<span data-ttu-id="d3570-104">NTLMSSP, il cui identificatore del servizio di autenticazione è RPC \_ C \_ AuthN \_ WinNT, è un Security Support Provider disponibile in tutte le versioni di DCOM.</span><span class="sxs-lookup"><span data-stu-id="d3570-104">NTLMSSP, whose authentication service identifier is RPC\_C\_AUTHN\_WINNT, is a security support provider that is available on all versions of DCOM.</span></span> <span data-ttu-id="d3570-105">Usa il protocollo NTLM per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d3570-105">It uses the NTLM protocol for authentication.</span></span> <span data-ttu-id="d3570-106">NTLM non trasmette mai la password dell'utente al server durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d3570-106">NTLM never actually transmits the user's password to the server during authentication.</span></span> <span data-ttu-id="d3570-107">Pertanto, il server non può utilizzare la password durante la rappresentazione per accedere alle risorse di rete a cui l'utente può accedere.</span><span class="sxs-lookup"><span data-stu-id="d3570-107">Therefore, the server cannot use the password during impersonation to access network resources that the user would have access to.</span></span> <span data-ttu-id="d3570-108">È possibile accedere solo alle risorse locali.</span><span class="sxs-lookup"><span data-stu-id="d3570-108">Only local resources can be accessed.</span></span>

<span data-ttu-id="d3570-109">NTLM funziona sia localmente che tra computer diversi.</span><span class="sxs-lookup"><span data-stu-id="d3570-109">NTLM works both locally and across computers.</span></span> <span data-ttu-id="d3570-110">Ovvero, se il client e il server si trovano in computer diversi, NTLM può comunque assicurarsi che il client sia quello che dichiara di essere.</span><span class="sxs-lookup"><span data-stu-id="d3570-110">That is, if the client and server are on different computers, NTLM can still make sure the client is who it claims to be.</span></span>

<span data-ttu-id="d3570-111">Con NTLM, l'identità del client viene rappresentata da un nome di dominio, un nome utente e una password o un token.</span><span class="sxs-lookup"><span data-stu-id="d3570-111">With NTLM, the client's identity is represented by a domain name, user name, and a password or token.</span></span> <span data-ttu-id="d3570-112">Quando un server chiama [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), vengono restituiti il nome di dominio e il nome utente del client.</span><span class="sxs-lookup"><span data-stu-id="d3570-112">When a server calls [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), the client's domain name and user name are returned.</span></span> <span data-ttu-id="d3570-113">Tuttavia, quando un server chiama [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), viene restituito il token del client.</span><span class="sxs-lookup"><span data-stu-id="d3570-113">However, when a server calls [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), the client's token is returned.</span></span> <span data-ttu-id="d3570-114">Se non esiste alcuna relazione di trust tra client e server e se il server dispone di un account locale con lo stesso nome e la stessa password del client, l'account verrà utilizzato per rappresentare il client.</span><span class="sxs-lookup"><span data-stu-id="d3570-114">If there is no trust relationship between client and server and if the server has a local account with the same name and password as the client, that account will be used to represent the client.</span></span>

<span data-ttu-id="d3570-115">NTLM supporta l'autenticazione reciproca e cross-process (solo in locale).</span><span class="sxs-lookup"><span data-stu-id="d3570-115">NTLM supports mutual authentication cross-thread and cross-process (locally only).</span></span> <span data-ttu-id="d3570-116">Se il client specifica il nome dell'entità del server nel formato utente del dominio \\ in una chiamata a [**IClientSecurity:: seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), l'identità del server deve corrispondere al nome dell'entità o la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="d3570-116">If the client specifies the principal name of the server in the form domain\\user in a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), the server's identity must match that principal name or the call will fail.</span></span> <span data-ttu-id="d3570-117">Se il client specifica **null**, l'identità del server non verrà controllata.</span><span class="sxs-lookup"><span data-stu-id="d3570-117">If the client specifies **NULL**, the server's identity will not be checked.</span></span>

<span data-ttu-id="d3570-118">NTLM supporta inoltre il livello di rappresentazione del delegato cross-thread e cross-process (solo localmente).</span><span class="sxs-lookup"><span data-stu-id="d3570-118">NTLM additionally supports the delegate impersonation level cross-thread and cross-process (locally only).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3570-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d3570-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3570-120">Pacchetti COM e di sicurezza</span><span class="sxs-lookup"><span data-stu-id="d3570-120">COM and Security Packages</span></span>](com-and-security-packages.md)
</dt> </dl>

 

 