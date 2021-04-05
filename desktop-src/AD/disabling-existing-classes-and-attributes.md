---
title: Disabilitazione di classi e attributi esistenti
description: Le aggiunte dello schema sono permanenti.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74863d0d3c72f383259cfe262f4b7aa6fa27774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707714"
---
# <a name="disabling-existing-classes-and-attributes"></a><span data-ttu-id="b9b7f-103">Disabilitazione di classi e attributi esistenti</span><span class="sxs-lookup"><span data-stu-id="b9b7f-103">Disabling Existing Classes and Attributes</span></span>

<span data-ttu-id="b9b7f-104">Le aggiunte dello schema sono permanenti.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-104">Schema additions are permanent.</span></span> <span data-ttu-id="b9b7f-105">Non è possibile eliminare gli oggetti **attributeSchema** e **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="b9b7f-105">You cannot delete **attributeSchema** and **classSchema** objects.</span></span> <span data-ttu-id="b9b7f-106">In un sistema distribuito è difficile garantire che non esistano istanze di una determinata classe o attributo.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-106">In a distributed system, it is difficult to guarantee that there are no instances of a given class or attribute.</span></span> <span data-ttu-id="b9b7f-107">Se si rimuove la definizione di una classe o di un attributo, vengono danneggiate le istanze esistenti di tale classe o attributo.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-107">Removing the definition of a class or attribute damages existing instances of that class or attribute.</span></span>

<span data-ttu-id="b9b7f-108">È possibile disabilitare una classe o un attributo esistente contrassegnando il valore come "inattivo".</span><span class="sxs-lookup"><span data-stu-id="b9b7f-108">You can disable an existing class or attribute by marking it as "defunct".</span></span> <span data-ttu-id="b9b7f-109">Questa operazione non influisce sulle istanze esistenti della classe o dell'attributo in modo che siano contrassegnate, ma impedisce la creazione di nuove istanze.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-109">This does not affect existing instances of the class or attribute so marked, but it prevents the creation of new instances.</span></span>

<span data-ttu-id="b9b7f-110">Quando si disabilitano le classi e gli attributi dello schema, si applicano le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9b7f-110">The following restrictions apply when disabling schema classes and attributes:</span></span>

-   <span data-ttu-id="b9b7f-111">Non è possibile disabilitare una classe o un attributo di categoria 1.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-111">You cannot disable a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="b9b7f-112">Non è possibile disabilitare un attributo che è membro di una classe non anche disabilitata.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-112">You cannot disable an attribute that is a member of a class that is not also disabled.</span></span> <span data-ttu-id="b9b7f-113">Questo perché un attributo potrebbe essere necessario per la classe (non disabilitata) e la disabilitazione dell'attributo impedisce la creazione di nuove istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-113">This is because an attribute might be required for the (not disabled) class, and disabling the attribute prevents new instances of the class from being created.</span></span>

<span data-ttu-id="b9b7f-114">Per disabilitare **un attributo, impostare l'attributo** disattivo dell'oggetto **attributeSchema** su **true**.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-114">To disable an attribute, set the **isDefunct** attribute of its **attributeSchema** object to **TRUE**.</span></span> <span data-ttu-id="b9b7f-115">Quando un attributo è disabilitato, non è possibile creare nuove istanze dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-115">When an attribute is disabled, new instances of the attribute cannot be created.</span></span> <span data-ttu-id="b9b7f-116">Per abilitare nuovamente **l'attributo, impostare l'attributo** IsEnabled su **false**.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-116">To re-enable the attribute set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="b9b7f-117">Per disabilitare una classe, **impostare l'attributo disattivo dell'** oggetto **classSchema** su **true**.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-117">To disable a class, set the **isDefunct** attribute of its **classSchema** object to **TRUE**.</span></span> <span data-ttu-id="b9b7f-118">Quando una classe è disabilitata, non è possibile creare nuove istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-118">When a class is disabled, new instances of the class cannot be created.</span></span> <span data-ttu-id="b9b7f-119">Per abilitare nuovamente la classe, impostare l' **attributo IsEnabled** su **false**.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-119">To re-enable the class set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="b9b7f-120">L'impostazione di oggetti dello schema come inattivo può essere utile negli ambienti di produzione.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-120">Setting schema objects as defunct can be useful in production environments.</span></span> <span data-ttu-id="b9b7f-121">Quando una versione di test di un'estensione dello schema non è più necessaria, contrassegnarla come inattiva.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-121">When a test version of a schema extension is no longer required, mark it as defunct.</span></span> <span data-ttu-id="b9b7f-122">È possibile ripristinarlo rimuovendo l'attributo **Indefunto** o impostando il valore dell'attributo su **false**.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-122">You can restore it by removing the **isDefunct** attribute or setting the attribute value to **FALSE**.</span></span> <span data-ttu-id="b9b7f-123">In questo modo si protegge anche da una rimozione non intenzionale di un oggetto dello schema, impostando il campo come inattivo perché l'operazione può essere annullata facilmente.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-123">This also protects against an unintended removal of a schema object by setting it to defunct because the operation can be easily reversed.</span></span>

<span data-ttu-id="b9b7f-124">Tenere presente che il server Active Directory non esegue la pulizia delle istanze esistenti di un attributo o di una classe quando si rende inattivo un oggetto dello schema.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-124">Be aware that the Active Directory server does not clean up existing instances of an attribute or class when you make a schema object defunct.</span></span> <span data-ttu-id="b9b7f-125">Se si **rimuove la proprietà IsValid, le istanze** diventeranno di nuovo validi oggetti normali.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-125">If you remove the **isDefunct** property, any instances become valid, normal objects again.</span></span>

<span data-ttu-id="b9b7f-126">L'elenco seguente include altre conseguenze del contrassegno di un oggetto **attributeSchema** o **classSchema** inattivo:</span><span class="sxs-lookup"><span data-stu-id="b9b7f-126">The following list includes other consequences of marking an **attributeSchema** or **classSchema** object defunct:</span></span>

-   <span data-ttu-id="b9b7f-127">L'aggiunta o la modifica di un'istanza non riesce.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-127">Addition or modification of an instance fails.</span></span>
-   <span data-ttu-id="b9b7f-128">I codici di errore si comportano come se una classe inattiva non esisteva.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-128">Error codes behave as if a defunct class never existed.</span></span>
-   <span data-ttu-id="b9b7f-129">La ricerca e l'eliminazione si comportano come se non fossero stati resi inattivi gli oggetti dello schema.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-129">Search and delete behave as if no schema objects have been made defunct.</span></span>
-   <span data-ttu-id="b9b7f-130">Consente solo l'eliminazione dell'intero attributo dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-130">Only allow deleting entire attribute from object.</span></span>

<span data-ttu-id="b9b7f-131">Nell'elenco seguente sono incluse opzioni aggiuntive in un ambiente di produzione per ridurre l'impatto delle estensioni dello schema inattive:</span><span class="sxs-lookup"><span data-stu-id="b9b7f-131">The following list includes additional options in a production environment for reducing the impact of defunct schema extensions:</span></span>

-   <span data-ttu-id="b9b7f-132">Rimuovere tutti i valori dell'attributo **Faran** da una classe inattiva.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-132">Remove all **mayHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="b9b7f-133">Ridurre le dimensioni di tutti i valori dell'attributo **musthave** da una classe inattiva.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-133">Reduce the size of all **mustHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="b9b7f-134">Rimuovere un attributo inattivo dal catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-134">Remove a defunct attribute from the global catalog.</span></span>
-   <span data-ttu-id="b9b7f-135">Rimuovere un attributo inattivo da qualsiasi indice.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-135">Remove a defunct attribute from any index.</span></span>

<span data-ttu-id="b9b7f-136">Altre opzioni per la rimozione di modifiche dello schema indesiderate in un ambiente di produzione sono destinate agli sviluppatori a utilizzare un controller di dominio privato per il test.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-136">Other options for removing unwanted schema changes in a production environment are for developers to use a private domain controller for testing.</span></span> <span data-ttu-id="b9b7f-137">In questo caso, è possibile:</span><span class="sxs-lookup"><span data-stu-id="b9b7f-137">In this case, you can:</span></span>

-   <span data-ttu-id="b9b7f-138">"Reimpostare" il server Active Directory usando Dcpromo.exe per abbassare di più il controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-138">"Reset" the Active Directory server by using Dcpromo.exe to demote the DC.</span></span> <span data-ttu-id="b9b7f-139">Al termine dell'abbassamento di livello, utilizzare di nuovo Dcpromo.exe per innalzare di livello il server a un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-139">After the demote completes, use Dcpromo.exe again to promote the server back to a DC.</span></span> <span data-ttu-id="b9b7f-140">Lo sviluppatore può quindi utilizzare gli script LDIF per ricaricare le classi, gli attributi e le istanze degli oggetti richiesti.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-140">The developer can then use LDIF scripts to reload any required classes, attributes, and object instances.</span></span>
-   <span data-ttu-id="b9b7f-141">Utilizzare Ntbackup.exe per eseguire un backup dello stato del sistema in una partizione del disco disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-141">Use Ntbackup.exe to perform a system-state backup to an available disk partition.</span></span> <span data-ttu-id="b9b7f-142">Riavviare la modalità di ripristino del servizio Safe/directory per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-142">Reboot to Safe/Directory Service Restore mode to restore.</span></span>

<span data-ttu-id="b9b7f-143">Per i sistemi operativi Windows Server 2003, quando si imposta una classe o un attributo su inattivo, è possibile riutilizzare immediatamente i valori **ldapDisplayName**, **schemaIDGUID**, **OID** e **mapiID** dell'elemento dello schema inattivo quando si crea una nuova classe o attributo per sostituirlo.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-143">For Windows Server 2003 operating systems, when you set a class or attribute to defunct, you can immediately reuse the **ldapDisplayName**, **schemaIdGuid**, **OID** and **mapiID** values of the defunct schema element when you create a new class or attribute to replace it.</span></span> <span data-ttu-id="b9b7f-144">La versione inattiva della classe o dell'attributo viene mantenuta nel contenitore dello schema, ma è nascosta nello snap-in MMC.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-144">The defunct version of the class or attribute is maintained in the Schema container, but it is hidden in the MMC snap-in.</span></span> <span data-ttu-id="b9b7f-145">Per riattivare l'elemento dello schema precedente, impostare il valore di **Unfunct** su **false**.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-145">To reactivate the old schema element, set **isDefunct** to **FALSE**.</span></span>

<span data-ttu-id="b9b7f-146">Nell'esempio di codice LDIF riportato di seguito viene illustrato come modificare l'attributo **Indefunto** e modificare il RDN in modo che non venga confuso con la nuova classe creata per sostituirla.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-146">The following LDIF code example shows how to modify the **isDefunct** attribute and change the RDN so that it is not confused with the new class that you create to replace it.</span></span>

``` syntax
 dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modify
   replace: isDefunct
   isDefunct: TRUE
   -

   dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modrdn
   newrdn: cn=MyClassOld
   deleteoldrdn: 1

   dn:
   changetype: modify
   add: schemaUpdateNow
   schemaUpdateNow: 1
   -
```

<span data-ttu-id="b9b7f-147">Usare il comando seguente per eseguire l'esempio di codice LDIF su una foresta per un computer in esecuzione in sistemi operativi Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b9b7f-147">Use the following command to run the LDIF code example against a forest for a computer running on Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="b9b7f-148">**ldifde/i/f RDN. ldf/c "DC = X" "DC = Domain, DC = com"**</span><span class="sxs-lookup"><span data-stu-id="b9b7f-148">**ldifde /i /f rdn.ldf /c "DC=X" "dc=mydomain,dc=com"**</span></span>

<span data-ttu-id="b9b7f-149">(Dove "DC = X" è una costante)</span><span class="sxs-lookup"><span data-stu-id="b9b7f-149">(Where "DC=X" is a constant)</span></span>

 

 




