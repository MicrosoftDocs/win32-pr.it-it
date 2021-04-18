---
title: /c_ext opzione
description: Questa opzione è obsoleta a partire dalla versione 3,0 del compilatore MIDL. Tuttavia, l'utilizzo dell' \_ opzione c ext non genererà un errore del compilatore, pertanto non è necessario rimuovere i riferimenti a/MS \_ ext o/c \_ ext da un makefile esistente.
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /c_ext switch MIDL
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299217"
---
# <a name="c_ext-switch"></a><span data-ttu-id="ee8ef-105">\_opzione/c EXT</span><span class="sxs-lookup"><span data-stu-id="ee8ef-105">/c\_ext switch</span></span>

<span data-ttu-id="ee8ef-106">Questa opzione è obsoleta a partire dalla versione 3,0 del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="ee8ef-106">This switch is obsolete as of version 3.0 of the MIDL compiler.</span></span> <span data-ttu-id="ee8ef-107">Tuttavia, l'utilizzo dell'opzione **c \_ ext** non genererà un errore del compilatore, pertanto non è necessario rimuovere i riferimenti a [**/MS \_ ext**](-ms-ext.md) o **/c \_ ext** da un makefile esistente.</span><span class="sxs-lookup"><span data-stu-id="ee8ef-107">However, using the **c\_ext** switch will not generate a compiler error, so you do not have to remove references to [**/ms\_ext**](-ms-ext.md) or **/c\_ext** from an existing makefile.</span></span>

``` syntax
midl /c_ext
```

## <a name="switch-options"></a><span data-ttu-id="ee8ef-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="ee8ef-108">Switch Options</span></span>

<span data-ttu-id="ee8ef-109">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="ee8ef-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee8ef-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee8ef-110">Remarks</span></span>

<span data-ttu-id="ee8ef-111">Le funzionalità seguenti sono ora disponibili per impostazione predefinita:</span><span class="sxs-lookup"><span data-stu-id="ee8ef-111">The following features are now available by default:</span></span>

-   <span data-ttu-id="ee8ef-112">Molti file di intestazione esistenti definiscono i tipi con qualificatori, ad esempio **lontano** e **stdcall**, che non fanno parte dell'IDL DCE.</span><span class="sxs-lookup"><span data-stu-id="ee8ef-112">Many existing header files define types with qualifiers, such as **far** and **stdcall**, that are not part of the DCE IDL.</span></span> <span data-ttu-id="ee8ef-113">Tali compilatori (e il compilatore MIDL in modalità di compatibilità DCE) generano errori quando tentano di elaborare questi qualificatori.</span><span class="sxs-lookup"><span data-stu-id="ee8ef-113">Those compilers (and the MIDL compiler in DCE-compatibility mode) generate errors when they attempt to process these qualifiers.</span></span> <span data-ttu-id="ee8ef-114">Il compilatore MIDL consente di compilare file IDL che contengono questi qualificatori.</span><span class="sxs-lookup"><span data-stu-id="ee8ef-114">The MIDL compiler allows you to compile IDL files that contain these qualifiers.</span></span> <span data-ttu-id="ee8ef-115">I qualificatori di tipo non influiscono sulla modalità di trasmissione dei dati sulla rete.</span><span class="sxs-lookup"><span data-stu-id="ee8ef-115">The type qualifiers do not affect the way the data is transmitted on the network.</span></span>
-   <span data-ttu-id="ee8ef-116">È possibile omettere gli attributi direzionali, ad esempio [**\[ all'interno o all' \]**](in.md) [**\[ esterno \]**](out-idl.md).</span><span class="sxs-lookup"><span data-stu-id="ee8ef-116">You can omit directional attributes such as [**\[in\]**](in.md) or [**\[out\]**](out-idl.md).</span></span>

<span data-ttu-id="ee8ef-117">Le estensioni del linguaggio C seguenti sono supportate in modalità predefinita:</span><span class="sxs-lookup"><span data-stu-id="ee8ef-117">The following C-language extensions are supported in default mode:</span></span>

-   <span data-ttu-id="ee8ef-118">Campi di bit in strutture e unioni</span><span class="sxs-lookup"><span data-stu-id="ee8ef-118">Bit fields in structures and unions</span></span>
-   <span data-ttu-id="ee8ef-119">Commenti che iniziano con due barre (//)</span><span class="sxs-lookup"><span data-stu-id="ee8ef-119">Comments that start with two slash characters (//)</span></span>
-   <span data-ttu-id="ee8ef-120">Dichiarazioni esterne</span><span class="sxs-lookup"><span data-stu-id="ee8ef-120">External declarations</span></span>
-   <span data-ttu-id="ee8ef-121">Procedure con ellissi nell'elenco di parametri (...)</span><span class="sxs-lookup"><span data-stu-id="ee8ef-121">Procedures with ellipses in the parameter list (…)</span></span>
-   <span data-ttu-id="ee8ef-122">Sulle piattaforme a 32 bit, [**int**](int.md) è un tipo di base a 32 bit nativo; nelle piattaforme a 16 bit, **int** è riconosciuto ma non è un tipo utilizzabile in remoto</span><span class="sxs-lookup"><span data-stu-id="ee8ef-122">On 32-bit platforms, [**int**](int.md) is a native 32-bit base type; on 16-bit platforms, **int** is recognized but is not a remotable type</span></span>
-   <span data-ttu-id="ee8ef-123">Tipo [**void \***](void.md) non usato nelle operazioni remote</span><span class="sxs-lookup"><span data-stu-id="ee8ef-123">Type [**void \***](void.md) that is not used in remote operations</span></span>
-   <span data-ttu-id="ee8ef-124">I qualificatori di tipo, incluso il form con il prefisso ANSI-conforme, contengono due caratteri di sottolineatura: **cdecl**, **\_ \_ cdecl**, [**const**](const.md), **\_ \_ const**, **Export**, **\_ \_ Export**, **lontano**, **\_ \_ faraway**, **loadds**, **\_ \_ loadds**, **near**, **\_ \_ near**, **Pascal**, **\_ \_ Pascal**, **stdcall**, **\_ \_ stdcall**, **volatile** e **\_ \_ volatile**.</span><span class="sxs-lookup"><span data-stu-id="ee8ef-124">Type qualifiers—including the form with the ANSI-conformant prefix—contain two underscore characters: **cdecl**, **\_\_cdecl**, [**const**](const.md), **\_\_const**, **export**, **\_\_export**, **far**, **\_\_far**, **loadds**, **\_\_loadds**, **near**, **\_\_near**, **pascal**, **\_\_pascal**, **stdcall**, **\_\_stdcall**, **volatile**, and **\_\_volatile**.</span></span>

<span data-ttu-id="ee8ef-125">Per ulteriori informazioni sui qualificatori di dichiarazione, vedere la documentazione di Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="ee8ef-125">For more information about declaration qualifiers, see your Microsoft C/C++ documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee8ef-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee8ef-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee8ef-127">**configurazione di/app \_**</span><span class="sxs-lookup"><span data-stu-id="ee8ef-127">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="ee8ef-128">**/osf**</span><span class="sxs-lookup"><span data-stu-id="ee8ef-128">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="ee8ef-129">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="ee8ef-129">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




