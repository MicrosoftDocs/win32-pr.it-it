---
title: Stringhe di formato delle procedure
description: Di seguito è riportata una descrizione della stringa di formato completa. Assembla tutti i livelli correlati alle diverse fasi dell'evoluzione dell'interprete.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e58a9acf10caad23063bdba117dc402e411638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963318"
---
# <a name="procedure-format-strings"></a><span data-ttu-id="4190a-104">Stringhe di formato delle procedure</span><span class="sxs-lookup"><span data-stu-id="4190a-104">Procedure Format Strings</span></span>

<span data-ttu-id="4190a-105">Di seguito è riportata una descrizione della stringa di formato completa.</span><span class="sxs-lookup"><span data-stu-id="4190a-105">The following is a complete format string description.</span></span> <span data-ttu-id="4190a-106">Assembla tutti i livelli correlati alle diverse fasi dell'evoluzione dell'interprete.</span><span class="sxs-lookup"><span data-stu-id="4190a-106">It assembles all layers related to different stages of the interpreter evolution.</span></span>

## <a name="procedure-descriptor-overview"></a><span data-ttu-id="4190a-107">Panoramica del descrittore di procedure</span><span class="sxs-lookup"><span data-stu-id="4190a-107">Procedure Descriptor Overview</span></span>

<span data-ttu-id="4190a-108">Un descrittore di routine è costituito dai descrittori di intestazione e dai descrittori di parametro.</span><span class="sxs-lookup"><span data-stu-id="4190a-108">A procedure descriptor consists of the header descriptors and the parameter descriptors.</span></span> <span data-ttu-id="4190a-109">La descrizione dello stile [**-OI**](/windows/desktop/Midl/-oi) è considerata obsoleta in termini di utilizzo comune nella programmazione RPC corrente.</span><span class="sxs-lookup"><span data-stu-id="4190a-109">The [**–Oi**](/windows/desktop/Midl/-oi) style description is considered outdated, in terms of common usage in current RPC programming.</span></span> <span data-ttu-id="4190a-110">**-OIF** è considerato più aggiornato.</span><span class="sxs-lookup"><span data-stu-id="4190a-110">The **–Oif** is considered more current.</span></span>

## <a name="the-oi-style-description"></a><span data-ttu-id="4190a-111">Descrizione dello stile-OI</span><span class="sxs-lookup"><span data-stu-id="4190a-111">The –Oi Style Description</span></span>

<span data-ttu-id="4190a-112">Questa descrizione è costituita dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4190a-112">This description consists of the following:</span></span>

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

<span data-ttu-id="4190a-113">L'intestazione avrà da 6 a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="4190a-113">The header would have from 6 to 16 bytes.</span></span>

<span data-ttu-id="4190a-114">La descrizione completa viene generata durante la compilazione in modalità [**-OI**](/windows/desktop/Midl/-oi) .</span><span class="sxs-lookup"><span data-stu-id="4190a-114">The complete description is generated when compiling in [**–Oi**](/windows/desktop/Midl/-oi) mode.</span></span> <span data-ttu-id="4190a-115">In [**-modalità sistema operativo**](/windows/desktop/Midl/-os) vengono generati solo i descrittori di parametro, che vengono usati per la conversione.</span><span class="sxs-lookup"><span data-stu-id="4190a-115">In [**–Os**](/windows/desktop/Midl/-os) mode, only the parameter descriptors are generated, which are used for conversion.</span></span> <span data-ttu-id="4190a-116">L'interprete di selezione USA descrittori di parametri di stile obsoleti.</span><span class="sxs-lookup"><span data-stu-id="4190a-116">The pickling interpreter uses old style parameter descriptors.</span></span>

## <a name="the-oif-style-description"></a><span data-ttu-id="4190a-117">Descrizione dello stile – OIF</span><span class="sxs-lookup"><span data-stu-id="4190a-117">The –Oif Style Description</span></span>

<span data-ttu-id="4190a-118">La descrizione è costituita dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4190a-118">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

<span data-ttu-id="4190a-119">Il descrittore di intestazione di stile [**– OIF**](/windows/desktop/Midl/-oi) è costituito da</span><span class="sxs-lookup"><span data-stu-id="4190a-119">The [**–Oif**](/windows/desktop/Midl/-oi) style header descriptor consists of</span></span>

<span data-ttu-id="4190a-120">La descrizione dello stile – OIF viene generata durante la compilazione in modalità [**– OIF**](/windows/desktop/Midl/-oi) o **– Oicf** del compilatore.</span><span class="sxs-lookup"><span data-stu-id="4190a-120">The –Oif style description is generated when compiling in [**–Oif**](/windows/desktop/Midl/-oi) or **–Oicf** mode of the compiler.</span></span>

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

<span data-ttu-id="4190a-121">Alcune funzionalità più recenti come pipe, Async e [**/robust**](/windows/desktop/Midl/-robust) forzano la modalità [**– Oicf**](/windows/desktop/Midl/-oi) del compilatore, quando vengono usate.</span><span class="sxs-lookup"><span data-stu-id="4190a-121">Some more recent features like pipe, async, and [**/robust**](/windows/desktop/Midl/-robust) force the [**–Oicf**](/windows/desktop/Midl/-oi) mode of the compiler, when used.</span></span>

## <a name="the-extended-oif-description"></a><span data-ttu-id="4190a-122">Descrizione estesa-OIF</span><span class="sxs-lookup"><span data-stu-id="4190a-122">The Extended –Oif Description</span></span>

<span data-ttu-id="4190a-123">La descrizione è costituita dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4190a-123">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 