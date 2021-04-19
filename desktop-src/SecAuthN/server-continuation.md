---
description: In base al codice restituito da una chiamata precedente a AcceptSecurityContext (generale), il server può attendere una risposta dal client e può partecipare a scambi aggiuntivi con il client.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Continuazione server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fba8a60bea12daae0e6aaf93fed55fead5738c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311599"
---
# <a name="server-continuation"></a><span data-ttu-id="87d39-103">Continuazione server</span><span class="sxs-lookup"><span data-stu-id="87d39-103">Server Continuation</span></span>

<span data-ttu-id="87d39-104">In base al codice restituito da una chiamata precedente a [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), il server può attendere una risposta dal client e può partecipare a scambi aggiuntivi con il client.</span><span class="sxs-lookup"><span data-stu-id="87d39-104">Based on the return code from a previous call to [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), the server can wait for a response from the client and can participate in additional exchanges with the client.</span></span> <span data-ttu-id="87d39-105">Per continuare il protocollo di autenticazione, il server ripete le chiamate a **AcceptSecurityContext (generale)**.</span><span class="sxs-lookup"><span data-stu-id="87d39-105">To continue the authentication protocol, the server repeats calls to **AcceptSecurityContext (General)**.</span></span>

<span data-ttu-id="87d39-106">Lo stato restituito da [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) viene controllato per verificare se il server deve attendere messaggi aggiuntivi dal client.</span><span class="sxs-lookup"><span data-stu-id="87d39-106">The status returned by [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) is checked to see if the server needs to wait for additional messages from the client.</span></span> <span data-ttu-id="87d39-107">Nella maggior parte dei protocolli di autenticazione è disponibile un numero massimo di scambi anche per l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="87d39-107">In most authentication protocols, there is a maximum number of exchanges even for mutual authentication.</span></span> <span data-ttu-id="87d39-108">Attualmente, i protocolli NTLM e [*Kerberos*](../secgloss/k-gly.md) eseguono l'autenticazione reciproca con tre scambi.</span><span class="sxs-lookup"><span data-stu-id="87d39-108">Currently, both the NTLM and [*Kerberos protocols*](../secgloss/k-gly.md) do mutual authentication with three exchanges.</span></span>

 

 
