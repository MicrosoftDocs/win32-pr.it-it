---
title: Modifica di interfacce utente esistenti
description: Il riquadro dei risultati dello snap-in MMC utenti e computer Active Directory Visualizza varie colonne di dati di attributo per gli oggetti all'interno di un contenitore, ad esempio gli attributi nome e descrizione.
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Modifica delle interfacce utente esistenti AD
- Snap-in utenti e computer di Active Directory, modifica della visualizzazione
- Snap-in utenti e computer AD, aggiunta di colonne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0765988a9ceed3e98966091ad94b868b96fd88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855406"
---
# <a name="modifying-existing-user-interfaces"></a><span data-ttu-id="a6ed6-106">Modifica di interfacce utente esistenti</span><span class="sxs-lookup"><span data-stu-id="a6ed6-106">Modifying Existing User Interfaces</span></span>

<span data-ttu-id="a6ed6-107">Il riquadro dei risultati dello snap-in MMC utenti e computer Active Directory Visualizza varie colonne di dati di attributo per gli oggetti all'interno di un contenitore, ad esempio gli attributi **nome** e **Descrizione** .</span><span class="sxs-lookup"><span data-stu-id="a6ed6-107">The results pane of the Active Directory Users and Computers MMC snap-in displays several columns of attribute data for objects within a container, such as the **Name** and **Description** attributes.</span></span> <span data-ttu-id="a6ed6-108">Lo snap-in consente all'utente di aggiungere e rimuovere le colonne visualizzate nel riquadro dei risultati dello snap-in.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-108">The snap-in enables the user to add and remove the columns displayed in the results pane of the snap-in.</span></span>

<span data-ttu-id="a6ed6-109">Per modificare la visualizzazione, l'utente utilizza il menu a discesa **Visualizza** e seleziona **Aggiungi/Rimuovi colonne**.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-109">To change the display, the user uses the **View** pull-down menu and selects **Add/Remove Columns**.</span></span> <span data-ttu-id="a6ed6-110">Nella finestra di dialogo **Aggiungi/Rimuovi colonne** è disponibile un elenco di colonne che l'utente può scegliere di visualizzare nel riquadro risultati.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-110">In the **Add/Remove Columns** dialog box, there is a list of columns that the user can choose from to display in the results pane.</span></span>

<span data-ttu-id="a6ed6-111">Lo snap-in MMC utenti e computer Active Directory incluso in Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition e Windows Server 2003, Datacenter Edition, consente di modificare l'elenco delle colonne che possono essere visualizzate nel riquadro dei risultati dello snap-in per un contenitore.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-111">The Active Directory Users and Computers MMC snap-in that is included with Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition, and Windows Server 2003, Datacenter Edition, provides the ability to modify the list of columns that can be displayed in the results pane of the snap-in for a container.</span></span> <span data-ttu-id="a6ed6-112">Questa funzionalità è disponibile solo se lo snap-in è destinato a una foresta con schema di Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-112">This feature only exists if the snap-in is targeted at a forest with Windows Server 2003 schema.</span></span>

<span data-ttu-id="a6ed6-113">Per aggiungere una colonna all'elenco, aggiungere un valore all'attributo **outcolumns** dell'identificatore di visualizzazione per il tipo di oggetto a cui è associato l'attributo.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-113">To add a column to the list, add a value to the **extraColumns** attribute of the display specifier for the object type that the attribute is associated with.</span></span> <span data-ttu-id="a6ed6-114">L'attributo **outcolumns** è un attributo di stringa multivalore in cui ogni stringa è nel formato seguente.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-114">The **extraColumns** attribute is a multi-valued string attribute where each string is in the following format.</span></span>


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



<span data-ttu-id="a6ed6-115">La tabella seguente elenca il contenuto di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-115">The following table lists the contents of these values.</span></span>



| <span data-ttu-id="a6ed6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a6ed6-116">Value</span></span>                        | <span data-ttu-id="a6ed6-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6ed6-117">Description</span></span>                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ed6-118">" &lt; ldapDisplayName &gt; "</span><span class="sxs-lookup"><span data-stu-id="a6ed6-118">"&lt;ldapdisplayname&gt;"</span></span>    | <span data-ttu-id="a6ed6-119">Contiene una stringa che rappresenta **ldapDisplayName** dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-119">Contains a string that represents the **ldapDisplayName** of the attribute.</span></span>                                                         |
| <span data-ttu-id="a6ed6-120">" &lt; intestazione di colonna &gt; "</span><span class="sxs-lookup"><span data-stu-id="a6ed6-120">"&lt;column header&gt;"</span></span>      | <span data-ttu-id="a6ed6-121">Contiene una stringa che rappresenta il testo visualizzato nell'intestazione della colonna.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-121">Contains a string that represents the text displayed in the header for the column.</span></span>                                                  |
| <span data-ttu-id="a6ed6-122">" &lt; visibilità predefinita &gt; "</span><span class="sxs-lookup"><span data-stu-id="a6ed6-122">"&lt;default visibility&gt;"</span></span> | <span data-ttu-id="a6ed6-123">Contiene un valore numerico che è 0 se l'attributo è nascosto per impostazione predefinita o 1 se l'attributo è visibile per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-123">Contains a numeric value that is 0 if the attribute is hidden by default or 1 if the attribute is visible by default.</span></span>               |
| <span data-ttu-id="a6ed6-124">" &lt; larghezza &gt; "</span><span class="sxs-lookup"><span data-stu-id="a6ed6-124">"&lt;width&gt;"</span></span>              | <span data-ttu-id="a6ed6-125">Contiene la larghezza, in pixel, della colonna.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-125">Contains the width of the column, in pixels.</span></span> <span data-ttu-id="a6ed6-126">Se questo valore è-1, la larghezza della colonna viene impostata sulla larghezza dell'intestazione di colonna.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-126">If this value is -1, the width of the column is set to the width of the column header.</span></span> |
| <span data-ttu-id="a6ed6-127">"non &lt; usato &gt; "</span><span class="sxs-lookup"><span data-stu-id="a6ed6-127">"&lt;unused&gt;"</span></span>             | <span data-ttu-id="a6ed6-128">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-128">Unused.</span></span> <span data-ttu-id="a6ed6-129">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-129">Must be zero.</span></span>                                                                                                               |



 

<span data-ttu-id="a6ed6-130">Ad esempio, per aggiungere una colonna in cui verrà visualizzato il nome canonico per gli oggetti in un'unità organizzativa, viene aggiunto un valore per l'attributo **CanonicalName** all'attributo **outcolumns** dell'oggetto **organizationalUnit-Display** nel contenitore Display Specifiers.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-130">For example, to add a column that will display the canonical name for objects in an organizational unit, a value for the **canonicalName** attribute is added to the **extraColumns** attribute of the **organizationalUnit-Display** object in the display specifiers container.</span></span> <span data-ttu-id="a6ed6-131">La stringa aggiunta all'attributo **outcolumns** dell'oggetto **organizationalUnit-Display** sarà simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-131">The string added to the **extraColumns** attribute of the **organizationalUnit-Display** object will look like the following.</span></span>


```C++
canonicalName,Canonical Name,0,150,0
```



<span data-ttu-id="a6ed6-132">Nella finestra di dialogo **Aggiungi/Rimuovi colonne** vengono visualizzate solo le colonne contenute nell'attributo **outcolumns** dell'oggetto **displaySpecifier** del tipo di contenitore visualizzato.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-132">The **Add/Remove Columns** dialog box displays only the columns that are contained in the **extraColumns** attribute of the **displaySpecifier** object of the container type that is being displayed.</span></span> <span data-ttu-id="a6ed6-133">Se l' **attributo delle colonne non** contiene valori, nella finestra di dialogo **Aggiungi/Rimuovi colonne** viene visualizzato un set fisso di colonne.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-133">If the **extraColumns** attribute does not contain any values, the **Add/Remove Columns** dialog box will display a fixed set of columns.</span></span> <span data-ttu-id="a6ed6-134">Una copia del set di colonne fisso è contenuta nell'attributo **outcolumns** dell'oggetto di **visualizzazione predefinito** .</span><span class="sxs-lookup"><span data-stu-id="a6ed6-134">A copy of the fixed set of columns is contained in the **extraColumns** attribute of the **default-Display** object.</span></span>

<span data-ttu-id="a6ed6-135">Per aggiungere una o più colonne all'elenco di colonne per un oggetto specifico, è necessario copiare tutti **i valori delle colonne a** partire dall'oggetto **predefinito-display** nell'oggetto di destinazione e quindi aggiungere le colonne personalizzate.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-135">To add one or more columns to the list of columns for a specific object, you must copy all of the **extraColumns** values from the **default-Display** object to the target object and then add the custom columns.</span></span> <span data-ttu-id="a6ed6-136">Se si specifica l'attributo **outcolumns** su una determinata classe, tale classe utilizzerà tali colonne e non le unirà alle colonne specificate nella classe **default-Display** .</span><span class="sxs-lookup"><span data-stu-id="a6ed6-136">If you specify the **extraColumns** attribute on a given class, then that class will use those columns and will not merge them with the columns that are specified in the **default-Display** class.</span></span> <span data-ttu-id="a6ed6-137">Pertanto, ulteriori modifiche apportate alla classe **default-Display** non avranno alcun effetto su tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="a6ed6-137">Therefore, further changes to the **default-Display** class will have no effect on that object.</span></span>

<span data-ttu-id="a6ed6-138">Per visualizzare una colonna personalizzata per tutti i tipi di contenitore per i quali non sono state registrate colonne personalizzate, aggiungere un valore per la colonna all'attributo **outcolumns** dell'oggetto **visualizzato per impostazione predefinita** .</span><span class="sxs-lookup"><span data-stu-id="a6ed6-138">To display a custom column for all container types that do not have any custom columns registered, add a value for the column to the **extraColumns** attribute of the **default-Display** object.</span></span>

 

 




