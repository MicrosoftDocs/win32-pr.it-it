---
title: Sessioni null
description: A volte una chiamata in arrivo nella sessione null può apparire come una chiamata autenticata.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471659"
---
# <a name="null-sessions"></a><span data-ttu-id="53212-103">Sessioni null</span><span class="sxs-lookup"><span data-stu-id="53212-103">Null Sessions</span></span>

<span data-ttu-id="53212-104">A volte una chiamata in arrivo nella sessione null può apparire come una chiamata autenticata.</span><span class="sxs-lookup"><span data-stu-id="53212-104">Sometimes a call arriving on the null session can appear like an authenticated call.</span></span> <span data-ttu-id="53212-105">In particolare, la chiamata della funzione [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) restituisce il livello di autenticazione e il provider di sicurezza utilizzati per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="53212-105">Specifically, calling the [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) function returns the authentication level and security provider used for the call.</span></span> <span data-ttu-id="53212-106">Questa operazione non significa che la chiamata non si trovava in una sessione null.</span><span class="sxs-lookup"><span data-stu-id="53212-106">This operation does not mean the call was not on a null session.</span></span> <span data-ttu-id="53212-107">I due problemi sono ortogonali.</span><span class="sxs-lookup"><span data-stu-id="53212-107">The two issues are orthogonal.</span></span> <span data-ttu-id="53212-108">In Microsoft Windows 2000 una chiamata di procedura remota può tentare di rappresentare un chiamante e controllare le autorizzazioni dopo la rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="53212-108">On Microsoft Windows 2000, a remote procedure call can attempt to impersonate a caller and check the permissions after impersonation.</span></span> <span data-ttu-id="53212-109">In Microsoft Windows XP è più veloce chiamare la funzione [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) e verificare la presenza del flag **NullSession** .</span><span class="sxs-lookup"><span data-stu-id="53212-109">On Microsoft Windows XP, it is faster to call the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function and check for the **NullSession** flag.</span></span>

<span data-ttu-id="53212-110">Esiste un'altra differenza rilevante tra Windows 2000 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="53212-110">Another relevant difference exists between Windows 2000 and Windows XP.</span></span> <span data-ttu-id="53212-111">Se \_ viene specificato solo il flag RPC if \_ allow \_ \_ solo Secure, le chiamate sulla sessione null passano attraverso in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="53212-111">If only the RPC\_IF\_ALLOW\_SECURE\_ONLY flag is specified, calls on the null session go through in Windows 2000.</span></span> <span data-ttu-id="53212-112">In Windows XP, con la stretta generale delle impostazioni di sicurezza predefinite, quando si specifica questo flag, le chiamate della sessione null vengono rifiutate con accesso negato.</span><span class="sxs-lookup"><span data-stu-id="53212-112">In Windows XP, with the general tightening of default security settings, when this flag is specified, calls on the null session are rejected with access denied.</span></span> <span data-ttu-id="53212-113">Tuttavia, anche con il \_ flag RPC \_ if \_ allow \_ solo Secure, RPC non garantisce il livello di privilegio dell'utente chiamante.</span><span class="sxs-lookup"><span data-stu-id="53212-113">However, even with the RPC\_IF\_ALLOW\_SECURE\_ONLY flag, RPC does not guarantee the privilege level of the calling user.</span></span> <span data-ttu-id="53212-114">Tutti i controlli RPC sono che l'utente dispone di credenziali valide.</span><span class="sxs-lookup"><span data-stu-id="53212-114">All RPC checks is that the user has valid credentials.</span></span> <span data-ttu-id="53212-115">È possibile che l'utente chiamante stia utilizzando l'account Guest o altri account con privilegi limitati.</span><span class="sxs-lookup"><span data-stu-id="53212-115">It is possible that the calling user is using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="53212-116">Verificare che il server non assuma privilegi elevati una volta \_ RPC \_ se \_ \_ si usa Consenti solo sicurezza.</span><span class="sxs-lookup"><span data-stu-id="53212-116">Make sure the server does not assume high privilege once RPC\_IF\_ALLOW\_SECURE\_ONLY is used.</span></span>

 

 




