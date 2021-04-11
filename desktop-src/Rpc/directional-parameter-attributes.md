---
title: Attributi direzionali (parametro)
description: Gli attributi direzionali descrivono se i dati vengono trasmessi da client a server, da server a client o da entrambi.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- RPC (Remote Procedure Call), descritti, attributi direzionali
- in ingresso
- in uscita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec37dbf65919f5aae9e7674cf7102eddcdf5170
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118099"
---
# <a name="directional-parameter-attributes"></a><span data-ttu-id="2b25a-106">Attributi direzionali (parametro)</span><span class="sxs-lookup"><span data-stu-id="2b25a-106">Directional (Parameter) Attributes</span></span>

<span data-ttu-id="2b25a-107">Gli attributi direzionali descrivono se i dati vengono trasmessi da client a server, da server a client o da entrambi.</span><span class="sxs-lookup"><span data-stu-id="2b25a-107">Directional attributes describe whether the data is transmitted from client to server, server to client, or both.</span></span> <span data-ttu-id="2b25a-108">Tutti i parametri nel prototipo di funzione devono essere associati a attributi direzionali.</span><span class="sxs-lookup"><span data-stu-id="2b25a-108">All parameters in the function prototype must be associated with directional attributes.</span></span> <span data-ttu-id="2b25a-109">Le tre possibili combinazioni di attributi direzionali sono: 1) \[ [**in**](/windows/desktop/Midl/in) \] , 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] e 3) \[ **in**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="2b25a-109">The three possible combinations of directional attributes are: 1) \[[**in**](/windows/desktop/Midl/in)\], 2) \[[**out**](/windows/desktop/Midl/out-idl)\], and 3) \[**in**, **out**\].</span></span> <span data-ttu-id="2b25a-110">Che descrivono il modo in cui i parametri vengono passati tra la chiamata e le routine chiamate.</span><span class="sxs-lookup"><span data-stu-id="2b25a-110">These describe the way parameters are passed between calling and called procedures.</span></span> <span data-ttu-id="2b25a-111">Quando si compila nell'impostazione predefinita (modalità estesa Microsoft) e si omette un attributo direzionale per un parametro, il compilatore MIDL presuppone che il valore predefinito sia \[ **in** \] .</span><span class="sxs-lookup"><span data-stu-id="2b25a-111">When you compile in the default (Microsoft-extended mode) and you omit a directional attribute for a parameter, the MIDL compiler assumes a default value of \[**in**\].</span></span>

<span data-ttu-id="2b25a-112">Un \[ parametro [**out**](/windows/desktop/Midl/out-idl) \] deve essere un puntatore.</span><span class="sxs-lookup"><span data-stu-id="2b25a-112">An \[[**out**](/windows/desktop/Midl/out-idl)\] parameter must be a pointer.</span></span> <span data-ttu-id="2b25a-113">Infatti, l'attributo \[ **out** \] non è significativo quando viene applicato a parametri che non fungono da puntatori perché i parametri della funzione C vengono passati per valore.</span><span class="sxs-lookup"><span data-stu-id="2b25a-113">In fact, the \[**out**\] attribute is not meaningful when applied to parameters that do not act as pointers because C function parameters are passed by value.</span></span> <span data-ttu-id="2b25a-114">In C, la funzione chiamata riceve una copia privata del valore del parametro. non può modificare il valore della funzione chiamante per il parametro.</span><span class="sxs-lookup"><span data-stu-id="2b25a-114">In C, the called function receives a private copy of the parameter value; it cannot change the calling function's value for that parameter.</span></span> <span data-ttu-id="2b25a-115">Tuttavia, se il parametro funge da puntatore, può essere utilizzato per accedere e modificare la memoria.</span><span class="sxs-lookup"><span data-stu-id="2b25a-115">If the parameter acts as a pointer, however, it can be used to access and modify memory.</span></span> <span data-ttu-id="2b25a-116">L' \[  \] attributo out indica che la funzione server deve restituire il valore alla funzione chiamante del client e che la memoria associata al puntatore deve essere restituita secondo gli attributi assegnati al puntatore.</span><span class="sxs-lookup"><span data-stu-id="2b25a-116">The \[**out**\] attribute indicates that the server function should return the value to the client's calling function, and that memory associated with the pointer should be returned in accordance with the attributes assigned to the pointer.</span></span>

<span data-ttu-id="2b25a-117">Nell'interfaccia seguente vengono illustrate le tre possibili combinazioni di attributi direzionali che è possibile applicare a un parametro.</span><span class="sxs-lookup"><span data-stu-id="2b25a-117">The following interface demonstrates the three possible combinations of directional attributes that can be applied to a parameter.</span></span> <span data-ttu-id="2b25a-118">La funzione **InOutProc** è definita nel file IDL come:</span><span class="sxs-lookup"><span data-stu-id="2b25a-118">The function **InOutProc** is defined in the IDL file as:</span></span>

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

<span data-ttu-id="2b25a-119">Il primo parametro, *S1*, è \[ solo [**in**](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="2b25a-119">The first parameter, *s1*, is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="2b25a-120">Il relativo valore viene trasmesso al computer remoto, ma non viene restituito alla procedura chiamante.</span><span class="sxs-lookup"><span data-stu-id="2b25a-120">Its value is transmitted to the remote computer, but is not returned to the calling procedure.</span></span> <span data-ttu-id="2b25a-121">Sebbene l'applicazione server possa modificare il proprio valore per *S1*, il valore di *S1* sul client è lo stesso prima e dopo la chiamata.</span><span class="sxs-lookup"><span data-stu-id="2b25a-121">Although the server application can change its value for *s1*, the value of *s1* on the client is the same before and after the call.</span></span>

<span data-ttu-id="2b25a-122">Il secondo parametro, *PS2*, viene definito nel prototipo di funzione come puntatore con \[ [](/windows/desktop/Midl/in) \] gli attributi in e \[ [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="2b25a-122">The second parameter, *ps2*, is defined in the function prototype as a pointer with both \[[**in**](/windows/desktop/Midl/in)\] and \[[**out**](/windows/desktop/Midl/out-idl)\] attributes.</span></span> <span data-ttu-id="2b25a-123">L' \[ attributo **in** \] indica che il valore del parametro viene passato dal client al server.</span><span class="sxs-lookup"><span data-stu-id="2b25a-123">The \[**in**\] attribute indicates that the value of the parameter is passed from the client to the server.</span></span> <span data-ttu-id="2b25a-124">L' \[  \] attributo out indica che al client viene restituito il valore a cui punta *PS2* .</span><span class="sxs-lookup"><span data-stu-id="2b25a-124">The \[**out**\] attribute indicates that the value pointed to by *ps2* is returned to the client.</span></span>

<span data-ttu-id="2b25a-125">Il terzo parametro è \[ [**out**](/windows/desktop/Midl/out-idl) \] only.</span><span class="sxs-lookup"><span data-stu-id="2b25a-125">The third parameter is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="2b25a-126">Lo spazio viene allocato per il parametro sul server, ma il valore non è definito alla voce.</span><span class="sxs-lookup"><span data-stu-id="2b25a-126">Space is allocated for the parameter on the server, but the value is undefined on entry.</span></span> <span data-ttu-id="2b25a-127">Come indicato in precedenza, tutti i \[ parametri **out** \] devono essere puntatori.</span><span class="sxs-lookup"><span data-stu-id="2b25a-127">As mentioned above, all \[**out**\] parameters must be pointers.</span></span>

<span data-ttu-id="2b25a-128">La procedura remota modifica il valore di tutti e tre i parametri, ma solo i nuovi valori dei \[ [](/windows/desktop/Midl/out-idl) \] parametri out e \[ [**in**](/windows/desktop/Midl/in) \] sono disponibili per il client.</span><span class="sxs-lookup"><span data-stu-id="2b25a-128">The remote procedure changes the value of all three parameters, but only the new values of the \[[**out**](/windows/desktop/Midl/out-idl)\] and \[[**in**](/windows/desktop/Midl/in)\] parameters are available to the client.</span></span>


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



<span data-ttu-id="2b25a-129">Al ritorno dalla chiamata a **InOutProc**, il secondo e il terzo parametro vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="2b25a-129">On return from the call to **InOutProc**, the second and third parameters are modified.</span></span> <span data-ttu-id="2b25a-130">Il primo parametro, che è \[ solo [**in**](/windows/desktop/Midl/in) \] , è invariato.</span><span class="sxs-lookup"><span data-stu-id="2b25a-130">The first parameter, which is \[[**in**](/windows/desktop/Midl/in)\] only, is unchanged.</span></span>

![parametri in](images/prog-a22.png)

![out (parametri)](images/prog-a23.png)

![parametri in uscita](images/prog-a21.png)

 

 