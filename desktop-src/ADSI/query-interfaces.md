---
title: Interfacce di query
description: Per eseguire ricerche nella directory è possibile usare tre tipi di interfacce ADSI. L'ambiente dell'applicazione e altri requisiti possono indicare quale interfaccia viene utilizzata.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- Interfacce di query ADSI
- Query ADSI, interfacce di query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855261"
---
# <a name="query-interfaces"></a><span data-ttu-id="cd586-106">Interfacce di query</span><span class="sxs-lookup"><span data-stu-id="cd586-106">Query Interfaces</span></span>

<span data-ttu-id="cd586-107">Per eseguire ricerche nella directory è possibile usare tre tipi di interfacce ADSI.</span><span class="sxs-lookup"><span data-stu-id="cd586-107">Three types of ADSI interfaces can be used to perform directory searches.</span></span> <span data-ttu-id="cd586-108">L'ambiente dell'applicazione e altri requisiti possono indicare quale interfaccia viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd586-108">The application environment and other requirements may indicate which interface is used.</span></span>

-   <span data-ttu-id="cd586-109">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span><span class="sxs-lookup"><span data-stu-id="cd586-109">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="cd586-110">**IDirectorySearch** è un'interfaccia com di base disponibile solo per i programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="cd586-110">**IDirectorySearch** is a basic COM interface only available to C/C++ programmers.</span></span> <span data-ttu-id="cd586-111">Per ulteriori informazioni, vedere [ricerca con l'interfaccia IDirectorySearch](searching-with-idirectorysearch.md).</span><span class="sxs-lookup"><span data-stu-id="cd586-111">For more information, see [Searching With the IDirectorySearch Interface](searching-with-idirectorysearch.md).</span></span>
-   <span data-ttu-id="cd586-112">ADO.</span><span class="sxs-lookup"><span data-stu-id="cd586-112">ADO.</span></span> <span data-ttu-id="cd586-113">Le interfacce ADO (ActiveX Data Object) sono interfacce di automazione che utilizzano OLE DB.</span><span class="sxs-lookup"><span data-stu-id="cd586-113">The ActiveX Data Object (ADO) interfaces are Automation interfaces that use OLE DB.</span></span> <span data-ttu-id="cd586-114">Usare ADO per le query all'interno di applicazioni che si basano sull'automazione.</span><span class="sxs-lookup"><span data-stu-id="cd586-114">Use ADO for queries within applications that rely on Automation.</span></span> <span data-ttu-id="cd586-115">Sono incluse Visual Basic applicazioni, Active Server pagine e così via.</span><span class="sxs-lookup"><span data-stu-id="cd586-115">These include Visual Basic applications, Active Server Pages, and so on.</span></span> <span data-ttu-id="cd586-116">Per ulteriori informazioni, vedere [ricerca con ActiveX Data Objects](searching-with-activex-data-objects-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cd586-116">For more information, see [Searching with ActiveX Data Objects](searching-with-activex-data-objects-ado.md).</span></span>
-   <span data-ttu-id="cd586-117">OLE DB.</span><span class="sxs-lookup"><span data-stu-id="cd586-117">OLE DB.</span></span> <span data-ttu-id="cd586-118">OLE DB è un set di interfacce C/C++ utilizzate per eseguire query sui database.</span><span class="sxs-lookup"><span data-stu-id="cd586-118">OLE DB is a set of C/C++ interfaces used to query databases.</span></span> <span data-ttu-id="cd586-119">Grazie al supporto di queste interfacce, i provider ADSI possono implementare funzionalità di OLE DB avanzate, ad esempio query distribuite con altri provider di OLE DB.</span><span class="sxs-lookup"><span data-stu-id="cd586-119">By supporting these interfaces, ADSI providers can implement advanced OLE DB features, such as distributed queries with other OLE DB providers.</span></span> <span data-ttu-id="cd586-120">Per ulteriori informazioni, vedere [ricerca con OLE DB](searching-with-ole-db.md).</span><span class="sxs-lookup"><span data-stu-id="cd586-120">For more information, see [Searching with OLE DB](searching-with-ole-db.md).</span></span>

 

 




