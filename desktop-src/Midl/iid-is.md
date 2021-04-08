---
title: iid_is (attributo)
description: L'attributo \ IID \_ is \ Pointer indica l'IID dell'interfaccia com a cui punta un puntatore a interfaccia.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- attributo iid_is MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94c6f46a6828e81817e45ff6eb6eb8245b00a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045572"
---
# <a name="iid_is-attribute"></a><span data-ttu-id="12ac0-104">IID \_ è un attributo</span><span class="sxs-lookup"><span data-stu-id="12ac0-104">iid\_is attribute</span></span>

<span data-ttu-id="12ac0-105">L' **\[ IID \_ è \]** un attributo puntatore che specifica l'IID dell'interfaccia com a cui punta un puntatore di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="12ac0-105">The **\[iid\_is\]** pointer attribute specifies the IID of the COM interface pointed to by an interface pointer.</span></span>

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a><span data-ttu-id="12ac0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12ac0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ac0-107">*espressione limitata*</span><span class="sxs-lookup"><span data-stu-id="12ac0-107">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="12ac0-108">Specifica un'espressione del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="12ac0-108">Specifies a C-language expression.</span></span> <span data-ttu-id="12ac0-109">Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="12ac0-109">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="12ac0-110">MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento.</span><span class="sxs-lookup"><span data-stu-id="12ac0-110">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12ac0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="12ac0-111">Remarks</span></span>

<span data-ttu-id="12ac0-112">È possibile utilizzare **\[ IID \_ \]** negli elenchi di attributi per i parametri di funzione e per i membri della struttura o dell'Unione.</span><span class="sxs-lookup"><span data-stu-id="12ac0-112">You can use **\[iid\_is\]** in attribute lists for function parameters and for structure or union members.</span></span> <span data-ttu-id="12ac0-113">Gli stub usano l'IID per determinare come eseguire il marshalling del puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="12ac0-113">The stubs use the IID to determine how to marshal the interface pointer.</span></span> <span data-ttu-id="12ac0-114">Questa operazione è utile per un puntatore a interfaccia tipizzato come parametro della classe di base.</span><span class="sxs-lookup"><span data-stu-id="12ac0-114">This is useful for an interface pointer that is typed as a base class parameter.</span></span>

<span data-ttu-id="12ac0-115">I file che usano l' **\[ IID \_ sono \]** attributi devono essere compilati con il compilatore MIDL in modalità predefinita, che non usa l'opzione [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="12ac0-115">Files that use the **\[iid\_is\]** attribute must be compiled with the MIDL compiler in default mode, that is not using the [**/osf**](-osf.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="12ac0-116">Esempi</span><span class="sxs-lookup"><span data-stu-id="12ac0-116">Examples</span></span>

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a><span data-ttu-id="12ac0-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="12ac0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ac0-118">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="12ac0-118">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="12ac0-119">**uuid**</span><span class="sxs-lookup"><span data-stu-id="12ac0-119">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




