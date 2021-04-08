---
title: Gestione degli errori sconosciuti
description: Gestione degli errori sconosciuti
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c3d9e70b89a9a78be62d2940ad8a69ac34c8f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045277"
---
# <a name="handling-unknown-errors"></a><span data-ttu-id="5426c-103">Gestione degli errori sconosciuti</span><span class="sxs-lookup"><span data-stu-id="5426c-103">Handling Unknown Errors</span></span>

<span data-ttu-id="5426c-104">È lecito restituire un codice di stato solo dall'implementazione di un metodo di interfaccia approvato come legalmente restituibile.</span><span class="sxs-lookup"><span data-stu-id="5426c-104">It is legal to return a status code only from the implementation of an interface method sanctioned as legally returnable.</span></span> <span data-ttu-id="5426c-105">La mancata osservanza di questa regola consente di verificare la possibilità di conflitto tra i valori restituiti del codice di errore e quelli approvati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5426c-105">Failure to observe this rule invites the possibility of conflict between returned error-code values and those sanctioned by the application.</span></span> <span data-ttu-id="5426c-106">Prestare particolare attenzione a questo potenziale problema durante la propagazione dei codici di errore dalle funzioni chiamate internamente.</span><span class="sxs-lookup"><span data-stu-id="5426c-106">Pay particular attention to this potential problem when propagating error codes from functions that are called internally.</span></span>

<span data-ttu-id="5426c-107">Le applicazioni che chiamano interfacce devono considerare qualsiasi codice di errore restituito sconosciuto (in contrapposizione a un codice di esito positivo) come sinonimo di E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="5426c-107">Applications that call interfaces should treat any unknown returned error code (as opposed to a success code) as synonymous with E\_UNEXPECTED.</span></span> <span data-ttu-id="5426c-108">Questa pratica di gestione dei codici di errore sconosciuti è richiesta dai client delle funzioni e delle interfacce definite da COM.</span><span class="sxs-lookup"><span data-stu-id="5426c-108">This practice of handling unknown error codes is required by clients of the COM-defined interfaces and functions.</span></span> <span data-ttu-id="5426c-109">Poiché la procedura di programmazione tipica consiste nel gestire alcuni codici di errore specifici e trattare il resto in modo generico, è facile soddisfare questo requisito per la gestione di codici di errore imprevisti o sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="5426c-109">Because typical programming practice is to handle a few specific error codes in detail and treat the rest generically, this requirement of handling unexpected or unknown error codes is easily met.</span></span>

<span data-ttu-id="5426c-110">È importante gestire tutti i possibili errori quando si chiama un metodo di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="5426c-110">It is important to handle all possible errors when calling an interface method.</span></span> <span data-ttu-id="5426c-111">In caso contrario, potrebbe causare l'arresto anomalo dell'applicazione, il danneggiamento dei dati o il rischio di essere vulnerabile agli exploit di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="5426c-111">Failure to do so could cause your application to crash, to corrupt data, or to become vulnerable to security exploits.</span></span> <span data-ttu-id="5426c-112">Nell'esempio di codice seguente viene illustrata la modalità consigliata per la gestione degli errori sconosciuti:</span><span class="sxs-lookup"><span data-stu-id="5426c-112">The following code sample shows the recommended way of handling unknown errors:</span></span>


```C++
HRESULT hr; 
hr = xxMethod(); 
 
switch (GetScode(hr))  
{ 
    case NOERROR: 
      // Method returned success. 
      break; 
 
    case x1: 
      // Handle error x1 here.
      break; 
 
    case x2: 
      // Handle error x2 here.
      break; 
 
    case E_UNEXPECTED: 
    default: 
      // Handle unexpected errors here. 
      break; 
} 
 
```



<span data-ttu-id="5426c-113">Il controllo degli errori seguente viene spesso usato con le routine che non restituiscono alcun valore speciale (ad eccezione di S \_ OK o di un errore imprevisto):</span><span class="sxs-lookup"><span data-stu-id="5426c-113">The following error check is often used with those routines that do not return anything special (other than S\_OK or some unexpected error):</span></span>


```C++
if (xxMethod() == NOERROR) 
{
    // Handle success here.
} 
else 
{
    // Handle failure here.
} 
```



## <a name="related-topics"></a><span data-ttu-id="5426c-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5426c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5426c-115">Gestione degli errori in COM</span><span class="sxs-lookup"><span data-stu-id="5426c-115">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




