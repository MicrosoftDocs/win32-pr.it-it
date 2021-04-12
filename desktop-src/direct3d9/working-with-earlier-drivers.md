---
description: In questa sezione vengono elencati i problemi che possono verificarsi quando si utilizza Direct3D 9 su driver scritti per versioni di Direct3D precedenti a Direct3D 9.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Utilizzo di driver precedenti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76567bc4778924835e20a476b03dc94ea77739fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401105"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a><span data-ttu-id="74c79-103">Utilizzo di driver precedenti (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="74c79-103">Working with Earlier Drivers (Direct3D 9)</span></span>

<span data-ttu-id="74c79-104">In questa sezione vengono elencati i problemi che possono verificarsi quando si utilizza Direct3D 9 su driver scritti per versioni di Direct3D precedenti a Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="74c79-104">This section lists issues that can be encountered when working with Direct3D 9 on drivers written for versions of Direct3D earlier than Direct3D 9.</span></span>

-   <span data-ttu-id="74c79-105">Quando si usa un dispositivo T&L HAL, l'intensità della nebbia viene calcolata, ma l'operazione di valore assoluto non viene applicata a questo valore.</span><span class="sxs-lookup"><span data-stu-id="74c79-105">When working with a T&L HAL device, the fog intensity is computed but the absolute value operation is not applied to this value.</span></span> <span data-ttu-id="74c79-106">Il valore viene invece lasciato negativo se corrisponde a quello calcolato.</span><span class="sxs-lookup"><span data-stu-id="74c79-106">Rather, the value is left negative if that is what is computed.</span></span> <span data-ttu-id="74c79-107">Il modo migliore per evitare questa situazione consiste nell'impostare le trasformazioni in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="74c79-107">The best way to avoid this situation is to set up transforms appropriately.</span></span> <span data-ttu-id="74c79-108">Un metodo meno consigliato consiste nel fare in modo che i valori di inizio e di nebbia negativi corrispondano.</span><span class="sxs-lookup"><span data-stu-id="74c79-108">A less-preferred method is to make the fog-start and fog-end values negative to match.</span></span>

<span data-ttu-id="74c79-109">Per verificare la presenza di un driver Direct3D 9, cercare un valore diverso da zero per D3DDEVCAPS2 \_ STREAMOFFSET nel membro DevCaps2 di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="74c79-109">To check for a Direct3D 9 driver, look for a nonzero value for D3DDEVCAPS2\_STREAMOFFSET in the DevCaps2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="related-topics"></a><span data-ttu-id="74c79-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="74c79-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74c79-111">Suggerimenti per la programmazione</span><span class="sxs-lookup"><span data-stu-id="74c79-111">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



