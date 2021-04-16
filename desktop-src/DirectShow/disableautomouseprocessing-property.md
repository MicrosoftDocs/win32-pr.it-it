---
description: La proprietà DisableAutoMouseProcessing Abilita o Disabilita la funzionalità di elaborazione del mouse dell'oggetto MSWebDVD.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: Proprietà DisableAutoMouseProcessing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606392acd4030d68af9590555a40d571d70c581
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480860"
---
# <a name="disableautomouseprocessing-property"></a><span data-ttu-id="81518-103">Proprietà DisableAutoMouseProcessing</span><span class="sxs-lookup"><span data-stu-id="81518-103">DisableAutoMouseProcessing Property</span></span>

> [!Note]  
> <span data-ttu-id="81518-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="81518-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="81518-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="81518-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="81518-106">La `DisableAutoMouseProcessing` proprietà Abilita o Disabilita la funzionalità di elaborazione del mouse dell'oggetto **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="81518-106">The `DisableAutoMouseProcessing` property enables or disables the **MSWebDVD** object's mouse-processing functionality.</span></span>

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a><span data-ttu-id="81518-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81518-107">Return Value</span></span>

<span data-ttu-id="81518-108">Restituisce un valore booleano che indica se disabilitare l'elaborazione del mouse predefinita.</span><span class="sxs-lookup"><span data-stu-id="81518-108">Returns a boolean value indicating whether to disable the default mouse processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="81518-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="81518-109">Remarks</span></span>

<span data-ttu-id="81518-110">Questa proprietà è di lettura/scrittura e il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="81518-110">This property is read/write with a default value of false.</span></span> <span data-ttu-id="81518-111">Per impostazione predefinita, l'oggetto **mswebdvd** gestisce automaticamente le azioni del mouse per i menu su schermo DVD. Gli utenti possono evidenziare e attivare i pulsanti di menu senza programmazione speciale da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="81518-111">The **MSWebDVD** object automatically handles mouse actions for DVD on-screen menus by default; users can highlight and activate menu buttons without special programming by the application.</span></span> <span data-ttu-id="81518-112">Un'applicazione può disattivare questa funzionalità predefinita di gestione del mouse impostando questa proprietà su **true**.</span><span class="sxs-lookup"><span data-stu-id="81518-112">An application can turn off this default mouse-handling functionality by setting this property to **true**.</span></span> <span data-ttu-id="81518-113">Quando l'elaborazione automatica del mouse è disattivata, un'applicazione deve utilizzare i vari metodi e proprietà correlati ai pulsanti per gestire i movimenti del mouse e i clic del mouse nei menu sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="81518-113">When the automatic mouse processing is turned off, an application must use the various button-related methods and properties to handle mouse moves and mouse clicks on the on-screen menus.</span></span> <span data-ttu-id="81518-114">Inoltre, un'applicazione può utilizzare i metodi correlati ai pulsanti per sostituire la gestione automatica del mouse anche quando `DisableAutoMouseProcessing` è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="81518-114">Also, an application can use the button-related methods to override the automatic mouse handling even when when `DisableAutoMouseProcessing` is set to **false**.</span></span>

 

 



