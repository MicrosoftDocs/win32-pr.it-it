---
description: Stato del trasporto del dispositivo
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Stato del trasporto del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f52ea846c79be6cb2d011b635da358f7ecd0a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401346"
---
# <a name="device-transport-state"></a><span data-ttu-id="6b320-103">Stato del trasporto del dispositivo</span><span class="sxs-lookup"><span data-stu-id="6b320-103">Device Transport State</span></span>

<span data-ttu-id="6b320-104">Per recuperare lo stato corrente del dispositivo, ad esempio Play, pause o stop, chiamare il metodo [**IAMExtTransport:: Get \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) .</span><span class="sxs-lookup"><span data-stu-id="6b320-104">To retrieve the current state of the device, such as play, pause, or stop, call the [**IAMExtTransport::get\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) method.</span></span> <span data-ttu-id="6b320-105">Il metodo recupera una costante che indica lo stato del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="6b320-105">The method retrieves a constant that indicates the device state:</span></span>



| <span data-ttu-id="6b320-106">Valore</span><span class="sxs-lookup"><span data-stu-id="6b320-106">Value</span></span>                    | <span data-ttu-id="6b320-107">Stato dispositivo</span><span class="sxs-lookup"><span data-stu-id="6b320-107">Device State</span></span> |
|--------------------------|--------------|
| <span data-ttu-id="6b320-108">\_riproduzione in modalità ed \_</span><span class="sxs-lookup"><span data-stu-id="6b320-108">ED\_MODE\_PLAY</span></span>           | <span data-ttu-id="6b320-109">Esegui</span><span class="sxs-lookup"><span data-stu-id="6b320-109">Play</span></span>         |
| <span data-ttu-id="6b320-110">\_arresto modalità \_ ed</span><span class="sxs-lookup"><span data-stu-id="6b320-110">ED\_MODE\_STOP</span></span>           | <span data-ttu-id="6b320-111">Interrompere</span><span class="sxs-lookup"><span data-stu-id="6b320-111">Stop</span></span>         |
| <span data-ttu-id="6b320-112">\_Blocca modalità \_ ed</span><span class="sxs-lookup"><span data-stu-id="6b320-112">ED\_MODE\_FREEZE</span></span>         | <span data-ttu-id="6b320-113">Sospendi</span><span class="sxs-lookup"><span data-stu-id="6b320-113">Pause</span></span>        |
| <span data-ttu-id="6b320-114">\_modalità ed \_ FF</span><span class="sxs-lookup"><span data-stu-id="6b320-114">ED\_MODE\_FF</span></span>             | <span data-ttu-id="6b320-115">Avanzamento rapido</span><span class="sxs-lookup"><span data-stu-id="6b320-115">Fast-forward</span></span> |
| <span data-ttu-id="6b320-116">\_modalità ed \_ r</span><span class="sxs-lookup"><span data-stu-id="6b320-116">ED\_MODE\_REW</span></span>            | <span data-ttu-id="6b320-117">Riavvolgimento rapido</span><span class="sxs-lookup"><span data-stu-id="6b320-117">Rewind</span></span>       |
| <span data-ttu-id="6b320-118">\_record in modalità ed \_</span><span class="sxs-lookup"><span data-stu-id="6b320-118">ED\_MODE\_RECORD</span></span>         | <span data-ttu-id="6b320-119">Registra</span><span class="sxs-lookup"><span data-stu-id="6b320-119">Record</span></span>       |
| <span data-ttu-id="6b320-120">\_blocco del \_ record in modalità ed \_</span><span class="sxs-lookup"><span data-stu-id="6b320-120">ED\_MODE\_RECORD\_FREEZE</span></span> | <span data-ttu-id="6b320-121">Registrare-sospendere</span><span class="sxs-lookup"><span data-stu-id="6b320-121">Record-pause</span></span> |



 

<span data-ttu-id="6b320-122">Il codice seguente controlla lo stato del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="6b320-122">The following code checks the device state:</span></span>


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="6b320-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b320-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b320-124">Controllo di una videocamera DV</span><span class="sxs-lookup"><span data-stu-id="6b320-124">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



