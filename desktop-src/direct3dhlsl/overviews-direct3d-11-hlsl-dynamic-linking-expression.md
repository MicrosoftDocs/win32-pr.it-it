---
title: Limitazioni di utilizzo dell'interfaccia
description: L'hardware GPU corrente non supporta la variazione delle informazioni sugli slot al runtime dello shader. Di conseguenza, i riferimenti all'interfaccia non possono essere modificati all'interno di un'espressione condizionale, ad esempio un'istruzione if o switch.
ms.assetid: 95a505d8-3ec4-49b7-bb2b-f29a655e4225
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8825d192dcb874ce8b148c4ade5c579a55857311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329364"
---
# <a name="interface-usage-restrictions"></a><span data-ttu-id="431e4-104">Limitazioni di utilizzo dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="431e4-104">Interface Usage Restrictions</span></span>

<span data-ttu-id="431e4-105">L'hardware GPU corrente non supporta la variazione delle informazioni sugli slot al runtime dello shader.</span><span class="sxs-lookup"><span data-stu-id="431e4-105">Current GPU hardware does not support varying slot information at shader runtime.</span></span> <span data-ttu-id="431e4-106">Di conseguenza, i riferimenti all'interfaccia non possono essere modificati all'interno di un'espressione condizionale, ad esempio un'istruzione if o switch.</span><span class="sxs-lookup"><span data-stu-id="431e4-106">As a consequence interface references cannot be modified within a conditional expression such as an if or switch statement.</span></span>

<span data-ttu-id="431e4-107">Il codice dello shader seguente illustra quando si verifica questa restrizione e un possibile approccio alternativo.</span><span class="sxs-lookup"><span data-stu-id="431e4-107">The following shader code illustrates when this restriction will occur and a possible alternate approach.</span></span>

<span data-ttu-id="431e4-108">Date le seguenti dichiarazioni di interfaccia:</span><span class="sxs-lookup"><span data-stu-id="431e4-108">Given the following interface declarations:</span></span>


```
interface A
{
    float GetRatio();
    bool IsGood();
};

interface B
{
    float GetValue();
};

A arrayA[6];
B arrayB[6];
```



<span data-ttu-id="431e4-109">Date le seguenti dichiarazioni di classe:</span><span class="sxs-lookup"><span data-stu-id="431e4-109">Given the following class declarations:</span></span>


```
class C1 : A
{
    float var;
    float GetRatio() { return 1.0f; }
    bool IsGood() { return true; }
};

class C2 : C1, B
{
    float GetRatio() { return C1::GetRatio() * 0.33f; }
    float GetValue() { return 5.0f; }
    bool IsGood() { return false; }
};

class C3 : B
{
    float var;
    float GetValue() { return -1.0f; }
};

class C4 : A, B
{
    float var;
    float GetRatio() { return var; }
    float GetValue() { return var * 2.0f; }
    bool IsGood() { return var > 0.0f; }
};
```



<span data-ttu-id="431e4-110">Un riferimento all'interfaccia non può essere modificato all'interno dell'espressione condizionale (istruzione if):</span><span class="sxs-lookup"><span data-stu-id="431e4-110">An interface reference cannot be modified within the conditional expression (an if statement):</span></span>


```
float main() : wicked
{
    float rev;
    {
        A a = arrayA[0];
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                // This forces the loop to be unrolled, 
                // since the slot information is changing.
                a = arrayA[i]; 
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                // This causes an error since the compiler is
                // unable to determine the interface slot
                rev += arrayB[i].GetValue() + a.GetRatio(); 
            }
        }
    }
    return rev;
}
```



<span data-ttu-id="431e4-111">Date le stesse dichiarazioni di interfaccia e di classe, è possibile usare un indice per fornire la stessa funzionalità ed evitare l'unrolling del ciclo forzato.</span><span class="sxs-lookup"><span data-stu-id="431e4-111">Given the same interface and class declarations, you could use an index to provide the same functionality and avoid the forced loop unroll.</span></span>


```
float main() : wicked
{
    float rev;
    {
        uint index = 0;
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                index = i;
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                rev += arrayB[i].GetValue() + arrayA[index].GetRatio();
            }
        }
    }
    return rev;
}
```



## <a name="related-topics"></a><span data-ttu-id="431e4-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="431e4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="431e4-113">Collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="431e4-113">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 




