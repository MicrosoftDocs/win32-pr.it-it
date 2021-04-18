---
description: Gestione degli errori di amministrazione COM+
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Gestione degli errori di amministrazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304950"
---
# <a name="handling-com-administration-errors"></a><span data-ttu-id="2af68-103">Gestione degli errori di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="2af68-103">Handling COM+ Administration Errors</span></span>

<span data-ttu-id="2af68-104">Gli errori generati quando si utilizzano gli oggetti COMAdmin vengono segnalati in due modi, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2af68-104">Errors that are generated when using the COMAdmin objects are reported in two ways, as follows:</span></span>

-   <span data-ttu-id="2af68-105">Utilizzo di codici di errore specifici della libreria COMAdmin.</span><span class="sxs-lookup"><span data-stu-id="2af68-105">Using error codes specific to the COMAdmin library.</span></span>
-   <span data-ttu-id="2af68-106">Uso delle informazioni estese sull'errore disponibili in una raccolta [**errorInfo**](errorinfo.md) speciale.</span><span class="sxs-lookup"><span data-stu-id="2af68-106">Using extended error information available in a special [**ErrorInfo**](errorinfo.md) collection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2af68-107">Codici errore</span><span class="sxs-lookup"><span data-stu-id="2af68-107">Error Codes</span></span>

<span data-ttu-id="2af68-108">I codici di errore di amministrazione vengono gestiti come tutti i messaggi di errore COM.</span><span class="sxs-lookup"><span data-stu-id="2af68-108">You handle administration error codes as you would any COM error message.</span></span> <span data-ttu-id="2af68-109">In Microsoft Visual C++, questi codici vengono restituiti come valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2af68-109">In Microsoft Visual C++, these codes are returned as **HRESULT** values.</span></span> <span data-ttu-id="2af68-110">In Microsoft Visual Basic vengono generate come eccezioni che è possibile intercettare.</span><span class="sxs-lookup"><span data-stu-id="2af68-110">In Microsoft Visual Basic, they are thrown as exceptions that you can catch.</span></span> <span data-ttu-id="2af68-111">Per i programmatori C++, i codici di errore di amministrazione COM+ sono definiti in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="2af68-111">For C++ programmers, the COM+ administration error codes are defined in Winerror.h.</span></span> <span data-ttu-id="2af68-112">Per i programmatori Visual Basic, sono disponibili tramite l'IDE di Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2af68-112">For Visual Basic programmers, they are available through the Visual Basic IDE.</span></span>

## <a name="errorinfo-collection"></a><span data-ttu-id="2af68-113">Raccolta ErrorInfo</span><span class="sxs-lookup"><span data-stu-id="2af68-113">ErrorInfo Collection</span></span>

<span data-ttu-id="2af68-114">Quando si verifica un errore, segnalato da un tipo di codice di errore, potrebbero essere disponibili informazioni più dettagliate, a seconda della natura dell'errore.</span><span class="sxs-lookup"><span data-stu-id="2af68-114">When an error occurs, signaled by some kind of failure code, more detailed information may be available, depending on the nature of the error.</span></span> <span data-ttu-id="2af68-115">Gli oggetti COMAdmin forniscono informazioni estese nei casi in cui la ragione precisa dell'errore è difficile da determinare senza un report dettagliato, ad esempio con più operazioni di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="2af68-115">The COMAdmin objects provide extended information in circumstances where the precise cause of the failure is difficult to determine without a detailed report, such as with multiple read and write operations.</span></span>

<span data-ttu-id="2af68-116">Ad esempio, quando si usano metodi quali [**popolare**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) in un oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , è possibile leggere o scrivere dati per ogni elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="2af68-116">For example, when you use methods such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, you can be reading or writing data for every item in the collection.</span></span> <span data-ttu-id="2af68-117">Possono verificarsi errori complessi e possono essere difficili da diagnosticare in base a un singolo codice di errore numerico.</span><span class="sxs-lookup"><span data-stu-id="2af68-117">Complicated errors can occur, and they can be difficult to diagnose based on a single numeric error code.</span></span> <span data-ttu-id="2af68-118">Pertanto, la libreria COMAdmin crea informazioni estese sugli errori tramite una raccolta speciale.</span><span class="sxs-lookup"><span data-stu-id="2af68-118">Therefore, the COMAdmin Library makes extended error information through a special collection.</span></span>

<span data-ttu-id="2af68-119">Quando sono disponibili informazioni estese sugli errori, questo viene inserito nella raccolta [**errorInfo**](errorinfo.md) correlata alla raccolta originale in cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="2af68-119">When extended error information is available, it is placed in the [**ErrorInfo**](errorinfo.md) collection that is related to the original collection that had the error.</span></span> <span data-ttu-id="2af68-120">Per recuperare la segnalazione errori, ottenere la raccolta **errorInfo** correlata alla raccolta originale ed esaminare gli elementi che contiene.</span><span class="sxs-lookup"><span data-stu-id="2af68-120">To retrieve the error report, get the **ErrorInfo** collection that is related to the original collection and examine the items it contains.</span></span> <span data-ttu-id="2af68-121">È possibile recuperare la raccolta **errorInfo** usando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) in [**COMAdminCatalogCollection**](comadmincatalogcollection.md), lasciando vuoto il secondo parametro, dove normalmente si specifica la proprietà chiave di un elemento padre.</span><span class="sxs-lookup"><span data-stu-id="2af68-121">You can retrieve the **ErrorInfo** collection by using [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on [**COMAdminCatalogCollection**](comadmincatalogcollection.md), leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

<span data-ttu-id="2af68-122">Quando viene ricevuto un errore, è necessario ottenere immediatamente e popolare la raccolta [**errorInfo**](errorinfo.md) per la raccolta che ha avuto esito negativo, senza eseguire altre operazioni su tale raccolta.</span><span class="sxs-lookup"><span data-stu-id="2af68-122">When you get an error, you must immediately get and populate the [**ErrorInfo**](errorinfo.md) collection for the collection that failed, without performing any other operations on that collection.</span></span> <span data-ttu-id="2af68-123">In caso contrario, la raccolta **errorInfo** viene reimpostata e non descrive in dettaglio l'errore.</span><span class="sxs-lookup"><span data-stu-id="2af68-123">Otherwise, the **ErrorInfo** collection is reset and does not detail that failure.</span></span>

<span data-ttu-id="2af68-124">Gli elementi nella raccolta [**errorInfo**](errorinfo.md) espongono le proprietà speciali per la segnalazione degli errori MajorRef e MinorRef, che descrivono in dettaglio la particolare origine dell'errore.</span><span class="sxs-lookup"><span data-stu-id="2af68-124">The items in the [**ErrorInfo**](errorinfo.md) collection expose the special error-reporting properties MajorRef and MinorRef, which detail the particular cause of the error.</span></span> <span data-ttu-id="2af68-125">Per ulteriori informazioni, vedere **errorInfo**.</span><span class="sxs-lookup"><span data-stu-id="2af68-125">For more information, see **ErrorInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2af68-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2af68-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2af68-127">Operazioni di amministrazione COM+ all'interno delle transazioni</span><span class="sxs-lookup"><span data-stu-id="2af68-127">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="2af68-128">Esempio introduttivo di utilizzo del catalogo di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="2af68-128">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="2af68-129">Panoramica degli oggetti COMAdmin</span><span class="sxs-lookup"><span data-stu-id="2af68-129">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="2af68-130">Recupero di raccolte nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="2af68-130">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="2af68-131">Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="2af68-131">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



