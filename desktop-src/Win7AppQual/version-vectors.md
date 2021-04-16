---
description: Un vettore di versione elabora i commenti condizionali in una pagina Web HTML. Ovvero i vettori di versione consentono di creare markup in base alla versione del browser.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Vettori di versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41fb0b24a205b280be163caeb63287fc5036b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350546"
---
# <a name="version-vectors"></a><span data-ttu-id="bd413-104">Vettori di versione</span><span class="sxs-lookup"><span data-stu-id="bd413-104">Version Vectors</span></span>

<span data-ttu-id="bd413-105">Un *vettore di versione* elabora i commenti condizionali in una pagina Web HTML.</span><span class="sxs-lookup"><span data-stu-id="bd413-105">A *version vector* processes conditional comments in an HTML webpage.</span></span> <span data-ttu-id="bd413-106">Ovvero i vettori di versione consentono di creare markup in base alla versione del browser.</span><span class="sxs-lookup"><span data-stu-id="bd413-106">That is, version vectors enable you to create markup based on the browser version.</span></span>

<span data-ttu-id="bd413-107">Osservare l'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="bd413-107">Consider the following code example.</span></span>


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



<span data-ttu-id="bd413-108">In questo caso, se la versione del browser Windows Internet Explorer è almeno 5,5, nella pagina Web viene visualizzato il paragrafo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bd413-108">In this case, if the Windows Internet Explorer browser version is at least 5.5, the corresponding paragraph is displayed in the webpage.</span></span> <span data-ttu-id="bd413-109">Sebbene la prima condizione in questo esempio illustri la funzione dei commenti condizionali, questi commenti non vengono in genere usati per visualizzare markup come la prima condizione.</span><span class="sxs-lookup"><span data-stu-id="bd413-109">Although the first condition in this example illustrates the function of conditional comments, these comments are not typically used to display markup like the first condition.</span></span> <span data-ttu-id="bd413-110">Al contrario, i restanti commenti condizionali nell'esempio precedente sono più frequenti.</span><span class="sxs-lookup"><span data-stu-id="bd413-110">Instead, the remaining conditional comments in the previous example are more common.</span></span> <span data-ttu-id="bd413-111">Nei commenti rimanenti, i commenti condizionali utilizzano un foglio di stile diverso per ogni versione del browser.</span><span class="sxs-lookup"><span data-stu-id="bd413-111">In these remaining comments, the conditional comments use a different style sheet for each different version of the browser.</span></span>

<span data-ttu-id="bd413-112">Nell'esempio di codice precedente viene inoltre verificata l'uguaglianza per Microsoft Internet Explorer 6 e Windows Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="bd413-112">The preceding code example also checks for equality for Microsoft Internet Explorer 6 and Windows Internet Explorer 7.</span></span> <span data-ttu-id="bd413-113">Per Windows Internet Explorer 8, tuttavia, nell'esempio viene utilizzato l'operatore GTE (maggiore o uguale a).</span><span class="sxs-lookup"><span data-stu-id="bd413-113">But for Windows Internet Explorer 8, the example uses the gte operator (greater than or equal).</span></span> <span data-ttu-id="bd413-114">Questo operatore consente di provare in futuro l'esempio in modo che venga usata la versione più conforme agli standard del foglio di stile quando viene rilasciata una nuova versione del browser, anziché usare il foglio di stile errato o un foglio di stile.</span><span class="sxs-lookup"><span data-stu-id="bd413-114">This operator helps future-proof the example so that the most standards-compliant version of the style sheet is used when a new version of the browser is released (instead of using the wrong style sheet or no style sheet).</span></span> <span data-ttu-id="bd413-115">Le applicazioni esistenti spesso non considerano una versione di Internet Explorer precedente 7 (o la versione più recente di Internet Explorer per cui è stato compilato il sito).</span><span class="sxs-lookup"><span data-stu-id="bd413-115">Existing applications often do not consider a version of Internet Explorer past 7 (or the newest version of Internet Explorer that the site is built for).</span></span> <span data-ttu-id="bd413-116">Per ulteriori informazioni sui vettori di versione, vedere la pagina relativa ai [vettori di versione](/previous-versions/cc817577(v=msdn.10)) in MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="bd413-116">For more information about version vectors, see [Version Vectors](/previous-versions/cc817577(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd413-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd413-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd413-118">Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità</span><span class="sxs-lookup"><span data-stu-id="bd413-118">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



