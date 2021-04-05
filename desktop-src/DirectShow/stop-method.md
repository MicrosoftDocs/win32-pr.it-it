---
description: Il metodo Stop interrompe la riproduzione.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Metodo Stop (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968148"
---
# <a name="stop-method-directshow"></a><span data-ttu-id="3934a-103">Metodo Stop (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="3934a-103">Stop Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="3934a-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3934a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3934a-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="3934a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3934a-106">Il `Stop` metodo interrompe la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3934a-106">The `Stop` method stops playback.</span></span>

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a><span data-ttu-id="3934a-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3934a-107">Return Value</span></span>

<span data-ttu-id="3934a-108">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="3934a-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3934a-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3934a-109">Remarks</span></span>

<span data-ttu-id="3934a-110">Se [**EnableResetOnStop**](enableresetonstop-property.md) è impostato su true, la chiamata a `Stop` inserisce lo strumento di navigazione del DVD, insieme al resto del grafico del filtro, nello stato interrotto, il che significa che alla successiva pressione del pulsante **Play** la riproduzione inizia all'inizio del disco. Se **EnableResetOnStop** è impostato su true, la riproduzione riprende dal punto in cui si è interrotta quando l'utente rilascia il comando di **riproduzione** successivo.</span><span class="sxs-lookup"><span data-stu-id="3934a-110">If [**EnableResetOnStop**](enableresetonstop-property.md) is set to true, calling `Stop` puts the DVD Navigator, along with the rest of the filter graph, into a stopped state, which means that the next time the user presses the **Play** button, playback starts at the beginning of the disc. If **EnableResetOnStop** is set to true, playback resumes where it left off when the user issues the next **Play** command.</span></span>

 

 



