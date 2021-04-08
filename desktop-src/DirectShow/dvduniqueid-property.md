---
description: La proprietà DVDUniqueID recupera un numero generato dal sistema che identifica in modo univoco il disco corrente.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: Proprietà DVDUniqueID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23138f348ef1ec71f1506c8892532bd42f1c807d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876569"
---
# <a name="dvduniqueid-property"></a><span data-ttu-id="22eb1-103">Proprietà DVDUniqueID</span><span class="sxs-lookup"><span data-stu-id="22eb1-103">DVDUniqueID Property</span></span>

> [!Note]  
> <span data-ttu-id="22eb1-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="22eb1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="22eb1-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="22eb1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="22eb1-106">La `DVDUniqueID` proprietà recupera un numero generato dal sistema che identifica in modo univoco il disco corrente.</span><span class="sxs-lookup"><span data-stu-id="22eb1-106">The `DVDUniqueID` property retrieves a system-generated number that uniquely identifies the current disc.</span></span>

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a><span data-ttu-id="22eb1-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22eb1-107">Return Value</span></span>

<span data-ttu-id="22eb1-108">Restituisce un valore intero che identifica in modo univoco il disco corrente.</span><span class="sxs-lookup"><span data-stu-id="22eb1-108">Returns an integer value that uniquely identifies the current disc.</span></span>

## <a name="remarks"></a><span data-ttu-id="22eb1-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="22eb1-109">Remarks</span></span>

<span data-ttu-id="22eb1-110">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="22eb1-110">This property is read-only with no default value.</span></span> <span data-ttu-id="22eb1-111">Il numero Identifier (ID) non è assolutamente univoco, ma è univoco per tutti gli scopi pratici.</span><span class="sxs-lookup"><span data-stu-id="22eb1-111">The identifier (ID) number is not absolutely unique, but it is unique for all practical purposes.</span></span> <span data-ttu-id="22eb1-112">L'ID si applica a tutte le copie replicate di un disco. In altre parole, tutte le copie di un film specifico hanno lo stesso ID.</span><span class="sxs-lookup"><span data-stu-id="22eb1-112">The ID applies to all replicated copies of a disc. In other words, all copies of a specific movie have the same ID.</span></span> <span data-ttu-id="22eb1-113">L'ID si basa su dimensioni file, date e altre informazioni e non sul valore BCA.</span><span class="sxs-lookup"><span data-stu-id="22eb1-113">The ID is based on file sizes, dates, and other information, and not the BCA value.</span></span>

 

 



