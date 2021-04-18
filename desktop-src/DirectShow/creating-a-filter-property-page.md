---
description: Creazione di una pagina delle proprietà del filtro
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Creazione di una pagina delle proprietà del filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cc19bf918ba47c53a04e34f5e5292bfdc716eca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303972"
---
# <a name="creating-a-filter-property-page"></a><span data-ttu-id="01036-103">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="01036-103">Creating a Filter Property Page</span></span>

<span data-ttu-id="01036-104">Questa sezione descrive come creare una pagina delle proprietà per un filtro DirectShow personalizzato, usando la classe [**CBasePropertyPage**](cbasepropertypage.md) .</span><span class="sxs-lookup"><span data-stu-id="01036-104">This section describes how to create a property page for a custom DirectShow filter, using the [**CBasePropertyPage**](cbasepropertypage.md) class.</span></span> <span data-ttu-id="01036-105">Il codice di esempio riportato in questa sezione illustra tutti i passaggi necessari per creare una pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="01036-105">The example code in this section shows all the steps needed to create a property page.</span></span> <span data-ttu-id="01036-106">Nell'esempio viene illustrata una pagina delle proprietà per un filtro effetto video ipotetico che supporta una proprietà saturazione.</span><span class="sxs-lookup"><span data-stu-id="01036-106">The example shows a property page for a hypothetical video effect filter that supports a saturation property.</span></span> <span data-ttu-id="01036-107">La pagina delle proprietà dispone di un dispositivo di scorrimento, che può essere spostato dall'utente per regolare il livello di saturazione del filtro.</span><span class="sxs-lookup"><span data-stu-id="01036-107">The property page has a slider, which the user can move to adjust the filter's saturation level.</span></span>

<span data-ttu-id="01036-108">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="01036-108">This section contains the following topics:</span></span>

-   [<span data-ttu-id="01036-109">Passaggio 1. Definire un meccanismo per l'impostazione della proprietà</span><span class="sxs-lookup"><span data-stu-id="01036-109">Step 1. Define a Mechanism for Setting the Property</span></span>](step-1--define-a-mechanism-for-setting-the-property.md)
-   [<span data-ttu-id="01036-110">Passaggio 2. Implementare ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="01036-110">Step 2. Implement ISpecifyPropertyPages</span></span>](step-2--implement-ispecifypropertypages.md)
-   [<span data-ttu-id="01036-111">Passaggio 3. Supporta QueryInterface</span><span class="sxs-lookup"><span data-stu-id="01036-111">Step 3. Support QueryInterface</span></span>](step-3--support-queryinterface.md)
-   [<span data-ttu-id="01036-112">Passaggio 4. Creazione della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="01036-112">Step 4. Create the Property Page</span></span>](step-4--create-the-property-page.md)
-   [<span data-ttu-id="01036-113">Passaggio 5. Archiviare un puntatore al filtro</span><span class="sxs-lookup"><span data-stu-id="01036-113">Step 5. Store a Pointer to the Filter</span></span>](step-5--store-a-pointer-to-the-filter.md)
-   [<span data-ttu-id="01036-114">Passaggio 6. Inizializzare la finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="01036-114">Step 6. Initialize the Dialog</span></span>](step-6--initialize-the-dialog.md)
-   [<span data-ttu-id="01036-115">Passaggio 7. Gestire i messaggi della finestra</span><span class="sxs-lookup"><span data-stu-id="01036-115">Step 7. Handle Window Messages</span></span>](step-7--handle-window-messages.md)
-   [<span data-ttu-id="01036-116">Passaggio 8. Applicare le modifiche alle proprietà</span><span class="sxs-lookup"><span data-stu-id="01036-116">Step 8. Apply Property Changes</span></span>](step-8--apply-property-changes.md)
-   [<span data-ttu-id="01036-117">Passaggio 9. Disconnettere la pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="01036-117">Step 9. Disconnect the Property Page</span></span>](step-9--disconnect-the-property-page.md)
-   [<span data-ttu-id="01036-118">Passaggio 10. Supporto della registrazione COM</span><span class="sxs-lookup"><span data-stu-id="01036-118">Step 10. Support COM Registration</span></span>](step-10--support-com-registration.md)

## <a name="related-topics"></a><span data-ttu-id="01036-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="01036-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01036-120">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="01036-120">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



