---
description: Il rettangolo di delimitazione di tutti i monitoraggi è lo schermo virtuale. Il desktop copre lo schermo virtuale invece di un singolo monitor. Nella figura seguente viene illustrata una possibile disposizione di tre monitoraggi.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: Schermata virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4550ab0f849b90523842e6cc4e093c238ff11cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995125"
---
# <a name="the-virtual-screen"></a><span data-ttu-id="93feb-105">Schermata virtuale</span><span class="sxs-lookup"><span data-stu-id="93feb-105">The Virtual Screen</span></span>

<span data-ttu-id="93feb-106">Il rettangolo di delimitazione di tutti i monitoraggi è lo *schermo virtuale*.</span><span class="sxs-lookup"><span data-stu-id="93feb-106">The bounding rectangle of all the monitors is the *virtual screen*.</span></span> <span data-ttu-id="93feb-107">Il desktop copre lo schermo virtuale invece di un singolo monitor.</span><span class="sxs-lookup"><span data-stu-id="93feb-107">The desktop covers the virtual screen instead of a single monitor.</span></span> <span data-ttu-id="93feb-108">Nella figura seguente viene illustrata una possibile disposizione di tre monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="93feb-108">The following illustration shows a possible arrangement of three monitors.</span></span>

![illustrazione che mostra tre caselle che rappresentano i monitoraggi disposti in una casella che rappresenta lo schermo virtuale](images/multimon-1.png)

<span data-ttu-id="93feb-110">Il *monitoraggio primario* contiene l'origine (0,0).</span><span class="sxs-lookup"><span data-stu-id="93feb-110">The *primary monitor* contains the origin (0,0).</span></span> <span data-ttu-id="93feb-111">Ciò è per la compatibilità con le applicazioni esistenti che prevedono un monitoraggio con un'origine.</span><span class="sxs-lookup"><span data-stu-id="93feb-111">This is for compatibility with existing applications that expect a monitor with an origin.</span></span> <span data-ttu-id="93feb-112">Il monitoraggio primario, tuttavia, non deve trovarsi nella parte superiore sinistra dello schermo virtuale.</span><span class="sxs-lookup"><span data-stu-id="93feb-112">However, the primary monitor does not have to be in the upper left of the virtual screen.</span></span> <span data-ttu-id="93feb-113">Nella figura 1 si trova vicino al centro.</span><span class="sxs-lookup"><span data-stu-id="93feb-113">In Figure 1, it is near the center.</span></span> <span data-ttu-id="93feb-114">Quando il monitoraggio primario non si trova in alto a sinistra dello schermo virtuale, parti dello schermo virtuale presentano coordinate negative.</span><span class="sxs-lookup"><span data-stu-id="93feb-114">When the primary monitor is not in the upper left of the virtual screen, parts of the virtual screen have negative coordinates.</span></span> <span data-ttu-id="93feb-115">Poiché la disposizione dei monitoraggi è impostata dall'utente, tutte le applicazioni devono essere progettate per funzionare con coordinate negative.</span><span class="sxs-lookup"><span data-stu-id="93feb-115">Because the arrangement of monitors is set by the user, all applications should be designed to work with negative coordinates.</span></span> <span data-ttu-id="93feb-116">Per ulteriori informazioni, vedere [considerazioni su più monitor per i programmi precedenti](multiple-monitor-considerations-for-older-programs.md).</span><span class="sxs-lookup"><span data-stu-id="93feb-116">For more information, see [Multiple Monitor Considerations for Older Programs](multiple-monitor-considerations-for-older-programs.md).</span></span>

<span data-ttu-id="93feb-117">Le coordinate dello schermo virtuale sono rappresentate da un valore a 16 bit con segno a causa dei valori a 16 bit contenuti in molti messaggi esistenti.</span><span class="sxs-lookup"><span data-stu-id="93feb-117">The coordinates of the virtual screen are represented by a signed 16-bit value because of the 16-bit values contained in many existing messages.</span></span> <span data-ttu-id="93feb-118">Quindi, i limiti dello schermo virtuale sono:</span><span class="sxs-lookup"><span data-stu-id="93feb-118">Thus, the bounds of the virtual screen are:</span></span>

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



