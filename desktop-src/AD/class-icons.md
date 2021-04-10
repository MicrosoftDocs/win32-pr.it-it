---
title: Icone della classe
description: L'icona utilizzata per rappresentare un oggetto classe può essere specificata nell'attributo iconPath nel contenitore DisplaySpecifiers.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- Nome visualizzazione classe AD, icone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691d4ef22babeded12ec9b951f92247df99521b6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956344"
---
# <a name="class-icons"></a><span data-ttu-id="f5a66-104">Icone della classe</span><span class="sxs-lookup"><span data-stu-id="f5a66-104">Class Icons</span></span>

<span data-ttu-id="f5a66-105">L'icona utilizzata per rappresentare un oggetto classe può essere specificata nell'attributo **iconPath** nel contenitore DisplaySpecifiers.</span><span class="sxs-lookup"><span data-stu-id="f5a66-105">The icon used to represent a class object can be specified in the **iconPath** attribute in the DisplaySpecifiers container.</span></span> <span data-ttu-id="f5a66-106">Ogni classe può inoltre archiviare più Stati dell'icona.</span><span class="sxs-lookup"><span data-stu-id="f5a66-106">Moreover, each class can store multiple icon states.</span></span> <span data-ttu-id="f5a66-107">Ad esempio, una classe di cartelle può avere icone per gli stati aperti, chiusi e disabilitati.</span><span class="sxs-lookup"><span data-stu-id="f5a66-107">For example, a folder class can have icons for the open, closed, and disabled states.</span></span> <span data-ttu-id="f5a66-108">L'implementazione corrente accetta un massimo di sedici diversi Stati di icona per classe.</span><span class="sxs-lookup"><span data-stu-id="f5a66-108">The current implementation accepts a maximum of sixteen different icon states per class.</span></span>

<span data-ttu-id="f5a66-109">L'attributo **iconPath** può essere specificato in uno dei due modi seguenti.</span><span class="sxs-lookup"><span data-stu-id="f5a66-109">The **iconPath** attribute can be specified in one of two ways.</span></span>


```C++
<state>,<icon file name>
```



<span data-ttu-id="f5a66-110">oppure</span><span class="sxs-lookup"><span data-stu-id="f5a66-110">or</span></span>


```C++
<state>,<module file name>,<resource ID>
```



<span data-ttu-id="f5a66-111">In questi esempi lo " &lt; stato &gt; " è un numero intero con un valore compreso tra 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="f5a66-111">In these examples, the "&lt;state&gt;" is an integer with a value between 0 and 15.</span></span> <span data-ttu-id="f5a66-112">Il valore 0 viene definito come lo stato predefinito o chiuso dell'icona.</span><span class="sxs-lookup"><span data-stu-id="f5a66-112">The value 0 is defined to be the default or closed state of the icon.</span></span> <span data-ttu-id="f5a66-113">Il valore 1 viene definito come lo stato aperto dell'icona.</span><span class="sxs-lookup"><span data-stu-id="f5a66-113">The value 1 is defined to be the open state of the icon.</span></span> <span data-ttu-id="f5a66-114">Il valore 2 è lo stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="f5a66-114">The value 2 is the disabled state.</span></span> <span data-ttu-id="f5a66-115">Tutti gli altri valori sono definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5a66-115">All other values are application-defined.</span></span>

<span data-ttu-id="f5a66-116">Il nome del file &lt; icona &gt; è il percorso e il nome del file di icona che contiene l'immagine dell'icona.</span><span class="sxs-lookup"><span data-stu-id="f5a66-116">The "&lt;icon file name&gt;" is the path and file name of an icon file that contains the icon image.</span></span>

<span data-ttu-id="f5a66-117">Il &lt; nome del file &gt; di modulo è il percorso e il nome file di un modulo, ad esempio un file exe o dll, che contiene l'immagine dell'icona in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5a66-117">The "&lt;module file name&gt;" is the path and file name of a module, such as an EXE or DLL, that contains the icon image in a resource.</span></span> <span data-ttu-id="f5a66-118">" &lt; ID risorsa &gt; " è un numero intero che specifica l'identificatore della risorsa icona all'interno del modulo.</span><span class="sxs-lookup"><span data-stu-id="f5a66-118">The "&lt;resource ID&gt;" is an integer that specifies the resource identifier of the icon resource within the module.</span></span>

## <a name="adding-a-value-to-the-iconpath-attribute"></a><span data-ttu-id="f5a66-119">Aggiunta di un valore all'attributo **iconPath**</span><span class="sxs-lookup"><span data-stu-id="f5a66-119">Adding a Value to the **iconPath** Attribute</span></span>

<span data-ttu-id="f5a66-120">Per aggiungere un valore all'attributo **iconPath** , seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="f5a66-120">To add a value to the **iconPath** attribute, perform the following steps.</span></span>

1.  <span data-ttu-id="f5a66-121">Determinare se il valore dell'attributo esiste.</span><span class="sxs-lookup"><span data-stu-id="f5a66-121">Determine if the value for the attribute exists.</span></span> <span data-ttu-id="f5a66-122">Se è necessario sostituire un valore, eliminare innanzitutto il valore esistente usando il metodo [**IADs::P UTEX**](/windows/desktop/api/iads/nf-iads-iads-putex) con il parametro *LnControlCode* impostato su **Ads \_ proprietà \_ Delete** e il parametro *vProp* impostato sul valore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f5a66-122">If a value is to be replaced, first, delete the existing value using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="f5a66-123">Non usare la **\_ Proprietà Ads \_ Clear** o **l' \_ \_ aggiornamento della proprietà ADS** per *lnControlCode*.</span><span class="sxs-lookup"><span data-stu-id="f5a66-123">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="f5a66-124">Creare la stringa che rappresenta i dati dell'icona dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="f5a66-124">Create the string that represents the attribute icon data.</span></span> <span data-ttu-id="f5a66-125">Per un esempio, vedere il formato riportato sopra.</span><span class="sxs-lookup"><span data-stu-id="f5a66-125">For an example, see the format above.</span></span>
3.  <span data-ttu-id="f5a66-126">Per aggiungere il nuovo valore, usare il metodo [**IADs::P UTEX**](/windows/desktop/api/iads/nf-iads-iads-putex) con il parametro *LnControlCode* impostato su **Ads \_ Property \_ Append**.</span><span class="sxs-lookup"><span data-stu-id="f5a66-126">To add the new value, use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND**.</span></span>
4.  <span data-ttu-id="f5a66-127">Per eseguire il commit delle modifiche nella directory, chiamare [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="f5a66-127">To commit changes to the directory, call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 