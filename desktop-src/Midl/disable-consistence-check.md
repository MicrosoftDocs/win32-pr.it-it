---
title: Attributo disable_consistency_check
description: Indica a RPC di non applicare la verifica della coerenza di correlazione.
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc55197b5eb680533745a09d4fca4f5827574a7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329047"
---
# <a name="disable_consistency_check-attribute"></a><span data-ttu-id="27f1b-103">disabilitare \_ l' \_ attributo di verifica coerenza</span><span class="sxs-lookup"><span data-stu-id="27f1b-103">disable\_consistency\_check Attribute</span></span>

<span data-ttu-id="27f1b-104">Indica a RPC di non applicare la verifica della coerenza di correlazione.</span><span class="sxs-lookup"><span data-stu-id="27f1b-104">Directs RPC to not enforce correlation consistency checking.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

<span data-ttu-id="27f1b-105">Per i parametri correlati, RPC imporrà che viene passato un buffer non null quando la variabile di conteggio delle correlazioni è non null.</span><span class="sxs-lookup"><span data-stu-id="27f1b-105">For correlated parameters, RPC will enforce that a non-null buffer is passed when the correlation count variable is non-null.</span></span>

## <a name="example"></a><span data-ttu-id="27f1b-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="27f1b-106">Example</span></span>

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

<span data-ttu-id="27f1b-107">Se la *stringa* è **null**, RPC rifiuterà la chiamata a meno che length non sia impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="27f1b-107">If *MyString* is **NULL**, RPC will reject the call unless Length is set to 0.</span></span> <span data-ttu-id="27f1b-108">Si noti che RPC consentirà la *lunghezza* pari a 0 mentre la *stringa* è non null e RPC tratterà la *stringa* come un'allocazione di buffer di lunghezza 0.</span><span class="sxs-lookup"><span data-stu-id="27f1b-108">Note that RPC will allow *Length* to be 0 while *MyString* is non-NULL, and RPC will treat *MyString* as a 0-length buffer allocation.</span></span>

## <a name="remarks"></a><span data-ttu-id="27f1b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="27f1b-109">Remarks</span></span>

<span data-ttu-id="27f1b-110">Per disabilitare questo controllo, l'IDL può contenere l' \[ \_ attributo disable \_ Verifica coerenza \] su un parametro, un typedef o un tipo di puntatore.</span><span class="sxs-lookup"><span data-stu-id="27f1b-110">To disable this checking, the IDL can contain the \[disable\_consistency\_check\] attribute on a parameter, typedef, or pointer type.</span></span> <span data-ttu-id="27f1b-111">In questo modo, RPC non impone la coerenza tra il puntatore del buffer e la variabile di correlazione per il buffer a cui punta il parametro o il puntatore.</span><span class="sxs-lookup"><span data-stu-id="27f1b-111">This will direct RPC to not enforce the consistency between the buffer pointer and the correlation variable for the buffer pointed to by the parameter or pointer.</span></span>

<span data-ttu-id="27f1b-112">Per disabilitare la verifica della coerenza per un'intera compilazione MIDL (e disabilitare l'imposizione del controllo in tutti i casi), è possibile usare l'opzione della riga di comando MIDL [/Backward \_ compat MAYBENULL \_ sizeis](-backward-compat.md) .</span><span class="sxs-lookup"><span data-stu-id="27f1b-112">To disable consistency checking for an entire MIDL compilation (and disable enforcement of the checking in all cases), the MIDL command line switch [/backward\_compat maybenull\_sizeis](-backward-compat.md) can be used.</span></span> <span data-ttu-id="27f1b-113">A tale scopo, è necessario che la destinazione della compilazione MIDL sia almeno â € "NT60 di destinazione.</span><span class="sxs-lookup"><span data-stu-id="27f1b-113">This requires that the target of the MIDL compilation be at least â€“target NT60.</span></span>

 

 




