---
title: attributo enum
description: La parola chiave enum identifica un tipo enumerato.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- attributo di enumerazione MIDL
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681244c9d852c25d8e63ad389b03f16e6db8148c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333588"
---
# <a name="enum-attribute"></a><span data-ttu-id="0de50-104">attributo enum</span><span class="sxs-lookup"><span data-stu-id="0de50-104">enum attribute</span></span>

<span data-ttu-id="0de50-105">La parola chiave **enum** identifica un tipo enumerato.</span><span class="sxs-lookup"><span data-stu-id="0de50-105">The keyword **enum** identifies an enumerated type.</span></span>

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a><span data-ttu-id="0de50-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0de50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0de50-107">*tag*</span><span class="sxs-lookup"><span data-stu-id="0de50-107">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="0de50-108">Specifica un tag facoltativo per il tipo enumerato.</span><span class="sxs-lookup"><span data-stu-id="0de50-108">Specifies an optional tag for the enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="0de50-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="0de50-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="0de50-110">Specifica l'enumerazione particolare.</span><span class="sxs-lookup"><span data-stu-id="0de50-110">Specifies the particular enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="0de50-111">*valore integer*</span><span class="sxs-lookup"><span data-stu-id="0de50-111">*integer-value*</span></span> 
</dt> <dd>

<span data-ttu-id="0de50-112">Specifica un valore intero costante.</span><span class="sxs-lookup"><span data-stu-id="0de50-112">Specifies a constant integer value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0de50-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0de50-113">Remarks</span></span>

<span data-ttu-id="0de50-114">i tipi **enum** possono apparire come identificatori di tipo nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come funzione-Return-Type o come identificatore di tipo parametro).</span><span class="sxs-lookup"><span data-stu-id="0de50-114">**enum** types can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (either as the function-return-type or as a parameter-type specifier).</span></span> <span data-ttu-id="0de50-115">Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="0de50-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="0de50-116">Nella modalità predefinita del compilatore MIDL è possibile assegnare valori integer agli enumeratori.</span><span class="sxs-lookup"><span data-stu-id="0de50-116">In the MIDL compiler's default mode, you can assign integer values to enumerators.</span></span> <span data-ttu-id="0de50-117">Questa funzionalità non è disponibile quando si esegue la compilazione con l'opzione [**/OSF**](-osf.md) . Come per gli enumeratori del linguaggio C, i nomi degli enumeratori devono essere univoci, ma i valori di enumeratore non devono essere.</span><span class="sxs-lookup"><span data-stu-id="0de50-117">(This feature is not available when you compile with the [**/osf**](-osf.md) switch.) As with C-language enumerators, enumerator names must be unique, but the enumerator values need not be.</span></span>

<span data-ttu-id="0de50-118">Quando gli operatori di assegnazione non vengono specificati, viene eseguito il mapping degli identificatori a numeri interi consecutivi da sinistra a destra, a partire da zero.</span><span class="sxs-lookup"><span data-stu-id="0de50-118">When assignment operators are not provided, identifiers are mapped to consecutive integers from left to right, starting with zero.</span></span> <span data-ttu-id="0de50-119">Quando vengono specificati gli operatori di assegnazione, i valori assegnati iniziano dal valore assegnato più di recente.</span><span class="sxs-lookup"><span data-stu-id="0de50-119">When assignment operators are provided, assigned values start from the most recently assigned value.</span></span>

<span data-ttu-id="0de50-120">Il numero massimo di identificatori è 65.535.</span><span class="sxs-lookup"><span data-stu-id="0de50-120">The maximum number of identifiers is 65,535.</span></span>

<span data-ttu-id="0de50-121">Gli oggetti di tipo **enum** sono tipi [**int**](int.md) e le relative dimensioni sono dipendenti dal sistema.</span><span class="sxs-lookup"><span data-stu-id="0de50-121">Objects of type **enum** are [**int**](int.md) types, and their size is system-dependent.</span></span> <span data-ttu-id="0de50-122">Per impostazione predefinita, gli oggetti di tipi **enum** vengono considerati oggetti a 16 bit di tipo [**unsigned**](unsigned.md) [**short**](short.md) quando vengono trasmessi in rete.</span><span class="sxs-lookup"><span data-stu-id="0de50-122">By default, objects of **enum** types are treated as 16-bit objects of type [**unsigned**](unsigned.md) [**short**](short.md) when transmitted over a network.</span></span> <span data-ttu-id="0de50-123">I valori non compresi nell'intervallo compreso tra 0 e 32.767 determinano il valore dell'enumerazione RPC X dell'eccezione in fase di esecuzione non \_ \_ compreso nell' \_ \_ \_ \_ intervallo.</span><span class="sxs-lookup"><span data-stu-id="0de50-123">Values outside the range 0 - 32,767 cause the run-time exception RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="0de50-124">Per trasmettere oggetti come entità a 32 bit, applicare l' **\[** [**attributo \_ enum V1**](v1-enum.md) **\]** al typedef **enum** .</span><span class="sxs-lookup"><span data-stu-id="0de50-124">To transmit objects as 32-bit entities, apply the **\[**[**v1\_enum**](v1-enum.md)**\]** attribute to the **enum** typedef.</span></span>

## <a name="examples"></a><span data-ttu-id="0de50-125">Esempi</span><span class="sxs-lookup"><span data-stu-id="0de50-125">Examples</span></span>

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a><span data-ttu-id="0de50-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0de50-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0de50-127">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="0de50-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0de50-128">**INT**</span><span class="sxs-lookup"><span data-stu-id="0de50-128">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="0de50-129">**short**</span><span class="sxs-lookup"><span data-stu-id="0de50-129">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="0de50-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="0de50-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="0de50-131">**unsigned**</span><span class="sxs-lookup"><span data-stu-id="0de50-131">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="0de50-132">**\_enum V1**</span><span class="sxs-lookup"><span data-stu-id="0de50-132">**v1\_enum**</span></span>](v1-enum.md)
</dt> </dl>

 

 




