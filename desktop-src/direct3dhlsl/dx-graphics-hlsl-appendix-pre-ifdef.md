---
title: " Direttive ifdef e ifndef"
description: Direttive per il preprocessore che determinano se una specifica costante o macro del preprocessore è definita.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- Direttive ifdef e ifndef HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 338308b58f1cdc68ec78984e65ffbf056a36b10b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045742"
---
# <a name="ifdef-and-ifndef-directives"></a><span data-ttu-id="b68cd-104">\#\#direttive ifdef e ifndef</span><span class="sxs-lookup"><span data-stu-id="b68cd-104">\#ifdef and \#ifndef Directives</span></span>

<span data-ttu-id="b68cd-105">Direttive per il preprocessore che determinano se una specifica costante o macro del preprocessore è definita.</span><span class="sxs-lookup"><span data-stu-id="b68cd-105">Preprocessor directives that determine whether a specific preprocessor constant or macro is defined.</span></span>



| <span data-ttu-id="b68cd-106">\#*identificatore* ifdef...</span><span class="sxs-lookup"><span data-stu-id="b68cd-106">\#ifdef *identifier* ...</span></span>  |
|---------------------------|
| <span data-ttu-id="b68cd-107">\#endif</span><span class="sxs-lookup"><span data-stu-id="b68cd-107">\#endif</span></span>                   |
| <span data-ttu-id="b68cd-108">\#*identificatore* ifndef...</span><span class="sxs-lookup"><span data-stu-id="b68cd-108">\#ifndef *identifier* ...</span></span> |
| <span data-ttu-id="b68cd-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="b68cd-109">\#endif</span></span>                   |



 

## <a name="parameters"></a><span data-ttu-id="b68cd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b68cd-110">Parameters</span></span>



| <span data-ttu-id="b68cd-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="b68cd-111">Item</span></span>                                                                              | <span data-ttu-id="b68cd-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b68cd-112">Description</span></span>                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b68cd-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*identificatore*</span><span class="sxs-lookup"><span data-stu-id="b68cd-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="b68cd-114">Identificatore della costante o della macro da verificare.</span><span class="sxs-lookup"><span data-stu-id="b68cd-114">Identifier of the constant or macro to check.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b68cd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b68cd-115">Remarks</span></span>

<span data-ttu-id="b68cd-116">È possibile utilizzare le \# \# direttive ifdef e ifndef in qualsiasi punto [ \# ](dx-graphics-hlsl-appendix-pre-if.md) in cui è possibile utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b68cd-116">You can use the \#ifdef and \#ifndef directives anywhere that the [\#if](dx-graphics-hlsl-appendix-pre-if.md) can be used.</span></span> <span data-ttu-id="b68cd-117">L' \# istruzione ifdef è equivalente alla direttiva.</span><span class="sxs-lookup"><span data-stu-id="b68cd-117">The \#ifdef statement is equivalent to ) directive.</span></span> <span data-ttu-id="b68cd-118">Queste direttive controllano solo la presenza o l'assenza di identificatori definiti usando la direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) , non per gli identificatori dichiarati nel codice sorgente C o C++.</span><span class="sxs-lookup"><span data-stu-id="b68cd-118">These directives check only for the presence or absence of identifiers defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive, not for identifiers declared in the C or C++ source code.</span></span>

<span data-ttu-id="b68cd-119">Queste direttive sono fornite solo per compatibilità con le versioni precedenti del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="b68cd-119">These directives are provided only for compatibility with previous versions of the language.</span></span> <span data-ttu-id="b68cd-120">È preferibile usare l'operatore [definito](dx-graphics-hlsl-appendix-pre-if.md) con la \# direttiva if.</span><span class="sxs-lookup"><span data-stu-id="b68cd-120">The use of the [defined](dx-graphics-hlsl-appendix-pre-if.md) operator with the \#if directive is preferred.</span></span>

<span data-ttu-id="b68cd-121">La \# direttiva ifndef controlla l'opposto della condizione controllata da \# ifdef.</span><span class="sxs-lookup"><span data-stu-id="b68cd-121">The \#ifndef directive checks for the opposite of the condition checked by \#ifdef.</span></span> <span data-ttu-id="b68cd-122">Se l'identificatore non è definito, la condizione è true (diverso da zero); in caso contrario, la condizione è false (zero).</span><span class="sxs-lookup"><span data-stu-id="b68cd-122">If the identifier is not defined, the condition is true (nonzero); otherwise, the condition is false (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="b68cd-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="b68cd-123">Examples</span></span>

<span data-ttu-id="b68cd-124">L'identifier può essere passato dalla riga di comando utilizzando l'opzione /D.</span><span class="sxs-lookup"><span data-stu-id="b68cd-124">The identifier can be passed from the command line using the /D option.</span></span> <span data-ttu-id="b68cd-125">È possibile specificare fino a 30 macro utilizzando /D.</span><span class="sxs-lookup"><span data-stu-id="b68cd-125">Up to 30 macros can be specified with /D.</span></span> <span data-ttu-id="b68cd-126">Ciò è utile per controllare l'esistenza di una definizione poiché una definizione può essere passata dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b68cd-126">This is useful for checking whether a definition exists, because a definition can be passed from the command line.</span></span> <span data-ttu-id="b68cd-127">Nell'esempio seguente viene usato questo comportamento per determinare se eseguire un'applicazione in modalità test.</span><span class="sxs-lookup"><span data-stu-id="b68cd-127">The following example uses this behavior to determine whether to run an application in test mode.</span></span>


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



<span data-ttu-id="b68cd-128">Quando viene compilato usando il comando seguente, PROG. cpp verrà compilato in modalità test. in caso contrario, verrà compilato in modalità finale.</span><span class="sxs-lookup"><span data-stu-id="b68cd-128">When compiled using the following command, prog.cpp will compile in test mode; otherwise, it will compile in final mode.</span></span>


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a><span data-ttu-id="b68cd-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b68cd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b68cd-130">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b68cd-130">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="b68cd-131">\#Se,)</span><span class="sxs-lookup"><span data-stu-id="b68cd-131">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





