---
description: Controlla il modo in cui WMI crea o aggiorna le classi a seconda dei flag specificati.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classFlags
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 422185e3b1549d28e6d7004e2032675148d2408e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308841"
---
# <a name="pragma-classflags"></a><span data-ttu-id="cf019-103">pragma classFlags</span><span class="sxs-lookup"><span data-stu-id="cf019-103">pragma classflags</span></span>

<span data-ttu-id="cf019-104">Il comando per il preprocessore **pragma classFlags** controlla il modo in cui WMI crea o aggiorna le classi a seconda dei flag specificati.</span><span class="sxs-lookup"><span data-stu-id="cf019-104">The **pragma classflags** preprocessor command controls the way WMI creates or updates classes depending on the flags specified.</span></span>

<span data-ttu-id="cf019-105">Di seguito viene descritta la sintassi per questo comando:</span><span class="sxs-lookup"><span data-stu-id="cf019-105">The following describes the syntax for this command:</span></span>


```mof
#pragma classflags ("[flag1], [flag2]")
```



<span data-ttu-id="cf019-106">Il *\[ flag \]* deve essere uno o più degli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="cf019-106">*\[Flag\]* must be one or more of the following arguments.</span></span> <span data-ttu-id="cf019-107">È possibile combinare eventuali flag che non si contraddicono tra loro.</span><span class="sxs-lookup"><span data-stu-id="cf019-107">You can combine any flags that do not contradict each other.</span></span>



| <span data-ttu-id="cf019-108">Flag</span><span class="sxs-lookup"><span data-stu-id="cf019-108">Flag</span></span>        | <span data-ttu-id="cf019-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf019-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf019-110">createonly</span><span class="sxs-lookup"><span data-stu-id="cf019-110">createonly</span></span>  | <span data-ttu-id="cf019-111">Indica al compilatore di non apportare modifiche alle classi esistenti e di terminare una compilazione se una classe specificata nel file MOF esiste già in WMI.</span><span class="sxs-lookup"><span data-stu-id="cf019-111">Instructs the compiler not make any changes to existing classes and terminates a compilation if a class specified in the MOF file already exists in WMI.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="cf019-112">ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="cf019-112">forceupdate</span></span> | <span data-ttu-id="cf019-113">Forza gli aggiornamenti delle classi quando esistono classi figlio in conflitto.</span><span class="sxs-lookup"><span data-stu-id="cf019-113">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="cf019-114">Se, ad esempio, si definisce un qualificatore di classe in una classe figlio e la classe di base tenta di aggiungere lo stesso qualificatore, l'utilizzo di questo flag causa la risoluzione del conflitto da parte del compilatore eliminando il qualificatore in conflitto nella classe figlio.</span><span class="sxs-lookup"><span data-stu-id="cf019-114">For example, if you define a class qualifier in a child class and the base class attempts to add the same qualifier, using this flag causes the compiler to resolve this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="cf019-115">Se la classe figlio dispone di istanze, l'aggiornamento avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="cf019-115">If the child class has instances, the update fails.</span></span> |
| <span data-ttu-id="cf019-116">safeupdate</span><span class="sxs-lookup"><span data-stu-id="cf019-116">safeupdate</span></span>  | <span data-ttu-id="cf019-117">Consente al compilatore di aggiornare le classi anche se esistono classi figlio, se la modifica non provoca conflitti con le classi figlio.</span><span class="sxs-lookup"><span data-stu-id="cf019-117">Allows the compiler to update classes even if child classes exist, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="cf019-118">Questo flag, ad esempio, consente di aggiungere una nuova proprietà a una classe di base senza dover aggiungere anche la proprietà a una classe figlio preesistente.</span><span class="sxs-lookup"><span data-stu-id="cf019-118">For example, this flag allows you to add a new property to a base class without also having to add the property to any pre-existing child class.</span></span> <span data-ttu-id="cf019-119">Se le classi figlio hanno istanze, l'aggiornamento avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="cf019-119">If the child classes have instances, the update fails.</span></span>                           |
| <span data-ttu-id="cf019-120">UpdateOnly</span><span class="sxs-lookup"><span data-stu-id="cf019-120">updateonly</span></span>  | <span data-ttu-id="cf019-121">Indica al compilatore di non creare nuove classi e fa in modo che il compilatore interrompa la compilazione se non esiste una classe specificata nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="cf019-121">Instructs the compiler to not create any new classes and causes the compiler to terminate the compilation if a class specified in the MOF file does not exist.</span></span>                                                                                                                                                                                                  |



 

## <a name="examples"></a><span data-ttu-id="cf019-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="cf019-122">Examples</span></span>

<span data-ttu-id="cf019-123">Nell'esempio seguente viene illustrato come utilizzare questo comando con i flag UpdateOnly e ForceUpdate.</span><span class="sxs-lookup"><span data-stu-id="cf019-123">The following example shows how to use this command with the updateonly and forceupdate flags.</span></span>


```mof
#pragma classflags ("updateonly", "forceupdate")
```



## <a name="requirements"></a><span data-ttu-id="cf019-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf019-124">Requirements</span></span>



| <span data-ttu-id="cf019-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf019-125">Requirement</span></span> | <span data-ttu-id="cf019-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cf019-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="cf019-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf019-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cf019-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf019-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="cf019-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf019-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cf019-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf019-130">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf019-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf019-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf019-132">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="cf019-132">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




