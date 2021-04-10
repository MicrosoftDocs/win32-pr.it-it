---
description: Fornisce informazioni specifiche di SChannel su una credenziale.
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: Esecuzione di query sugli attributi di una credenziale Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc63ccc358561dea95cb1273e1367e7fbb39d390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227375"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a><span data-ttu-id="5502e-103">Esecuzione di query sugli attributi di una credenziale Schannel</span><span class="sxs-lookup"><span data-stu-id="5502e-103">Querying the Attributes of an Schannel Credential</span></span>

<span data-ttu-id="5502e-104">La funzione [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) fornisce informazioni specifiche di SChannel su una credenziale.</span><span class="sxs-lookup"><span data-stu-id="5502e-104">The [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) function provides Schannel-specific information about a credential.</span></span> <span data-ttu-id="5502e-105">Queste informazioni vengono specificate in origine al momento della creazione della credenziale.</span><span class="sxs-lookup"><span data-stu-id="5502e-105">This information is originally specified when the credential is created.</span></span> <span data-ttu-id="5502e-106">Per ulteriori informazioni, vedere [ottenere le credenziali Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="5502e-106">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span> <span data-ttu-id="5502e-107">Le informazioni restituite da questa funzione sono valide per qualsiasi connessione ([*contesti di sicurezza*](../secgloss/s-gly.md)) creata utilizzando le credenziali specificate.</span><span class="sxs-lookup"><span data-stu-id="5502e-107">The information reported by this function is valid for any connections ([*security contexts*](../secgloss/s-gly.md)) created by using the specified credential.</span></span>

 

 
