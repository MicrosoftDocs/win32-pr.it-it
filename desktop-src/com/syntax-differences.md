---
title: Differenze di sintassi
description: Il cambiamento più evidente quando ci si sposta tra i linguaggi di programmazione è la modifica della sintassi.
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3a9c2123d8b94f9fc6fe79d4ab48188830c7a1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474350"
---
# <a name="syntax-differences"></a><span data-ttu-id="2150f-103">Differenze di sintassi</span><span class="sxs-lookup"><span data-stu-id="2150f-103">Syntax Differences</span></span>

<span data-ttu-id="2150f-104">Il cambiamento più evidente quando ci si sposta tra i linguaggi di programmazione è la modifica della sintassi.</span><span class="sxs-lookup"><span data-stu-id="2150f-104">The most apparent change as you move between programming languages is the change in syntax.</span></span>

<span data-ttu-id="2150f-105">Si consideri il metodo Add dell'oggetto EnhEvents, illustrato come viene dichiarato in tre lingue diverse.</span><span class="sxs-lookup"><span data-stu-id="2150f-105">Consider the EnhEvents object's Add method, shown as it is declared in three different languages.</span></span>

``` syntax
object.Add(Time As Double, Name As String) As Variant

HRESULT Add(
  double Time, 
  BSTR Name, 
  VARIANT* pVal
);
 
public com.ms.com.Variant Add( 
  double Time, 
  java.lang.String Name
);
 
```

<span data-ttu-id="2150f-106">Sebbene la sintassi di ogni linguaggio esprima il metodo in modo diverso, la funzionalità è la stessa.</span><span class="sxs-lookup"><span data-stu-id="2150f-106">Although the syntax of each language expresses the method differently, the functionality is the same.</span></span> <span data-ttu-id="2150f-107">In ogni linguaggio, il metodo Add accetta i parametri *Time* e *Name* e restituisce un oggetto EnhEvent.</span><span class="sxs-lookup"><span data-stu-id="2150f-107">In each language, the Add method takes the parameters *Time* and *Name* and returns an EnhEvent object.</span></span> <span data-ttu-id="2150f-108">Nell'esempio di C++, il metodo restituisce l'oggetto usando un terzo parametro di output, *pval*.</span><span class="sxs-lookup"><span data-stu-id="2150f-108">In the C++ example, the method returns the object by using a third, output parameter, *pVal*.</span></span>

<span data-ttu-id="2150f-109">In genere, la funzionalità di un oggetto COM è la stessa in tutti i linguaggi di programmazione.</span><span class="sxs-lookup"><span data-stu-id="2150f-109">Typically, the functionality of a COM object is the same across programming languages.</span></span> <span data-ttu-id="2150f-110">Per questo motivo, la documentazione relativa a un oggetto COM è utile anche se l'oggetto è documentato in un altro linguaggio di programmazione rispetto a quello in uso.</span><span class="sxs-lookup"><span data-stu-id="2150f-110">Because of this, documentation for a COM object is useful even if the object is documented in another programming language than the one you are using.</span></span> <span data-ttu-id="2150f-111">Le descrizioni delle funzionalità, dei parametri e dei valori restituiti dell'oggetto sono, con poche eccezioni, valide per tutti i linguaggi.</span><span class="sxs-lookup"><span data-stu-id="2150f-111">The descriptions of the object's functionality, parameters, and return values are, with few exceptions, valid for all languages.</span></span>

<span data-ttu-id="2150f-112">Per informazioni su come convertire la sintassi di un oggetto COM in un altro linguaggio di programmazione, vedere [traduzione della sintassi degli oggetti com per i linguaggi di programmazione](translating-com-object-syntax-for-programming-languages.md).</span><span class="sxs-lookup"><span data-stu-id="2150f-112">For information about how to convert the syntax of a COM object to another programming language, see [Translating COM Object Syntax for Programming Languages](translating-com-object-syntax-for-programming-languages.md).</span></span>

<span data-ttu-id="2150f-113">Le differenze di sintassi tra i linguaggi di scripting JavaScript, JScript e VBScript sono meno evidenti rispetto alle differenze di sintassi tra i linguaggi di programmazione illustrati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="2150f-113">The syntax differences among the scripting languages JavaScript, JScript, and VBScript are less pronounced than the syntax differences among the programming languages shown preceding.</span></span> <span data-ttu-id="2150f-114">Si consideri, ad esempio, la funzione quadrata implementata in ognuno di questi tre linguaggi di scripting:</span><span class="sxs-lookup"><span data-stu-id="2150f-114">For example, consider the square function as it is implemented in each of these three scripting languages:</span></span>

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

<span data-ttu-id="2150f-115">Si noti che i linguaggi di scripting, a differenza dei linguaggi di programmazione, sono debolmente tipizzati.</span><span class="sxs-lookup"><span data-stu-id="2150f-115">Notice that the scripting languages, unlike the programming languages, are weakly typed.</span></span> <span data-ttu-id="2150f-116">In altre parole, non è necessario specificare il tipo di dati di un parametro o di un valore restituito quando si dichiara una funzione.</span><span class="sxs-lookup"><span data-stu-id="2150f-116">In other words, you do not have to specify the data type of a parameter or return value when you declare a function.</span></span> <span data-ttu-id="2150f-117">Al contrario, viene eseguito automaticamente il cast delle variabili al tipo di dati appropriato.</span><span class="sxs-lookup"><span data-stu-id="2150f-117">Instead, the variables are automatically cast to the appropriate data type.</span></span> <span data-ttu-id="2150f-118">Nel caso di VBScript, tutte le variabili hanno lo stesso tipo di dati, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="2150f-118">In the case of VBScript, all variables are of the same data type, **Variant**.</span></span>

<span data-ttu-id="2150f-119">La sintassi JavaScript e JScript per Square è la stessa.</span><span class="sxs-lookup"><span data-stu-id="2150f-119">The JavaScript and JScript syntax for square is the same.</span></span> <span data-ttu-id="2150f-120">JScript è ampiamente compatibile con JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2150f-120">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="2150f-121">Tuttavia, JScript include alcuni oggetti attualmente non supportati da JavaScript, ad esempio **ActiveXObject**, **Enumerator**, **Error**, **Global** e **VBArray**.</span><span class="sxs-lookup"><span data-stu-id="2150f-121">However, JScript includes some objects not currently supported by JavaScript, such as **ActiveXObject**, **Enumerator**, **Error**, **Global**, and **VBArray**.</span></span> <span data-ttu-id="2150f-122">Per ulteriori informazioni su questi oggetti, vedere la Guida di [riferimento al linguaggio JScript](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="2150f-122">For more information about these objects, see the [JScript Language Reference](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span></span>

<span data-ttu-id="2150f-123">Sulla superficie, la sintassi di JavaScript e JScript è simile alla sintassi Java.</span><span class="sxs-lookup"><span data-stu-id="2150f-123">On the surface, JavaScript and JScript syntax resembles Java syntax.</span></span> <span data-ttu-id="2150f-124">Questa somiglianza è solo superficiale.</span><span class="sxs-lookup"><span data-stu-id="2150f-124">This similarity is only superficial.</span></span> <span data-ttu-id="2150f-125">Il linguaggio Java è stato sviluppato indipendentemente da JavaScript e JScript e non è correlato a entrambi.</span><span class="sxs-lookup"><span data-stu-id="2150f-125">The Java language was developed independently from both JavaScript and JScript and is not related to either.</span></span>

<span data-ttu-id="2150f-126">VBScript, d'altra parte, è un subset del linguaggio di programmazione Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2150f-126">VBScript, on the other hand, is a subset of the Visual Basic programming language.</span></span> <span data-ttu-id="2150f-127">Per questo motivo, la sintassi VBScript è un subset della sintassi Visual Basic e spesso è interscambiabile con Visual Basic sintassi.</span><span class="sxs-lookup"><span data-stu-id="2150f-127">Because of this, VBScript syntax is a subset of Visual Basic syntax and is often interchangeable with Visual Basic syntax.</span></span>

<span data-ttu-id="2150f-128">Per informazioni sull'utilizzo di oggetti COM in linguaggi di scripting, vedere Creazione di [script con oggetti com](scripting-with-com-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2150f-128">For information on using COM objects in scripting languages, see [Scripting with COM Objects](scripting-with-com-objects.md).</span></span>

 

 