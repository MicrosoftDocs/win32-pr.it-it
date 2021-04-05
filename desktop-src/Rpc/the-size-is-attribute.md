---
title: Attributo size_is
description: L'attributo \ size \_ is \ è associato a una costante Integer, un'espressione o una variabile che specifica la dimensione di allocazione della matrice.
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872629"
---
# <a name="the-size_is-attribute"></a><span data-ttu-id="afce0-104">La \[ dimensione \_ è \] attribute</span><span class="sxs-lookup"><span data-stu-id="afce0-104">The \[size\_is\] Attribute</span></span>

<span data-ttu-id="afce0-105">L' \[ attributo [size \_ è](/windows/desktop/Midl/size-is) \] associato a una costante Integer, un'espressione o una variabile che specifica la dimensione di allocazione della matrice.</span><span class="sxs-lookup"><span data-stu-id="afce0-105">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute is associated with an integer constant, expression, or variable that specifies the allocation size of the array.</span></span> <span data-ttu-id="afce0-106">Si consideri una matrice di caratteri la cui lunghezza è determinata dall'input dell'utente:</span><span class="sxs-lookup"><span data-stu-id="afce0-106">Consider a character array whose length is determined by user input:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> <span data-ttu-id="afce0-107">L'asterisco ( \* ) che contrassegna il segnaposto per la dimensione della matrice di variabili è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="afce0-107">The asterisk (\*) that marks the placeholder for the variable-array dimension is optional.</span></span>

 

<span data-ttu-id="afce0-108">Lo stub del server deve allocare memoria nel server che corrisponde alla memoria del client per il parametro.</span><span class="sxs-lookup"><span data-stu-id="afce0-108">The server stub must allocate memory on the server that corresponds to the memory on the client for that parameter.</span></span> <span data-ttu-id="afce0-109">La variabile che specifica la dimensione deve essere sempre almeno un parametro \[ [in](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="afce0-109">The variable that specifies the size must always be at least an \[ [in](/windows/desktop/Midl/in)\] parameter.</span></span> <span data-ttu-id="afce0-110">L'attributo Directional è obbligatorio, **\[ in \]** modo che il valore Size venga definito alla voce dello stub del server.</span><span class="sxs-lookup"><span data-stu-id="afce0-110">The **\[in\]** directional attribute is required so that the size value is defined on entry to the server stub.</span></span> <span data-ttu-id="afce0-111">Questo valore di dimensione fornisce informazioni che lo stub del server richiede per allocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="afce0-111">This size value provides information that the server stub requires to allocate the memory.</span></span>

<span data-ttu-id="afce0-112">Il parametro size può essere anche \[ in [uscita](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="afce0-112">The size parameter can also be \[in, [out](/windows/desktop/Midl/out-idl)\].</span></span> <span data-ttu-id="afce0-113">Questa operazione è utile se, ad esempio, l'array inviato dal client non è sufficientemente grande per i dati che il server deve archiviare.</span><span class="sxs-lookup"><span data-stu-id="afce0-113">This is useful if, for instance, the array the client sends is not large enough for the data that the server needs to store in it.</span></span> <span data-ttu-id="afce0-114">È possibile utilizzare un parametro **\[ in, \] out** size per restituire le dimensioni richieste al programma client.</span><span class="sxs-lookup"><span data-stu-id="afce0-114">You can use an **\[in, out\]** size parameter to send the required size back to the client program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afce0-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afce0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afce0-116">Più livelli di puntatori</span><span class="sxs-lookup"><span data-stu-id="afce0-116">Multiple Levels of Pointers</span></span>](multiple-levels-of-pointers.md)
</dt> </dl>

 

 