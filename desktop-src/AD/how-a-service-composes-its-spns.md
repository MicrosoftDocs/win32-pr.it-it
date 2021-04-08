---
title: Come un servizio compone i relativi nomi SPN
description: Un servizio può utilizzare due funzioni per comporre i relativi SPN DsGetSpn è una funzione generica per la composizione di SPN e DsServerRegisterSpn è una funzione specializzata per la composizione e la registrazione di nomi SPN semplici per un servizio basato su host.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- nome dell'entità servizio AD, come compone un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5611527cc3c240eebc195058ce39daab71aeef23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855429"
---
# <a name="how-a-service-composes-its-spns"></a><span data-ttu-id="713c7-104">Come un servizio compone i relativi nomi SPN</span><span class="sxs-lookup"><span data-stu-id="713c7-104">How a Service Composes its SPNs</span></span>

<span data-ttu-id="713c7-105">Un servizio può utilizzare due funzioni per comporre i relativi nomi SPN: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) è una funzione generica per la composizione di SPN e [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) è una funzione specializzata per la composizione e la registrazione di nomi SPN semplici per un servizio basato su host.</span><span class="sxs-lookup"><span data-stu-id="713c7-105">A service can use two functions to compose its SPNs: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) is a general-purpose function for composing SPNs and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) is a specialized function for composing and registering simple SPNs for a host-based service.</span></span>

<span data-ttu-id="713c7-106">Un programma di installazione del servizio usa in genere la funzione [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) per comporre i nomi SPN, che vengono quindi registrati nell'account di accesso del servizio usando la funzione [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) .</span><span class="sxs-lookup"><span data-stu-id="713c7-106">A service installer typically uses the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose SPNs, which it then registers on the service's logon account using the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function.</span></span> <span data-ttu-id="713c7-107">**DsGetSpn** può eseguire le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="713c7-107">The **DsGetSpn** can perform the following functions.</span></span>

-   <span data-ttu-id="713c7-108">Creare un nome SPN semplice con il <service class> / <host> formato "" per un servizio basato su host.</span><span class="sxs-lookup"><span data-stu-id="713c7-108">Create a simple SPN with the "<service class>/<host>" format for a host-based service.</span></span>
-   <span data-ttu-id="713c7-109">Creare un nome SPN complesso che includa il &lt; componente "nome servizio &gt; " utilizzato dai servizi replicabili o il &lt; componente "porta &gt; " che distingue più istanze di un servizio in un singolo host.</span><span class="sxs-lookup"><span data-stu-id="713c7-109">Create a complex SPN that includes the "&lt;service name&gt;" component used by replicable services or the "&lt;port&gt;" component that distinguishes multiple instances of a service on a single host.</span></span>
-   <span data-ttu-id="713c7-110">Per impostazione predefinita, creare un singolo SPN con il &lt; componente "host &gt; " impostato sul nome di un host specificato o sul nome del computer locale.</span><span class="sxs-lookup"><span data-stu-id="713c7-110">Create a single SPN with the "&lt;host&gt;" component set to either the name of a specified host or the name of the local computer by default.</span></span>
-   <span data-ttu-id="713c7-111">Creare una matrice di nomi SPN per più istanze del servizio che vengono eseguite su più host in tutta la foresta.</span><span class="sxs-lookup"><span data-stu-id="713c7-111">Create an array of SPNs for multiple service instances that will run on multiple hosts throughout the forest.</span></span> <span data-ttu-id="713c7-112">Ogni SPN specifica il nome dell'host per un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="713c7-112">Each SPN specifies the name of the host for a service instance.</span></span>
-   <span data-ttu-id="713c7-113">Creare una matrice di nomi SPN per più istanze del servizio che vengono eseguite nello stesso host.</span><span class="sxs-lookup"><span data-stu-id="713c7-113">Create an array of SPNs for multiple service instances that will run on the same host.</span></span> <span data-ttu-id="713c7-114">Ogni SPN specifica il nome dell'host e un numero di porta per un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="713c7-114">Each SPN specifies the name of the host and a port number for a service instance.</span></span>

<span data-ttu-id="713c7-115">La matrice di nomi restituiti da [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) deve essere liberata chiamando la funzione [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) .</span><span class="sxs-lookup"><span data-stu-id="713c7-115">The array of names returned by [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) must be freed by calling the [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) function.</span></span>

<span data-ttu-id="713c7-116">Tenere presente che le funzioni [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)e [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) non verificano che i nomi SPN siano univoci.</span><span class="sxs-lookup"><span data-stu-id="713c7-116">Be aware that the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna), and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) functions do not verify that SPNs are unique.</span></span> <span data-ttu-id="713c7-117">Poiché l'autenticazione reciproca non riesce se un client presenta un nome SPN non univoco, verificare l'univocità prima di registrare un nome SPN.</span><span class="sxs-lookup"><span data-stu-id="713c7-117">Because mutual authentication fails if a client presents an SPN that is not unique, verify uniqueness before registering an SPN.</span></span> <span data-ttu-id="713c7-118">A tale scopo, eseguire una ricerca nel catalogo globale (GC) per gli attributi **servicePrincipalName** che corrispondono al nome SPN.</span><span class="sxs-lookup"><span data-stu-id="713c7-118">To do this, search the global catalog (GC) for **servicePrincipalName** attributes that match your SPN.</span></span> <span data-ttu-id="713c7-119">Per ulteriori informazioni sulla ricerca nel GC, vedere la pagina relativa alla [ricerca nel catalogo globale](searching-global-catalog-contents.md).</span><span class="sxs-lookup"><span data-stu-id="713c7-119">For more information about searching the GC, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 




