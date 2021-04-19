---
description: La proprietà WindowlessActivation Inizializza l'oggetto MSWebDVD in fase di progettazione per la modalità finestra o senza finestra.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Proprietà WindowlessActivation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427fdcb265d60200bfe8716cd1ece384861fbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317828"
---
# <a name="windowlessactivation-property"></a><span data-ttu-id="268a8-103">Proprietà WindowlessActivation</span><span class="sxs-lookup"><span data-stu-id="268a8-103">WindowlessActivation Property</span></span>

> [!Note]  
> <span data-ttu-id="268a8-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="268a8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="268a8-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="268a8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="268a8-106">La `WindowlessActivation` Proprietà Inizializza l'oggetto **mswebdvd** in fase di progettazione per la modalità finestra o senza finestra.</span><span class="sxs-lookup"><span data-stu-id="268a8-106">The `WindowlessActivation` property initializes the **MSWebDVD** object at design time for either windowed or windowless mode.</span></span>

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a><span data-ttu-id="268a8-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="268a8-107">Return Value</span></span>

<span data-ttu-id="268a8-108">Restituisce un valore che indica se l'oggetto è in modalità finestra come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="268a8-108">Returns whether the object is in windowed mode as a Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="268a8-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="268a8-109">Remarks</span></span>

<span data-ttu-id="268a8-110">Questa proprietà è di lettura/scrittura e il valore predefinito è true.</span><span class="sxs-lookup"><span data-stu-id="268a8-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="268a8-111">Pertanto, è necessario impostare questa proprietà solo se si esegue l'oggetto **mswebdvd** in un contenitore a finestra.</span><span class="sxs-lookup"><span data-stu-id="268a8-111">Therefore, you only need to set this property if you are running the **MSWebDVD** object in a windowed container.</span></span> <span data-ttu-id="268a8-112">Quando è contenuto in una pagina Web di Microsoft® Internet Explorer, **mswebdvd** è sempre in modalità senza finestra e non è necessario impostare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="268a8-112">When contained in a Web page in Microsoft® Internet Explorer, **MSWebDVD** is always in windowless mode, and you don't need to set this property.</span></span>

 

 



