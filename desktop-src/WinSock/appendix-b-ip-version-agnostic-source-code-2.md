---
description: In questa appendice viene illustrata una versione riscritta delle applicazioni di esempio SIMPLEC. c e simples. c che gestiscono normalmente il codice server CodeIPv6-Enabled client abilitato per IPv4 o IPv6.
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: 'Appendice B: codice sorgente indipendente dalla versione IP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333e344376695122ebcd650ebf2595d70afbf7ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879237"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a><span data-ttu-id="9eb9f-103">Appendice B: codice sorgente indipendente dalla versione IP</span><span class="sxs-lookup"><span data-stu-id="9eb9f-103">Appendix B: IP-version Agnostic Source Code</span></span>

<span data-ttu-id="9eb9f-104">In questa appendice viene illustrata una versione riscritta delle applicazioni di esempio SIMPLEC. c e simples. c che gestiscono normalmente IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="9eb9f-104">This appendix illustrates a rewritten version of the Simplec.c and Simples.c sample applications that gracefully handles either IPv4 or IPv6.</span></span>

-   [<span data-ttu-id="9eb9f-105">Codice client abilitato per IPv6</span><span class="sxs-lookup"><span data-stu-id="9eb9f-105">IPv6-Enabled Client Code</span></span>](ipv6-enabled-client-code-2.md)
-   [<span data-ttu-id="9eb9f-106">Codice server abilitato per IPv6</span><span class="sxs-lookup"><span data-stu-id="9eb9f-106">IPv6-Enabled Server Code</span></span>](ipv6-enabled-server-code-2.md)

<span data-ttu-id="9eb9f-107">Questo codice esemplifica le linee guida definite in questa guida IPv6 ed è incluso per fornire codice sorgente che è stato modificato correttamente per aggiungere il supporto per IPv6.</span><span class="sxs-lookup"><span data-stu-id="9eb9f-107">This code exemplifies the guidelines set forth in this IPv6 guide, and is included to provide source code that has been successfully modified to add support for IPv6.</span></span> <span data-ttu-id="9eb9f-108">Questo esempio è intenzionalmente semplice, ma offre un esempio pratico per la lettura e la revisione.</span><span class="sxs-lookup"><span data-stu-id="9eb9f-108">This sample is intentionally simple, but provides a hands-on sample for perusing and reviewing.</span></span> <span data-ttu-id="9eb9f-109">Una versione solo IPv4 di questo codice sorgente è disponibile nell' [appendice a: codice sorgente solo IPv4](appendix-a-ipv4-only-source-code-2.md).</span><span class="sxs-lookup"><span data-stu-id="9eb9f-109">An IPv4 only version of this source code is provided in [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md).</span></span>

<span data-ttu-id="9eb9f-110">Confrontando il codice sorgente in Appendice A (solo IPv4) e Appendice B (IP-version Agnostic), si ottiene un'idea delle modifiche necessarie per modificare l'applicazione Windows Sockets per aggiungere il supporto per IPv6.</span><span class="sxs-lookup"><span data-stu-id="9eb9f-110">By comparing the source code in Appendix A (IPv4 only) and Appendix B (IP-version agnostic), you get a sense of the changes necessary to modify your Windows Sockets application to add support for IPv6.</span></span>

 

 



