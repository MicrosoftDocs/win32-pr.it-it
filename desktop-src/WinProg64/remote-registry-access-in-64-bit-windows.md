---
title: Accesso al registro di sistema remoto in Windows a 64 bit
description: Il redirector del registro di sistema consente l'accesso remoto al registro di sistema in Windows a 64 bit tramite la funzione RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- accesso al registro di sistema remoto a 64 bit programmazione Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299830"
---
# <a name="remote-registry-access-in-64-bit-windows"></a><span data-ttu-id="c92ce-104">Accesso al registro di sistema remoto in Windows a 64 bit</span><span class="sxs-lookup"><span data-stu-id="c92ce-104">Remote Registry Access in 64-bit Windows</span></span>

<span data-ttu-id="c92ce-105">Il redirector del registro di sistema consente l'accesso remoto al registro di sistema in Windows a 64 bit tramite la funzione [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) .</span><span class="sxs-lookup"><span data-stu-id="c92ce-105">The registry redirector provides remote access to the registry on 64-bit Windows through the [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) function.</span></span>

<span data-ttu-id="c92ce-106">Se il client è un'applicazione a 32 bit, accede alla visualizzazione del registro di sistema predefinita a 32 bit del server.</span><span class="sxs-lookup"><span data-stu-id="c92ce-106">If the client is a 32-bit application, it accesses the server's default 32-bit registry view.</span></span> <span data-ttu-id="c92ce-107">Se il client è un'applicazione a 64 bit, accede alla visualizzazione del registro di sistema a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="c92ce-107">If the client is a 64-bit application, it accesses the 64-bit registry view.</span></span>

<span data-ttu-id="c92ce-108">**Windows Server 2003:** Tutti i client accedono alla visualizzazione del registro di sistema a 64 bit, a meno che l'applicazione non usi il \_ \_ flag 32KEY WOW64 chiave.</span><span class="sxs-lookup"><span data-stu-id="c92ce-108">**Windows Server 2003:** All clients access the 64-bit registry view unless the application uses the KEY\_WOW64\_32KEY flag.</span></span> <span data-ttu-id="c92ce-109">Questo comportamento è stato modificato con Windows Server 2003 con Service Pack 1 (SP1) e Windows XP Professional x64 Edition, a condizione che sia il client che il server eseguano queste versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="c92ce-109">This behavior changed with Windows Server 2003 with Service Pack 1 (SP1) and Windows XP Professional x64 Edition, provided that both the client and the server are running these versions of Windows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c92ce-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c92ce-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c92ce-111">Redirector del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c92ce-111">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="c92ce-112">Reflection del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c92ce-112">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

 