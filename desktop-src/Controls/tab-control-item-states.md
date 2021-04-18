---
title: Stati degli elementi di controllo Tab (CommCtrl. h)
description: Gli elementi di controllo struttura a schede supportano ora lo stato di un elemento per supportare il \_ messaggio TCM DESELECTALL. Inoltre, la struttura TCITEM supporta i valori dello stato dell'elemento.
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5214f1a2eee757bfdf5b2a81a8916292b9d7f98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327230"
---
# <a name="tab-control-item-states"></a><span data-ttu-id="de462-104">Stati degli elementi di controllo Tab</span><span class="sxs-lookup"><span data-stu-id="de462-104">Tab Control Item States</span></span>

<span data-ttu-id="de462-105">Gli elementi di controllo struttura a schede supportano ora lo stato di un elemento per supportare il messaggio [**TCM \_ DESELECTALL**](tcm-deselectall.md) .</span><span class="sxs-lookup"><span data-stu-id="de462-105">Tab control items now support an item state to support the [**TCM\_DESELECTALL**](tcm-deselectall.md) message.</span></span> <span data-ttu-id="de462-106">Inoltre, la struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) supporta i valori dello stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="de462-106">Additionally, the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure supports item state values.</span></span>



| <span data-ttu-id="de462-107">Costante</span><span class="sxs-lookup"><span data-stu-id="de462-107">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="de462-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de462-108">Description</span></span>                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <span data-ttu-id="de462-109"><dt>**\_ButtonPressed TCIS**</dt></span><span class="sxs-lookup"><span data-stu-id="de462-109"><dt>**TCIS\_BUTTONPRESSED**</dt></span></span> </dl> | <span data-ttu-id="de462-110">[Versione 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="de462-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="de462-111">L'elemento di controllo Tab è selezionato.</span><span class="sxs-lookup"><span data-stu-id="de462-111">The tab control item is selected.</span></span> <span data-ttu-id="de462-112">Questo stato è significativo solo se è stato impostato il flag di stile dei [**\_ pulsanti TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="de462-112">This state is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span><br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <span data-ttu-id="de462-113"><dt>**TCIS \_ evidenziato**</dt></span><span class="sxs-lookup"><span data-stu-id="de462-113"><dt>**TCIS\_HIGHLIGHTED**</dt></span></span> </dl>       | <span data-ttu-id="de462-114">[Versione 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="de462-114">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="de462-115">L'elemento di controllo Tab è evidenziato e la scheda e il testo vengono disegnati utilizzando il colore di evidenziazione corrente.</span><span class="sxs-lookup"><span data-stu-id="de462-115">The tab control item is highlighted, and the tab and text are drawn using the current highlight color.</span></span> <span data-ttu-id="de462-116">Quando si utilizza un colore elevato, si tratta di un'interpolazione vera, non di un colore con stato.</span><span class="sxs-lookup"><span data-stu-id="de462-116">When using high-color, this will be a true interpolation, not a dithered color.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="de462-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de462-117">Requirements</span></span>



| <span data-ttu-id="de462-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="de462-118">Requirement</span></span> | <span data-ttu-id="de462-119">Valore</span><span class="sxs-lookup"><span data-stu-id="de462-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de462-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de462-120">Header</span></span><br/> | <dl> <span data-ttu-id="de462-121"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="de462-121"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





