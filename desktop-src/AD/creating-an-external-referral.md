---
title: Creazione di un riferimento esterno
description: Se viene creato un oggetto crossRef esterno e un controller di dominio lo usa per generare un riferimento, l'oggetto crossRef fornisce due elementi dati importanti nelle proprietà seguenti.
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- riferimenti esterni Active Directory
- Esempi di Active Directory Active Directory, creazione di un riferimento esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724591"
---
# <a name="creating-an-external-referral"></a><span data-ttu-id="e62b9-105">Creazione di un riferimento esterno</span><span class="sxs-lookup"><span data-stu-id="e62b9-105">Creating an External Referral</span></span>

<span data-ttu-id="e62b9-106">Se viene creato un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) esterno e un controller di dominio lo usa per generare un riferimento, l'oggetto **crossRef** fornisce due elementi dati importanti nelle proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="e62b9-106">If an external [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is created and a domain controller uses it to generate a referral, the **crossRef** object provides two important data elements in the following properties.</span></span> <span data-ttu-id="e62b9-107">Per ulteriori informazioni sulle situazioni in cui questo può verificarsi, vedere la sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="e62b9-107">For more information about situations where this can occur, see the previous section.</span></span>



| <span data-ttu-id="e62b9-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e62b9-108">Property</span></span>                           | <span data-ttu-id="e62b9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e62b9-109">Description</span></span>                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e62b9-110">**dnsRoot**</span><span class="sxs-lookup"><span data-stu-id="e62b9-110">**dnsRoot**</span></span>](/windows/desktop/ADSchema/a-dnsroot) | <span data-ttu-id="e62b9-111">Specifica il server o il dominio che può fornire dati dal contesto dei nomi specificato in [**NCName**](/windows/desktop/ADSchema/a-ncname).</span><span class="sxs-lookup"><span data-stu-id="e62b9-111">Specifies the server or domain that can serve data from the naming context specified in [**nCName**](/windows/desktop/ADSchema/a-ncname).</span></span>                                           |
| [<span data-ttu-id="e62b9-112">**nCName**</span><span class="sxs-lookup"><span data-stu-id="e62b9-112">**nCName**</span></span>](/windows/desktop/ADSchema/a-ncname)   | <span data-ttu-id="e62b9-113">Specifica il nome distinto per il dominio, lo schema o il contenitore di configurazione radice nel server o nel dominio specificato da [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot).</span><span class="sxs-lookup"><span data-stu-id="e62b9-113">Specifies the distinguished name for the domain, schema, or configuration container rooted at the server or domain specified by [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot).</span></span> |



 

<span data-ttu-id="e62b9-114">Se, ad esempio, il server con indirizzo DNS di serv1.northwest.Fabrikam.com serve il contesto dei nomi radice in CN = MyServer, OU = MyDOM, O = Fabrikam, impostare [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) sull'indirizzo DNS di tale server e [**NCName**](/windows/desktop/ADSchema/a-ncname) sul nome distinto del contenitore di dominio, schema o configurazione.</span><span class="sxs-lookup"><span data-stu-id="e62b9-114">For example, if the server with DNS address of serv1.northwest.Fabrikam.com serves the naming context rooted at CN=MyContainer,OU=MyDOM,O=Fabrikam, set the [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) to that server's DNS address and the [**nCName**](/windows/desktop/ADSchema/a-ncname) to the distinguished name of the domain, schema, or configuration container.</span></span>

<span data-ttu-id="e62b9-115">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come creare un riferimento esterno, vedere il [codice di esempio per la creazione di un oggetto crossRef esterno](example-code-for-creating-an-external-crossref-object.md).</span><span class="sxs-lookup"><span data-stu-id="e62b9-115">For more information and a code example that shows how to create an external referral, see [Example Code for Creating an External crossRef Object](example-code-for-creating-an-external-crossref-object.md).</span></span>

 

 