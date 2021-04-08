---
description: La proprietà EnableResetOnStop imposta o recupera un valore che determina il modo in cui riprenderà la riproduzione quando il grafico del filtro esegue una transizione da uno stato interrotto.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Proprietà EnableResetOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9449d8dd3e2e5ab0e1f008cba3e4cb2aabaa78c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746647"
---
# <a name="enableresetonstop-property"></a><span data-ttu-id="b244b-103">Proprietà EnableResetOnStop</span><span class="sxs-lookup"><span data-stu-id="b244b-103">EnableResetOnStop Property</span></span>

> [!Note]  
> <span data-ttu-id="b244b-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b244b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b244b-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="b244b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b244b-106">La `EnableResetOnStop` proprietà imposta o recupera un valore che determina il modo in cui riprenderà la riproduzione quando il grafico del filtro esegue una transizione da uno stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="b244b-106">The `EnableResetOnStop` property sets or retrieves a value that determines how play will resume when the filter graph makes a transition from a stopped state.</span></span>

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a><span data-ttu-id="b244b-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b244b-107">Return Value</span></span>

<span data-ttu-id="b244b-108">Restituisce un valore booleano che indica la posizione in cui l'oggetto MSWebDVD verrà riprodotto dopo l'arresto del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="b244b-108">Returns a Boolean value indicating where the MSWebDVD object will start playing again after the filter graph is stopped.</span></span>

## <a name="remarks"></a><span data-ttu-id="b244b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b244b-109">Remarks</span></span>

<span data-ttu-id="b244b-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b244b-110">This property is read/write.</span></span>

<span data-ttu-id="b244b-111">I valori possibili di questa proprietà sono: e il valore predefinito è true.</span><span class="sxs-lookup"><span data-stu-id="b244b-111">The possible values of this property are: with a default value of true.</span></span>



| <span data-ttu-id="b244b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b244b-112">Value</span></span> | <span data-ttu-id="b244b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b244b-113">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b244b-114">true</span><span class="sxs-lookup"><span data-stu-id="b244b-114">true</span></span>  | <span data-ttu-id="b244b-115">Il navigatore DVD si reimposta e avvia la riproduzione dall'inizio del disco. Questo è il valore predefinito</span><span class="sxs-lookup"><span data-stu-id="b244b-115">DVD Navigator will reset and start play from the beginning of the disc. This is the default value</span></span> |
| <span data-ttu-id="b244b-116">false</span><span class="sxs-lookup"><span data-stu-id="b244b-116">false</span></span> | <span data-ttu-id="b244b-117">Il navigatore DVD riprenderà la riproduzione da dove era stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="b244b-117">DVD Navigator will resume play where it left off.</span></span>                                                 |



 

 

 



