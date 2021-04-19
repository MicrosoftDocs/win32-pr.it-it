---
description: Il metodo ActivateButton attiva il pulsante di menu selezionato.
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: Metodo ActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8a463a3aad1ee0dcabc0e5daaa4a4969efa37aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304210"
---
# <a name="activatebutton-method"></a><span data-ttu-id="e77b7-103">Metodo ActivateButton</span><span class="sxs-lookup"><span data-stu-id="e77b7-103">ActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="e77b7-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e77b7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e77b7-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e77b7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e77b7-106">Il metodo ActivateButton attiva il pulsante di menu selezionato.</span><span class="sxs-lookup"><span data-stu-id="e77b7-106">The ActivateButton method activates the selected menu button.</span></span>

``` syntax
        MSWebDVD.ActivateButton()
```

## <a name="return-value"></a><span data-ttu-id="e77b7-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e77b7-107">Return Value</span></span>

<span data-ttu-id="e77b7-108">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="e77b7-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e77b7-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="e77b7-109">Remarks</span></span>

<span data-ttu-id="e77b7-110">Utilizzare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione di [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="e77b7-110">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="e77b7-111">Usare questo metodo per attivare un pulsante che è stato selezionato tramite il metodo [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md)o [**SelectRightButton**](selectrightbutton-method.md) .</span><span class="sxs-lookup"><span data-stu-id="e77b7-111">Use this method to activate a button that has been selected through the [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), or [**SelectRightButton**](selectrightbutton-method.md) method.</span></span>

 

 



