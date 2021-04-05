---
title: Restrizioni sull'estensione dello schema
description: Per ridurre la possibilità di modifiche dello schema da parte di un'applicazione che suddivide altre applicazioni e per mantenere la coerenza dello schema, Active Directory Domain Services applicare restrizioni sul tipo di modifiche dello schema che possono essere apportate da un'applicazione o da un utente.
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c97ab3d9f6406a89b24c772e7df8254095f1286
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707567"
---
# <a name="restrictions-on-schema-extension"></a><span data-ttu-id="ed7f6-103">Restrizioni sull'estensione dello schema</span><span class="sxs-lookup"><span data-stu-id="ed7f6-103">Restrictions on Schema Extension</span></span>

<span data-ttu-id="ed7f6-104">Per ridurre la possibilità di modifiche dello schema da parte di un'applicazione che suddivide altre applicazioni e per mantenere la coerenza dello schema, Active Directory Domain Services applicare restrizioni sul tipo di modifiche dello schema che possono essere apportate da un'applicazione o da un utente.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-104">In order to reduce the possibility of schema changes by one application breaking other applications and to maintain schema consistency, Active Directory Domain Services enforce restrictions on the type of schema changes that an application or user is allowed to make.</span></span>

<span data-ttu-id="ed7f6-105">Le restrizioni vengono imposte solo sulla modifica degli oggetti dello schema esistenti.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-105">The restrictions are imposed only on modification of existing schema objects.</span></span> <span data-ttu-id="ed7f6-106">Lo schema è suddiviso in due categorie.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-106">The schema is categorized into two categories.</span></span> <span data-ttu-id="ed7f6-107">Gli oggetti dello schema forniti con Windows 2000 nello schema di base appartengono alla categoria 1.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-107">The schema objects that ship with Windows 2000 in the base schema belong to Category 1.</span></span> <span data-ttu-id="ed7f6-108">Tutti gli oggetti dello schema aggiunti in seguito da altre applicazioni o utenti tramite estensione dello schema dinamico appartengono alla categoria 2.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-108">Any schema objects added later by other applications or users through dynamic schema extension belong to Category 2.</span></span> <span data-ttu-id="ed7f6-109">La categoria di un oggetto dello schema può essere determinata dal bit 0x10 impostato nell'attributo **systemFlags** dell'oggetto **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="ed7f6-109">The category of a schema object can be determined by the 0x10 bit set in the **systemFlags** attribute on the **classSchema** object.</span></span> <span data-ttu-id="ed7f6-110">Questo bit viene impostato solo sugli oggetti di categoria 1 e non può essere modificato, né può essere impostato su qualsiasi oggetto di categoria 2.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-110">This bit is only set on Category 1 objects, and cannot be altered, nor can it be set on any Category 2 object.</span></span>

<span data-ttu-id="ed7f6-111">L'attributo **systemFlags** viene utilizzato internamente da Active Directory Domain Services per identificare le caratteristiche speciali degli oggetti "Infrastructure" nello schema di base.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-111">The **systemFlags** attribute is used internally by Active Directory Domain Services to identify special characteristics of "infrastructure" objects in the base schema.</span></span> <span data-ttu-id="ed7f6-112">Oltre a identificare gli oggetti di categoria 1, **systemFlags** controlla se un oggetto può essere spostato, eliminato o rinominato.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-112">In addition to identifying Category 1 objects, **systemFlags** controls whether an object can be moved, deleted, or renamed.</span></span> <span data-ttu-id="ed7f6-113">Queste operazioni sono evitate per gli oggetti da cui dipende Windows 2000 per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-113">These operations are prevented for objects that Windows 2000 depends on to run.</span></span>

<span data-ttu-id="ed7f6-114">Per tutti gli oggetti dello schema, categoria 1 o 2, Active Directory Domain Services impone le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ed7f6-114">On any schema objects, Category 1 or 2, Active Directory Domain Services impose the following restrictions:</span></span>

-   <span data-ttu-id="ed7f6-115">Non è possibile aggiungere un nuovo **mustContain** a una classe (direttamente o tramite ereditarietà mediante l'aggiunta di una classe ausiliaria).</span><span class="sxs-lookup"><span data-stu-id="ed7f6-115">You cannot add a new **mustContain** to a class (directly or through inheritance by adding an auxiliary class).</span></span>
-   <span data-ttu-id="ed7f6-116">Non è possibile eliminare **mustContain** della classe (direttamente o tramite ereditarietà).</span><span class="sxs-lookup"><span data-stu-id="ed7f6-116">You cannot delete any **mustContain** of the class (directly or through inheritance).</span></span>

<span data-ttu-id="ed7f6-117">Per gli oggetti dello schema di categoria 1 vengono inoltre applicate le restrizioni aggiuntive seguenti:</span><span class="sxs-lookup"><span data-stu-id="ed7f6-117">In addition, the following additional restrictions are imposed on Category 1 schema objects:</span></span>

-   <span data-ttu-id="ed7f6-118">Non è possibile modificare gli attributi seguenti di un attributo di categoria 1:</span><span class="sxs-lookup"><span data-stu-id="ed7f6-118">You cannot change the following attributes of a Category 1 attribute:</span></span>

    -   <span data-ttu-id="ed7f6-119">**RangeLower** e **rangeUpper** (intervallo di valori).</span><span class="sxs-lookup"><span data-stu-id="ed7f6-119">**rangeLower** and **rangeUpper** (value range).</span></span>
    -   <span data-ttu-id="ed7f6-120">**attributeSecurityGuid** (determina il set di proprietà a cui appartiene l'attributo, se presente).</span><span class="sxs-lookup"><span data-stu-id="ed7f6-120">**attributeSecurityGuid** (determines which property set the attribute belongs in, if any).</span></span>

-   <span data-ttu-id="ed7f6-121">Non è possibile modificare il **defaultObjectCategory** di una classe di categoria 1.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-121">You cannot change the **defaultObjectCategory** of a Category 1 class.</span></span>
-   <span data-ttu-id="ed7f6-122">Non è possibile modificare il **objectCategory** di un'istanza di una classe di categoria 1.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-122">You cannot change the **objectCategory** of any instance of a Category 1 class.</span></span>
-   <span data-ttu-id="ed7f6-123">Non è possibile rendere inattivo una classe o un attributo di categoria 1.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-123">You cannot make a Category 1 class or attribute defunct.</span></span>
-   <span data-ttu-id="ed7f6-124">Non è possibile modificare il **ldapDisplayName** di una classe o di un attributo di categoria 1.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-124">You cannot change the **lDAPDisplayName** of a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="ed7f6-125">Non è possibile rinominare una classe o un attributo di categoria 1.</span><span class="sxs-lookup"><span data-stu-id="ed7f6-125">You cannot rename a Category 1 class or attribute.</span></span>

 

 




