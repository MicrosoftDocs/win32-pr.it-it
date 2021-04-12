---
title: Classi ausiliarie collegate in modo dinamico
description: Una classe ausiliaria collegata dinamicamente è una classe collegata a un singolo oggetto, anziché a una classe di oggetti.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- Active Directory classi ausiliarie collegate in modo dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0cacb09d3aef05bcaf0ef729411c2e023469be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220946"
---
# <a name="dynamically-linked-auxiliary-classes"></a><span data-ttu-id="67425-104">Classi ausiliarie collegate in modo dinamico</span><span class="sxs-lookup"><span data-stu-id="67425-104">Dynamically Linked Auxiliary Classes</span></span>

<span data-ttu-id="67425-105">Una classe ausiliaria collegata dinamicamente è una classe collegata a un singolo oggetto, anziché a una classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="67425-105">A dynamically linked auxiliary class is a class that is attached to an individual object, rather than to an object class.</span></span> <span data-ttu-id="67425-106">Il collegamento dinamico consente di archiviare attributi aggiuntivi con un singolo oggetto senza l'effetto a livello di foresta dell'estensione della definizione dello schema per un'intera classe.</span><span class="sxs-lookup"><span data-stu-id="67425-106">Dynamic linking enables you to store additional attributes with an individual object without the forest-wide impact of extending the schema definition for an entire class.</span></span> <span data-ttu-id="67425-107">Ad esempio, un'azienda può utilizzare il collegamento dinamico per collegare una classe ausiliaria specifica alle vendite agli oggetti utente dei propri venditori e altre classi ausiliarie specifiche del reparto agli oggetti utente dei dipendenti in altri reparti.</span><span class="sxs-lookup"><span data-stu-id="67425-107">For example, an enterprise could use dynamic linking to attach a sales-specific auxiliary class to the user objects of its sales people, and other department-specific auxiliary classes to the user objects of employees in other departments.</span></span>

<span data-ttu-id="67425-108">Il collegamento dinamico non è complesso: aggiungere il nome della classe ausiliaria ai valori dell'attributo **objectClass** di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="67425-108">Dynamic linking is not complex: add the name of the auxiliary class to the values of an object's **objectClass** attribute.</span></span> <span data-ttu-id="67425-109">Se la classe ausiliaria ha attributi obbligatori (**musthave** o **systemMustHave**), è necessario impostarli nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="67425-109">If the auxiliary class has any mandatory attributes (**mustHave** or **systemMustHave**), you must set them at the same time.</span></span> <span data-ttu-id="67425-110">Per ulteriori informazioni e un esempio di codice, vedere [aggiunta di una classe ausiliaria a un'istanza dell'oggetto](adding-an-auxiliary-class-to-an-object-instance.md).</span><span class="sxs-lookup"><span data-stu-id="67425-110">For more information and a code example, see [Adding an Auxiliary Class to an Object Instance](adding-an-auxiliary-class-to-an-object-instance.md).</span></span>

<span data-ttu-id="67425-111">Per rimuovere una classe ausiliaria collegata dinamicamente, cancellare i valori di tutti gli attributi dalla classe ausiliaria, quindi rimuovere il nome della classe ausiliaria dall'attributo **objectClass** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="67425-111">To remove a dynamically linked auxiliary class, clear the values of all attributes from the auxiliary class, and then remove the name of the auxiliary class from the **objectClass** attribute of the object.</span></span>

<span data-ttu-id="67425-112">Se si aggiunge dinamicamente una classe ausiliaria che è una sottoclasse di un'altra classe ausiliaria, entrambe le classi ausiliarie vengono aggiunte all'oggetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="67425-112">If you dynamically add an auxiliary class that is a subclass of another auxiliary class, both auxiliary classes are added to the target object.</span></span> <span data-ttu-id="67425-113">Tuttavia, la rimozione della classe ausiliaria figlio non comporta la rimozione dell'elemento padre. ogni classe deve essere rimossa in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="67425-113">However, removing the child auxiliary class does not remove its parent; each class must be explicitly removed.</span></span>

 

 




