---
description: TLS è uno standard strettamente correlato a SSL 3,0 e viene talvolta definito &\# 0034; SSL 3,1&\# 0034;.
ms.assetid: 92b1b486-7e10-48a2-b1d2-56d4e472dbe4
title: TLS e SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac1a2e783b6f3355127a3148f1575f73119f6604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316201"
---
# <a name="tls-vs-ssl"></a><span data-ttu-id="3e259-103">TLS e SSL</span><span class="sxs-lookup"><span data-stu-id="3e259-103">TLS vs. SSL</span></span>

<span data-ttu-id="3e259-104">TLS è uno standard strettamente correlato a SSL 3,0 e viene talvolta definito "SSL 3,1".</span><span class="sxs-lookup"><span data-stu-id="3e259-104">TLS is a standard closely related to SSL 3.0, and is sometimes referred to as "SSL 3.1".</span></span> <span data-ttu-id="3e259-105">TLS sostituisce SSL 2,0 e deve essere usato in una nuova fase di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="3e259-105">TLS supersedes SSL 2.0 and should be used in new development.</span></span> <span data-ttu-id="3e259-106">A partire da Windows 10, versione 1607 e Windows Server 2016, SSL 2,0 è stato rimosso e non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="3e259-106">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

<span data-ttu-id="3e259-107">Le applicazioni che richiedono un elevato livello di interoperabilità devono supportare SSL 3,0 e TLS.</span><span class="sxs-lookup"><span data-stu-id="3e259-107">Applications that require a high level of interoperability should support SSL 3.0 and TLS.</span></span> <span data-ttu-id="3e259-108">A causa delle analogie tra questi due protocolli, i dettagli SSL non sono inclusi in questa documentazione, tranne nei casi in cui si differenziano da TLS.</span><span class="sxs-lookup"><span data-stu-id="3e259-108">Because of the similarities between these two protocols, SSL details are not included in this documentation, except where they differ from TLS.</span></span> <span data-ttu-id="3e259-109">Di seguito è riportato da [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):</span><span class="sxs-lookup"><span data-stu-id="3e259-109">The following is from [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):</span></span>

<span data-ttu-id="3e259-110">"Le differenze tra questo protocollo e SSL 3,0 non sono drammatiche, ma sono sufficientemente significative che TLS 1,0 e SSL 3,0 non interagiscono (sebbene TLS 1,0 incorpori un meccanismo mediante il quale un'implementazione TLS può tornare a SSL 3,0)".</span><span class="sxs-lookup"><span data-stu-id="3e259-110">"The differences between this protocol and SSL 3.0 are not dramatic, but they are significant enough that TLS 1.0 and SSL 3.0 do not interoperate (although TLS 1.0 does incorporate a mechanism by which a TLS implementation can back down to SSL 3.0)."</span></span>

 

 



