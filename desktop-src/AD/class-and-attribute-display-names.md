---
title: Nomi visualizzati della classe e dell'attributo
description: Questo argomento contiene informazioni sulle linee guida e per i nomi visualizzati delle classi e degli attributi.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- Visualizza gli identificatori di Active Directory, della classe e dell'attributo
- Nome visualizzazione classe AD
- nome visualizzato attributo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d65cd6ac6fc3077ff0d2bba15ffa9904b147654
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472670"
---
# <a name="class-and-attribute-display-names"></a><span data-ttu-id="3c062-106">Nomi visualizzati della classe e dell'attributo</span><span class="sxs-lookup"><span data-stu-id="3c062-106">Class and Attribute Display Names</span></span>

<span data-ttu-id="3c062-107">L'identificatore di visualizzazione per una classe di oggetti contiene gli attributi seguenti che possono essere usati per specificare i nomi visualizzati localizzati usati nell'interfaccia utente per gli oggetti di tale classe:</span><span class="sxs-lookup"><span data-stu-id="3c062-107">The display specifier for an object class contains the following attributes that can be used to specify the localized display names used in the UI for objects of that class:</span></span>

-   <span data-ttu-id="3c062-108">L'attributo **classDisplayName** è una stringa Unicode a valore singolo che specifica il nome visualizzato della classe.</span><span class="sxs-lookup"><span data-stu-id="3c062-108">The **classDisplayName** attribute is a single-value Unicode string that specifies the class display name.</span></span>
-   <span data-ttu-id="3c062-109">L'attributo **nell'attributeDisplayNames** è una proprietà multivalore che specifica i nomi da utilizzare nell'interfaccia utente per gli attributi della classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="3c062-109">The **attributeDisplayNames** attribute is a multi-value property that specifies the names to use in the UI for attributes of the object class.</span></span>

<span data-ttu-id="3c062-110">I valori **nell'attributeDisplayNames** sono stringhe Unicode; ogni elemento è costituito da una coppia di nomi delimitati da virgole:</span><span class="sxs-lookup"><span data-stu-id="3c062-110">The **attributeDisplayNames** values are Unicode strings; each element consists of a comma-delimited name pair:</span></span>


```C++
<attribute name>,<display text>
```



<span data-ttu-id="3c062-111">In questo esempio " &lt; nome attributo &gt; " è l' **ldapDisplayName** dell'attributo e " &lt; testo visualizzato &gt; " è il testo da visualizzare come nome dell'attributo nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="3c062-111">In this example, "&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute and "&lt;display text&gt;" is the text to display as the name of that attribute in the user interface.</span></span>

## <a name="guidelines-for-class-and-attribute-display-names"></a><span data-ttu-id="3c062-112">Linee guida per i nomi visualizzati delle classi e degli attributi</span><span class="sxs-lookup"><span data-stu-id="3c062-112">Guidelines for Class and Attribute Display Names</span></span>

<span data-ttu-id="3c062-113">Poiché molti fornitori possono estendere le classi con nuovi attributi o creare classi completamente nuove, è importante che i nomi visualizzati della classe e dell'attributo non siano ambigui e non comportino conflitti.</span><span class="sxs-lookup"><span data-stu-id="3c062-113">Because many vendors may extend classes with new attributes or creating entirely new classes, it is important that the class and attribute display names are unambiguous and do not result in conflicts.</span></span>

<span data-ttu-id="3c062-114">Ogni fornitore deve anteporre al nome visualizzato della classe un identificatore descrittivo univoco in base al nome del fornitore.</span><span class="sxs-lookup"><span data-stu-id="3c062-114">Each vendor should prefix the class display name with a unique friendly identifier based on the vendor name.</span></span> <span data-ttu-id="3c062-115">Se, ad esempio, la società fittizia Fabrikam Inc. crea una nuova classe derivata dalla classe "Contact", può avere un nome visualizzato di classe univoco "contatto Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="3c062-115">For example, if the fictitious company, Fabrikam Inc., creates a new class derived from the "contact" class, they can have a unique class display name "Fabrikam Contact."</span></span>

<span data-ttu-id="3c062-116">Se un fornitore estende una classe esistente con nuovi attributi, deve identificare in modo univoco il nome visualizzato dell'attributo in modo che non si verifichino conflitti con altri nomi visualizzati dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="3c062-116">If a vendor extends an existing class with new attributes, they should again uniquely identify the attribute display name so that no conflicts occur with other attribute display names.</span></span> <span data-ttu-id="3c062-117">Anche in questo caso, il prefisso del nome visualizzato dell'attributo con identificatore descrittivo univoco in base al nome del fornitore è una procedura consigliata.</span><span class="sxs-lookup"><span data-stu-id="3c062-117">Again, prefixing the attribute display name with unique friendly identifier based on the vendor name is good practice.</span></span> <span data-ttu-id="3c062-118">Se, ad esempio, l'azienda Fabrikam estende la classe utente con un nuovo attributo HR, può visualizzare in modo univoco l'attributo "informazioni su Fabrikam HR".</span><span class="sxs-lookup"><span data-stu-id="3c062-118">For example, if the Fabrikam company extends the user class with a new HR attribute, they could uniquely display the attribute as "Fabrikam HR Information."</span></span>

<span data-ttu-id="3c062-119">Inoltre, dal punto di vista della localizzazione, ogni fornitore deve localizzare i nomi visualizzati della classe e dell'attributo in ogni lingua supportata da Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3c062-119">In addition, from a localization perspective, each vendor should localize the class and attribute display names into each language supported by Windows 2000.</span></span>

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a><span data-ttu-id="3c062-120">Aggiunta di un valore all'attributo nell'attributeDisplayNames</span><span class="sxs-lookup"><span data-stu-id="3c062-120">Adding a Value to the attributeDisplayNames Attribute</span></span>

<span data-ttu-id="3c062-121">\*\*Per aggiungere un valore di mapping dei nomi all'attributo \*\*nell'attributeDisplayNames\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3c062-121">**To add a name mapping value to the **attributeDisplayNames** attribute**</span></span>

1.  <span data-ttu-id="3c062-122">Determinare se esiste il valore del mapping dei nomi per l'attributo.</span><span class="sxs-lookup"><span data-stu-id="3c062-122">Determine if the name mapping value for the attribute exists.</span></span> <span data-ttu-id="3c062-123">Se è necessario sostituire un valore di mapping dei nomi, eliminare innanzitutto il valore esistente, usando il metodo [**IADs::P UTEX**](/windows/desktop/api/iads/nf-iads-iads-putex) , con il parametro *LnControlCode* impostato su **Ads \_ proprietà \_ Delete** e il parametro *vProp* impostato sul valore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3c062-123">If a name mapping value is to be replaced, first deleted the existing value, using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method, with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="3c062-124">Non usare la **\_ Proprietà Ads \_ Clear** o **l' \_ \_ aggiornamento della proprietà ADS** per *lnControlCode*.</span><span class="sxs-lookup"><span data-stu-id="3c062-124">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="3c062-125">Creare la stringa che rappresenta il nome visualizzato dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="3c062-125">Create the string that represents the attribute display name.</span></span> <span data-ttu-id="3c062-126">Per un esempio, vedere il formato riportato sopra.</span><span class="sxs-lookup"><span data-stu-id="3c062-126">For an example, see the format above.</span></span>
3.  <span data-ttu-id="3c062-127">Usare il metodo [**IADs::P UTEX**](/windows/desktop/api/iads/nf-iads-iads-putex) con il parametro *LnControlCode* impostato su **Ads \_ Property \_ Append** per aggiungere il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="3c062-127">Use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND** to add the new value.</span></span>
4.  <span data-ttu-id="3c062-128">Chiamare [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per eseguire il commit delle modifiche nella directory.</span><span class="sxs-lookup"><span data-stu-id="3c062-128">Call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>

<span data-ttu-id="3c062-129">Per ulteriori informazioni sulla denominazione di nuove classi e attributi, vedere [Naming Attributes and classes](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="3c062-129">For more information about naming new classes and attributes, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span>

 

 