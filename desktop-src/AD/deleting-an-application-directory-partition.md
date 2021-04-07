---
title: Eliminazione di una partizione di directory applicativa
description: Una partizione di directory applicativa viene eliminata eliminando l'oggetto crossRef che rappresenta la partizione di directory applicativa.
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- Eliminazione di un annuncio della partizione di directory applicativa
- AD, eliminazione delle partizioni di directory applicative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724575"
---
# <a name="deleting-an-application-directory-partition"></a><span data-ttu-id="03104-105">Eliminazione di una partizione di directory applicativa</span><span class="sxs-lookup"><span data-stu-id="03104-105">Deleting an Application Directory Partition</span></span>

<span data-ttu-id="03104-106">Una partizione di directory applicativa viene eliminata eliminando l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresenta la partizione di directory applicativa.</span><span class="sxs-lookup"><span data-stu-id="03104-106">An application directory partition is deleted by deleting the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition.</span></span> <span data-ttu-id="03104-107">Quando l'eliminazione dell'oggetto **crossRef** viene replicata in un controller di dominio che dispone di una replica della partizione di directory applicativa, il KCC eliminerà la replica locale della partizione di directory applicativa.</span><span class="sxs-lookup"><span data-stu-id="03104-107">When the deletion of the **crossRef** object replicates to a domain controller that has a replica of the application directory partition, the KCC will delete the local replica of the application directory partition.</span></span> <span data-ttu-id="03104-108">Questa operazione provoca l'eliminazione di tutte le repliche della partizione di directory applicativa.</span><span class="sxs-lookup"><span data-stu-id="03104-108">This eventually causes all replicas of the application directory partition to be deleted.</span></span>

<span data-ttu-id="03104-109">Quando l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) viene eliminato, il server di Active Directory eliminerà l'oggetto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) creato al momento della creazione della partizione di directory applicativa, oltre a eliminare tutti gli oggetti nella partizione di directory applicativa.</span><span class="sxs-lookup"><span data-stu-id="03104-109">When the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is deleted, the Active Directory server will delete the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object that was created when the application directory partition was created, as well as deleting all objects in the application directory partition.</span></span> <span data-ttu-id="03104-110">Nessuno degli oggetti nella partizione di directory applicativa viene contrassegnato per la rimozione definitiva al momento dell'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="03104-110">None of the objects in the application directory partition are tombstoned when they deleted.</span></span>

<span data-ttu-id="03104-111">Quando viene eliminata una partizione di directory applicativa, è molto difficile ripristinarla.</span><span class="sxs-lookup"><span data-stu-id="03104-111">When an application directory partition is deleted, it is very difficult to restore it.</span></span> <span data-ttu-id="03104-112">Per ripristinare una partizione di directory applicativa, è necessario ripristinare un backup con una replica della partizione di directory applicativa, trovare l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresenta la partizione di directory applicativa e ripristinare l'oggetto **crossRef** in modo autorevole.</span><span class="sxs-lookup"><span data-stu-id="03104-112">To restore an application directory partition, it is necessary to restore a backup that has a replica of the application directory partition, find the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition and authoritatively restore the **crossRef** object.</span></span>

<span data-ttu-id="03104-113">**Per eliminare una partizione di directory applicativa e le relative repliche, seguire questa procedura**</span><span class="sxs-lookup"><span data-stu-id="03104-113">**To delete an application directory partition and its replicas, perform the following steps**</span></span>

1.  <span data-ttu-id="03104-114">Cercare nel contenitore partizioni un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con un valore di attributo [**NCName**](/windows/desktop/ADSchema/a-ncname) uguale al nome distinto della partizione di directory applicativa.</span><span class="sxs-lookup"><span data-stu-id="03104-114">Search the Partitions container for a [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that has an [**nCName**](/windows/desktop/ADSchema/a-ncname) attribute value that is equal to the distinguished name of the application directory partition.</span></span>
2.  <span data-ttu-id="03104-115">Eliminare l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) .</span><span class="sxs-lookup"><span data-stu-id="03104-115">Delete the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object.</span></span>

<span data-ttu-id="03104-116">Per ulteriori informazioni, vedere il [codice di esempio per l'eliminazione di una partizione di directory applicativa](example-code-for-deleting-an-application-directory-partition.md).</span><span class="sxs-lookup"><span data-stu-id="03104-116">For more information, see [Example Code for Deleting an Application Directory Partition](example-code-for-deleting-an-application-directory-partition.md).</span></span>

 

 