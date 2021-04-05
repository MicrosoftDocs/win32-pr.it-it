---
title: Connessione a Active Directory
description: Sono disponibili diversi metodi per accedere Active Directory.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Connessione a Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7626f01b644a0bb1a3acb39c5ef5ead70434e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955107"
---
# <a name="connecting-to-active-directory"></a><span data-ttu-id="cc60d-104">Connessione a Active Directory</span><span class="sxs-lookup"><span data-stu-id="cc60d-104">Connecting to Active Directory</span></span>

<span data-ttu-id="cc60d-105">Sono disponibili diversi metodi per accedere Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc60d-105">There are several methods used to access Active Directory.</span></span> <span data-ttu-id="cc60d-106">Si consiglia di usare l'API ADSI per accedere Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc60d-106">It is recommended that you use the ADSI API to access Active Directory.</span></span> <span data-ttu-id="cc60d-107">ADSI implementa il protocollo LDAP per comunicare con Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc60d-107">ADSI implements the LDAP protocol to communicate with Active Directory.</span></span> <span data-ttu-id="cc60d-108">Negli esempi di codice seguenti viene illustrato come accedere a Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc60d-108">The following code examples show how to access Active Directory.</span></span>


```VB
Set ns = GetObject("LDAP:")
```



<span data-ttu-id="cc60d-109">Il provider LDAP verrà aperto e preparato per il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="cc60d-109">This opens the LDAP provider and prepares it to retrieve data.</span></span> <span data-ttu-id="cc60d-110">Non viene stabilita alcuna connessione fino a quando non vengono richiesti i dati.</span><span class="sxs-lookup"><span data-stu-id="cc60d-110">No connection is established until data is requested.</span></span> <span data-ttu-id="cc60d-111">Quando vengono richiesti dati, ADSI, con l'aiuto del servizio Locator, tenta di trovare il controller di dominio migliore per la connessione e stabilisce una connessione al server.</span><span class="sxs-lookup"><span data-stu-id="cc60d-111">When data is requested, ADSI, with the help of the locator service, attempts to find the best domain controller (DC) for the connection and will establish a connection to the server.</span></span> <span data-ttu-id="cc60d-112">Questo processo è noto come binding senza server.</span><span class="sxs-lookup"><span data-stu-id="cc60d-112">This process is known as serverless binding.</span></span>

<span data-ttu-id="cc60d-113">ADSI consente inoltre di specificare il nome del server da utilizzare per la connessione.</span><span class="sxs-lookup"><span data-stu-id="cc60d-113">ADSI also enables you to specify the server name to use for the connection.</span></span>


```VB
Set obj = GetObject("LDAP://mysrv01")
```



<span data-ttu-id="cc60d-114">In un altro scenario, è possibile che si conosca solo il nome di dominio, ma non il nome del server specifico.</span><span class="sxs-lookup"><span data-stu-id="cc60d-114">In another scenario, you may only know the domain name but not the specific server name.</span></span> <span data-ttu-id="cc60d-115">Anche in questo caso, ADSI consente di specificare il nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="cc60d-115">Again, ADSI enables you to specify the domain name.</span></span> <span data-ttu-id="cc60d-116">In Windows 2000, il nome di dominio è rappresentato come nome DNS.</span><span class="sxs-lookup"><span data-stu-id="cc60d-116">In Windows 2000, the domain name is represented as a DNS name.</span></span> <span data-ttu-id="cc60d-117">Ad esempio, se Joe worden, l'amministratore di rete sceglie di connettersi usando il nome di dominio, può usare l'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="cc60d-117">For example, if Joe Worden, the network administrator, chooses to connect using the domain name, he could use the following code example.</span></span>


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



<span data-ttu-id="cc60d-118">ADSI si connetterà a uno dei controller di dominio nel dominio fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="cc60d-118">ADSI will connect to one of the domain controllers in the fabrikam.com domain.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc60d-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc60d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc60d-120">Associazione a oggetti Active Directory</span><span class="sxs-lookup"><span data-stu-id="cc60d-120">Binding to Active Directory Objects</span></span>](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




