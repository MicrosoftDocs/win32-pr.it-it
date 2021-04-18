---
description: Un contesto di sicurezza è il set di attributi di sicurezza e regole attive durante una sessione di comunicazione.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Semantica del contesto SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcb604e09b1a2458ef05204aefbe754af26b210
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316215"
---
# <a name="sspi-context-semantics"></a><span data-ttu-id="d3f8c-103">Semantica del contesto SSPI</span><span class="sxs-lookup"><span data-stu-id="d3f8c-103">SSPI Context Semantics</span></span>

<span data-ttu-id="d3f8c-104">Un [*contesto di sicurezza*](../secgloss/s-gly.md) è il set di attributi di sicurezza e regole attive durante una sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="d3f8c-104">A [*security context*](../secgloss/s-gly.md) is the set of security attributes and rules in effect during a communication session.</span></span> <span data-ttu-id="d3f8c-105">Sono incluse informazioni quali le identità del principale e le informazioni sulle chiavi, le crittografie e gli algoritmi utilizzati.</span><span class="sxs-lookup"><span data-stu-id="d3f8c-105">This includes such information as the identities of the principal and information on the keys, ciphers, and algorithms being used.</span></span> <span data-ttu-id="d3f8c-106">Per [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI), un contesto di sicurezza è una struttura opaca creata tramite uno scambio che interessa la funzione [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) e la funzione [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .</span><span class="sxs-lookup"><span data-stu-id="d3f8c-106">For [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI), a security context is an opaque structure that is created through an exchange involving the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function and the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span>

<span data-ttu-id="d3f8c-107">Per ulteriori informazioni sugli attributi di contesto, vedere [requisiti di contesto](context-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d3f8c-107">For more information about the context attributes, see [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="d3f8c-108">Il modello SSPI supporta tre tipi di contesti di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d3f8c-108">The SSPI model supports three types of security contexts.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3f8c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3f8c-109">Type</span></span></th>
<th><span data-ttu-id="d3f8c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3f8c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3f8c-111"><a href="connection-oriented-contexts.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="d3f8c-111"><a href="connection-oriented-contexts.md">Connection</a></span></span></td>
<td><span data-ttu-id="d3f8c-112">Un <a href="/windows/desktop/SecGloss/c-gly"><em>contesto</em></a> orientato alla connessione è il contesto di sicurezza più comune e più semplice da usare.</span><span class="sxs-lookup"><span data-stu-id="d3f8c-112">A connection-oriented <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> is the most common security context, and the simplest to use.</span></span> <span data-ttu-id="d3f8c-113">Il chiamante è responsabile del formato generale del messaggio e della posizione dei dati nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="d3f8c-113">The caller is responsible for the overall message format and for the location of the data in the message.</span></span> <span data-ttu-id="d3f8c-114">Il chiamante è inoltre responsabile della posizione dei campi relativi alla sicurezza all'interno di un messaggio, ad esempio la posizione dei dati della firma.</span><span class="sxs-lookup"><span data-stu-id="d3f8c-114">The caller is also responsible for the location of the security-relevant fields within a message, such as the location of the signature data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3f8c-115"><a href="datagram-contexts.md">Datagram</a></span><span class="sxs-lookup"><span data-stu-id="d3f8c-115"><a href="datagram-contexts.md">Datagram</a></span></span></td>
<td><span data-ttu-id="d3f8c-116">Un contesto orientato ai <a href="/windows/desktop/SecGloss/d-gly"><em>datagramma</em></a>ha un supporto aggiuntivo per la comunicazione del datagramma di tipo DCE.</span><span class="sxs-lookup"><span data-stu-id="d3f8c-116">A <a href="/windows/desktop/SecGloss/d-gly"><em>datagram</em></a>-oriented context has extra support for DCE-style datagram communication.</span></span> <span data-ttu-id="d3f8c-117">Può anche essere usato in modo generico per un'applicazione di trasporto orientata ai datagramma.</span><span class="sxs-lookup"><span data-stu-id="d3f8c-117">It can also be used generically for a datagram-oriented transport application.</span></span><br/>
<blockquote>
<p>[!Important]</p>
<p><span data-ttu-id="d3f8c-118">Il pacchetto <a href="microsoft-kerberos.md">Microsoft Kerberos</a> non supporta i contesti di datagramma in modalità utente-utente.</span><span class="sxs-lookup"><span data-stu-id="d3f8c-118">The <a href="microsoft-kerberos.md">Microsoft Kerberos</a> package does not support datagram contexts in user-to-user mode.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3f8c-119"><a href="stream-contexts.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="d3f8c-119"><a href="stream-contexts.md">Stream</a></span></span></td>
<td><span data-ttu-id="d3f8c-120">Un contesto orientato al flusso è responsabile del blocco e della formattazione dei messaggi all'interno del pacchetto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d3f8c-120">A stream-oriented context is responsible for the blocking and message formatting within the security package.</span></span> <span data-ttu-id="d3f8c-121">Il chiamante non è interessato alla formattazione, ma piuttosto a un flusso di dati non elaborato.</span><span class="sxs-lookup"><span data-stu-id="d3f8c-121">The caller is not interested in formatting, but rather a raw stream of data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d3f8c-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d3f8c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3f8c-123">Requisiti del contesto</span><span class="sxs-lookup"><span data-stu-id="d3f8c-123">Context Requirements</span></span>](context-requirements.md)
</dt> <dt>

[<span data-ttu-id="d3f8c-124">Contesti orientati alla connessione</span><span class="sxs-lookup"><span data-stu-id="d3f8c-124">Connection-Oriented Contexts</span></span>](connection-oriented-contexts.md)
</dt> <dt>

[<span data-ttu-id="d3f8c-125">Contesti di datagramma</span><span class="sxs-lookup"><span data-stu-id="d3f8c-125">Datagram Contexts</span></span>](datagram-contexts.md)
</dt> <dt>

[<span data-ttu-id="d3f8c-126">Contesti di flusso</span><span class="sxs-lookup"><span data-stu-id="d3f8c-126">Stream Contexts</span></span>](stream-contexts.md)
</dt> </dl>

 

 
