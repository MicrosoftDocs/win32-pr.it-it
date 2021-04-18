---
description: Le risorse necessarie per la personalizzazione di un'applicazione, ad esempio i modelli aziendali, possono essere distribuite con l'applicazione includendo una trasformazione con il pacchetto di installazione dell'applicazione.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Uso delle trasformazioni per aggiungere risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c11fac7ad65601286fb550abd950bf5ac49af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312311"
---
# <a name="using-transforms-to-add-resources"></a><span data-ttu-id="c7b5d-103">Uso delle trasformazioni per aggiungere risorse</span><span class="sxs-lookup"><span data-stu-id="c7b5d-103">Using Transforms to Add Resources</span></span>

<span data-ttu-id="c7b5d-104">Le risorse necessarie per la personalizzazione di un'applicazione, ad esempio i modelli aziendali, possono essere distribuite con l'applicazione includendo una trasformazione con il pacchetto di installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-104">Resources that are needed for the customization of an application, such as corporate templates, can be deployed with the application by including a transform with the application's installation package.</span></span> <span data-ttu-id="c7b5d-105">Quando si distribuiscono risorse, ad esempio file, chiavi del registro di sistema o collegamenti, è necessario attenersi alle regole seguenti, usando una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-105">The following rules should be followed when deploying resources, such as files, registry keys, or shortcuts, using a transform.</span></span>

-   <span data-ttu-id="c7b5d-106">La trasformazione deve aggiungere uno o più componenti nuovi al database di installazione per contenere le risorse aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-106">The transform should add one or more new components to the installation database to contain the additional resources.</span></span> <span data-ttu-id="c7b5d-107">La trasformazione non deve aggiungere risorse a un componente già esistente nell'installazione.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-107">The transform should not add resources to a component that already exists in the installation.</span></span>
-   <span data-ttu-id="c7b5d-108">La trasformazione deve aggiungere una o più nuove funzionalità al database di installazione per contenere questi nuovi componenti.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-108">The transform should add one or more new features to the installation database to contain these new components.</span></span> <span data-ttu-id="c7b5d-109">Queste nuove funzionalità non devono essere gli elementi padre di tutte le funzionalità esistenti, ma le nuove funzionalità padre e figlio possono essere introdotte insieme.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-109">These new features should not be the parents of any existing features, but new parent and child features may be introduced together.</span></span> <span data-ttu-id="c7b5d-110">Alle nuove funzionalità devono essere assegnati nomi univoci in tutte le altre trasformazioni per questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-110">New features should be given names that are unique across all other transforms for this product.</span></span> <span data-ttu-id="c7b5d-111">Due trasformazioni non devono mai aggiungere una funzionalità a questo prodotto con lo stesso nome elencato nella colonna feature della [tabella Feature](feature-table.md) e contenenti componenti o risorse differenti.</span><span class="sxs-lookup"><span data-stu-id="c7b5d-111">No two transforms should ever add a feature to this product that has the same name listed in the Feature column of the [Feature table](feature-table.md) and containing different components or resources.</span></span>

 

 



