---
description: Alcuni pacchetti di sicurezza supportano messaggi di errore estesi che consentono ai lati di un collegamento di comunicazione di comunicare qualsiasi motivo per un errore.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Informazioni estese sull'errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a4f59c53da452a3254ff6faaebeb30983498161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313742"
---
# <a name="extended-error-information"></a><span data-ttu-id="d761a-103">Informazioni estese sull'errore</span><span class="sxs-lookup"><span data-stu-id="d761a-103">Extended Error Information</span></span>

<span data-ttu-id="d761a-104">Alcuni [*pacchetti di sicurezza*](/windows/desktop/SecGloss/s-gly) supportano messaggi di errore estesi che consentono ai lati di un collegamento di comunicazione di comunicare qualsiasi motivo per un errore.</span><span class="sxs-lookup"><span data-stu-id="d761a-104">Some [*security packages*](/windows/desktop/SecGloss/s-gly) support extended error messages that allow the sides of a communication link to communicate any reasons for a failure.</span></span> <span data-ttu-id="d761a-105">Il [*protocollo Kerberos*](/windows/desktop/SecGloss/k-gly) , ad esempio, potrebbe avere esito negativo a causa di una discrepanza temporale tra l'ora della richiesta di un ticket Kerberos e l'ora del ticket del problema.</span><span class="sxs-lookup"><span data-stu-id="d761a-105">For example, the [*Kerberos protocol*](/windows/desktop/SecGloss/k-gly) could fail because of a time discrepancy between the time of request for a Kerberos ticket and the ticket's time of issue.</span></span> <span data-ttu-id="d761a-106">Con le informazioni relative alle informazioni sugli errori estesi restituite, un client può risincronizzare l'orologio e generare un nuovo messaggio di connessione.</span><span class="sxs-lookup"><span data-stu-id="d761a-106">With information from returned extended error information, a client can resynchronize its clock and generate a new connection message.</span></span>

<span data-ttu-id="d761a-107">Un pacchetto di sicurezza che imposta il flag \_ \_ di errore esteso del flag SECPKG \_ nel membro **FCapabilities** di una struttura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) indica che il pacchetto di sicurezza supporta i messaggi di errore estesi.</span><span class="sxs-lookup"><span data-stu-id="d761a-107">A security package setting the SECPKG\_FLAG\_EXTENDED\_ERROR flag in the **fCapabilities** member of a [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure indicates that the security package supports extended error messages.</span></span>

<span data-ttu-id="d761a-108">Le applicazioni client che richiedono messaggi di errore estesi specificano il \_ flag di errore esteso di ISC req \_ durante la \_ chiamata della funzione [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .</span><span class="sxs-lookup"><span data-stu-id="d761a-108">Client applications requiring extended error messages specify the ISC\_REQ\_EXTENDED\_ERROR flag when calling the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span> <span data-ttu-id="d761a-109">Per le applicazioni server che richiedono messaggi di errore estesi, impostare il \_ \_ flag di errore esteso ASC req quando si \_ chiama [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span><span class="sxs-lookup"><span data-stu-id="d761a-109">Server applications requiring extended error messages set the ASC\_REQ\_EXTENDED\_ERROR flag when calling [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span></span>

 

 
