---
description: Salvataggio o eliminazione di modifiche
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Salvataggio o eliminazione di modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877493"
---
# <a name="saving-or-discarding-changes"></a><span data-ttu-id="eb041-103">Salvataggio o eliminazione di modifiche</span><span class="sxs-lookup"><span data-stu-id="eb041-103">Saving or Discarding Changes</span></span>

<span data-ttu-id="eb041-104">Quando si impostano le proprietà in un elemento, nessuna modifica viene effettivamente registrata nel catalogo COM+ fino a quando non si salvano in modo esplicito le modifiche.</span><span class="sxs-lookup"><span data-stu-id="eb041-104">When you set properties on an item, no changes are actually recorded to the COM+ catalog until you explicitly save changes.</span></span> <span data-ttu-id="eb041-105">A tale scopo, usare il metodo [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sull'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) per la raccolta che contiene l'elemento.</span><span class="sxs-lookup"><span data-stu-id="eb041-105">You do this using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object for the collection containing the item.</span></span>

<span data-ttu-id="eb041-106">Se si desidera annullare le modifiche di cui non è ancora stato eseguito il commit, è possibile chiamare il metodo [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) sull'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="eb041-106">If you want to discard changes that have not yet been committed, you can call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="eb041-107">Questa operazione consente di leggere tutti i dati persistenti dal catalogo COM+ per tutti gli elementi della raccolta, eliminando in tal modo tutte le modifiche in sospeso.</span><span class="sxs-lookup"><span data-stu-id="eb041-107">This reads in all persistent data from the COM+ catalog for all items in the collection, effectively deleting any pending changes.</span></span>

<span data-ttu-id="eb041-108">Quando si utilizza [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), le incoerenze nelle impostazioni delle proprietà selezionate generano un errore e **SaveChanges** non riesce a scrivere l'oggetto che ha restituito l'errore.</span><span class="sxs-lookup"><span data-stu-id="eb041-108">When you use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), any inconsistencies in property settings that you have chosen result in an error, and **SaveChanges** fails to write the object that returned the error.</span></span> <span data-ttu-id="eb041-109">Tutte le proprietà di un determinato elemento vengono scritte o non vengono scritte nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="eb041-109">All properties on a given item either are written or fail to be written as a whole.</span></span>

<span data-ttu-id="eb041-110">Tuttavia, quando si verificano errori di scrittura, è possibile che non siano dovute a impostazioni incompatibili; potrebbero essersi verificati altri errori.</span><span class="sxs-lookup"><span data-stu-id="eb041-110">However, when write errors occur, they might not be due to incompatible settings; some other failure might have occurred.</span></span> <span data-ttu-id="eb041-111">È necessario esaminare i dettagli dell'errore in modo da essere certi.</span><span class="sxs-lookup"><span data-stu-id="eb041-111">You need to inspect the details of the failure to be certain.</span></span> <span data-ttu-id="eb041-112">Per ulteriori informazioni, vedere [gestione degli errori di amministrazione com+](handling-com--administration-errors.md) e [interdipendenze tra le proprietà](interdependencies-between-properties.md).</span><span class="sxs-lookup"><span data-stu-id="eb041-112">For more information, see [Handling COM+ Administration Errors](handling-com--administration-errors.md) and [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="eb041-113">Come regola generale, maggiore è il numero di modifiche che si tenta di salvare in una sola volta, in particolare modifiche a più oggetti, più è probabile che si ottenga un errore e più difficile tenere traccia del problema.</span><span class="sxs-lookup"><span data-stu-id="eb041-113">As a general rule, the more changes you attempt to save at once, particularly changes to multiple objects, the more likely you are to get an error and the more difficult it is to track down.</span></span>

<span data-ttu-id="eb041-114">Inoltre, tra le chiamate a [**popolare**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), non è presente un blocco sugli elementi nella raccolta; la contesa è possibile.</span><span class="sxs-lookup"><span data-stu-id="eb041-114">Additionally, between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), you do not have a lock on the items in the collection; contention is possible.</span></span> <span data-ttu-id="eb041-115">Per informazioni dettagliate, vedere [recupero e impostazione delle proprietà](getting-and-setting-properties.md).</span><span class="sxs-lookup"><span data-stu-id="eb041-115">For more details, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb041-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb041-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb041-117">Recupero e impostazione delle proprietà</span><span class="sxs-lookup"><span data-stu-id="eb041-117">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="eb041-118">Interdipendenze tra proprietà</span><span class="sxs-lookup"><span data-stu-id="eb041-118">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="eb041-119">Esecuzione di query per le proprietà disponibili</span><span class="sxs-lookup"><span data-stu-id="eb041-119">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> </dl>

 

 



