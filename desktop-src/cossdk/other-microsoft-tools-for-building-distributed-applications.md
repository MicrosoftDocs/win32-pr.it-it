---
description: Altri strumenti Microsoft per la creazione di applicazioni distribuite
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Altri strumenti Microsoft per la creazione di applicazioni distribuite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d65bd7c61a73bedb9463e8558415c7b27fe04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305136"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a><span data-ttu-id="5e0a0-103">Altri strumenti Microsoft per la creazione di applicazioni distribuite</span><span class="sxs-lookup"><span data-stu-id="5e0a0-103">Other Microsoft Tools for Building Distributed Applications</span></span>

<span data-ttu-id="5e0a0-104">Oltre agli strumenti di COM+, Microsoft offre gli strumenti seguenti per aiutare gli sviluppatori nella creazione di applicazioni distribuite:</span><span class="sxs-lookup"><span data-stu-id="5e0a0-104">In addition to the tools in COM+, Microsoft provides the following tools to assist the developer in creating distributed applications:</span></span>

-   <span data-ttu-id="5e0a0-105">Microsoft Data Access Components (MDAC).</span><span class="sxs-lookup"><span data-stu-id="5e0a0-105">Microsoft Data Access Components (MDAC).</span></span> <span data-ttu-id="5e0a0-106">Microsoft offre diverse vie per il recupero di dati da una miriade di origini.</span><span class="sxs-lookup"><span data-stu-id="5e0a0-106">Microsoft provides several avenues for retrieving data from a myriad of sources.</span></span> <span data-ttu-id="5e0a0-107">OLE DB, ad esempio, offre un set di interfacce COM per la compilazione di componenti di database.</span><span class="sxs-lookup"><span data-stu-id="5e0a0-107">For example, OLE DB offers a set of COM interfaces for building database components.</span></span> <span data-ttu-id="5e0a0-108">Le interfacce sono definite in modo che i provider di dati possano implementare livelli di supporto diversi, in base alle funzionalità dell'archivio dati sottostante.</span><span class="sxs-lookup"><span data-stu-id="5e0a0-108">The interfaces are defined so that data providers can implement different levels of support, based on the capabilities of the underlying data store.</span></span> <span data-ttu-id="5e0a0-109">Poiché OLE DB è basato su COM, può essere facilmente esteso e le estensioni vengono implementate come nuove interfacce.</span><span class="sxs-lookup"><span data-stu-id="5e0a0-109">Because OLE DB is COM-based, it can easily be extended, and extensions are implemented as new interfaces.</span></span> <span data-ttu-id="5e0a0-110">OLE DB include anche un'interfaccia di programmazione a livello di applicazione, denominata ActiveX Data Objects (ADO).</span><span class="sxs-lookup"><span data-stu-id="5e0a0-110">OLE DB also includes an application-level programming interface, called ActiveX Data Objects (ADO).</span></span> <span data-ttu-id="5e0a0-111">ADO espone le interfacce duali, in modo che possa essere usato facilmente da linguaggi di scripting, nonché Microsoft Visual C++, Visual Basic e altri strumenti di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="5e0a0-111">ADO exposes dual interfaces, so it can easily be used from scripting languages as well as Microsoft Visual C++, Visual Basic, and other developer tools.</span></span>

    > [!Note]  
    > <span data-ttu-id="5e0a0-112">Gli sviluppatori possono anche scegliere di usare un'API generica e indipendente dal fornitore, ad esempio Microsoft Open Database Connectivity (ODBC) Application Programming Interface (API).</span><span class="sxs-lookup"><span data-stu-id="5e0a0-112">Developers can also choose to use a generic, vendor-neutral API such as the Microsoft Open Database Connectivity (ODBC) application programming interface (API).</span></span> <span data-ttu-id="5e0a0-113">L'API ODBC è un'interfaccia del linguaggio C per accedere ai dati in un sistema DBMS utilizzando Structured Query Language (SQL).</span><span class="sxs-lookup"><span data-stu-id="5e0a0-113">The ODBC API is a C language interface for accessing data in a DBMS by using Structured Query Language (SQL).</span></span> <span data-ttu-id="5e0a0-114">Gestione driver ODBC fornisce l'interfaccia di programmazione e i componenti di runtime per individuare i driver specifici del sistema DBMS.</span><span class="sxs-lookup"><span data-stu-id="5e0a0-114">An ODBC driver manager provides the programming interface and run-time components to locate DBMS-specific drivers.</span></span> <span data-ttu-id="5e0a0-115">I driver ODBC, in genere forniti dal fornitore del sistema DBMS, convertono chiamate generiche da Gestione driver ODBC in chiamate al metodo di accesso ai dati nativi.</span><span class="sxs-lookup"><span data-stu-id="5e0a0-115">ODBC drivers, typically supplied by the DBMS vendor, translate generic calls from the ODBC driver manager into calls to the native data access method.</span></span> <span data-ttu-id="5e0a0-116">Il vantaggio principale dell'utilizzo dell'API ODBC è che è necessario apprendere una sola API per accedere a un'ampia gamma di sistemi DBMS.</span><span class="sxs-lookup"><span data-stu-id="5e0a0-116">The primary advantage of using the ODBC API is that you need to learn only one API to access a wide range of DBMSs.</span></span>

     

-   <span data-ttu-id="5e0a0-117">Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5e0a0-117">Microsoft SQL Server.</span></span> <span data-ttu-id="5e0a0-118">Oltre a fornire un sistema di database relazionale solido ed eloquente, Microsoft SQL Server possibile fornire un'applicazione distribuita con pool di connessioni e sicurezza che può integrarsi con il modello di sicurezza di Windows.</span><span class="sxs-lookup"><span data-stu-id="5e0a0-118">In addition to providing a robust and eloquent relational database system, Microsoft SQL Server can provide a distributed application with connection pooling and security that can integrate with the Windows security model.</span></span>

-   <span data-ttu-id="5e0a0-119">Integrazione delle transazioni COM (COMTI).</span><span class="sxs-lookup"><span data-stu-id="5e0a0-119">COM Transaction Integration (COMTI).</span></span> <span data-ttu-id="5e0a0-120">COMTI può essere usato per integrare i sistemi mainframe nei sistemi Windows, incluse le applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="5e0a0-120">COMTI can be used to integrate mainframe systems into Windows systems, including COM+ applications.</span></span> <span data-ttu-id="5e0a0-121">COMTI usa protocolli di comunicazione standard (ad esempio, LU 6,2) per la comunicazione tra computer Windows e mainframe e minicomputer.</span><span class="sxs-lookup"><span data-stu-id="5e0a0-121">COMTI uses standard communication protocols (for example, LU 6.2) for communicating between Windows computers and mainframe and minicomputers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e0a0-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5e0a0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e0a0-123">Presupposti e principi di progettazione COM+</span><span class="sxs-lookup"><span data-stu-id="5e0a0-123">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="5e0a0-124">Progettazione dell'applicazione COM+ tramite UML</span><span class="sxs-lookup"><span data-stu-id="5e0a0-124">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="5e0a0-125">Suggerimenti di progettazione generali per l'utilizzo di COM+</span><span class="sxs-lookup"><span data-stu-id="5e0a0-125">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="5e0a0-126">Ottimizzazione delle interazioni con il livello di logica di business COM+</span><span class="sxs-lookup"><span data-stu-id="5e0a0-126">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



