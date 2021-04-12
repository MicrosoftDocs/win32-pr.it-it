---
description: Elenco di alcuni dei possibili codici restituiti per i metodi e le funzioni.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4146a65e9092dcd3fed261c127e84fe8552128a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225376"
---
# <a name="s_present"></a><span data-ttu-id="0cc66-103">S \_ presente</span><span class="sxs-lookup"><span data-stu-id="0cc66-103">S\_PRESENT</span></span>

<span data-ttu-id="0cc66-104">Elenco di alcuni dei possibili codici restituiti per i metodi e le funzioni.</span><span class="sxs-lookup"><span data-stu-id="0cc66-104">A list of some of the possible return codes for methods and functions.</span></span>



|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc66-105">\#definire</span><span class="sxs-lookup"><span data-stu-id="0cc66-105">\#define</span></span>                  | <span data-ttu-id="0cc66-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cc66-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="0cc66-107">\_OK</span><span class="sxs-lookup"><span data-stu-id="0cc66-107">S\_OK</span></span>                     | <span data-ttu-id="0cc66-108">Il dispositivo è in esecuzione normalmente e può essere usato per il rendering.</span><span class="sxs-lookup"><span data-stu-id="0cc66-108">The device is running normally and can be used for rendering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="0cc66-109">S \_ presente \_ nascosto</span><span class="sxs-lookup"><span data-stu-id="0cc66-109">S\_PRESENT\_OCCLUDED</span></span>      | <span data-ttu-id="0cc66-110">L'area di presentazione è nascosto.</span><span class="sxs-lookup"><span data-stu-id="0cc66-110">The presentation area is occluded.</span></span> <span data-ttu-id="0cc66-111">L'occlusione indica che la finestra di presentazione è ridotta a icona o che un altro dispositivo è entrato in modalità schermo intero sullo stesso monitor della finestra di presentazione e la finestra di presentazione è completamente su tale monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="0cc66-111">Occlusion means that the presentation window is minimized or another device entered the fullscreen mode on the same monitor as the presentation window and the presentation window is completely on that monitor.</span></span> <span data-ttu-id="0cc66-112">L'occlusione non verrà eseguita se l'area client è coperta da un'altra finestra.</span><span class="sxs-lookup"><span data-stu-id="0cc66-112">Occlusion will not occur if the client area is covered by another Window.</span></span><br/> <span data-ttu-id="0cc66-113">Le applicazioni non riuscite possono continuare il rendering e tutte le chiamate riusciranno, ma la finestra di presentazione non verrà aggiornata.</span><span class="sxs-lookup"><span data-stu-id="0cc66-113">Occluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated.</span></span> <span data-ttu-id="0cc66-114">Preferibilmente, l'applicazione deve arrestare il rendering nella finestra di presentazione usando il dispositivo e continuando a chiamare [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) fino a quando non viene \_ modificata la modalità presente di S OK o s \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0cc66-114">Preferably the application should stop rendering to the presentation window using the device and keep calling [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) until S\_OK or S\_PRESENT\_MODE\_CHANGED returns.</span></span><br/> |
| <span data-ttu-id="0cc66-115">\_modalità presente \_ S \_ modificata</span><span class="sxs-lookup"><span data-stu-id="0cc66-115">S\_PRESENT\_MODE\_CHANGED</span></span> | <span data-ttu-id="0cc66-116">La modalità di visualizzazione del desktop è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="0cc66-116">The desktop display mode has been changed.</span></span> <span data-ttu-id="0cc66-117">L'applicazione può continuare il rendering, ma è possibile che la conversione o l'allungamento dei colori sia sufficiente.</span><span class="sxs-lookup"><span data-stu-id="0cc66-117">The application can continue rendering, but there might be color conversion/stretching.</span></span> <span data-ttu-id="0cc66-118">Selezionare un formato di buffer nascosto simile alla modalità di visualizzazione corrente e chiamare Reset per ricreare le catene di scambio.</span><span class="sxs-lookup"><span data-stu-id="0cc66-118">Pick a back buffer format similar to the current display mode, and call Reset to recreate the swap chains.</span></span> <span data-ttu-id="0cc66-119">Il dispositivo lascerà questo stato dopo la chiamata di reset.</span><span class="sxs-lookup"><span data-stu-id="0cc66-119">The device will leave this state after a Reset is called.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="0cc66-120">Altri codici di errore sono contenuti in [D3DERR](d3derr.md).</span><span class="sxs-lookup"><span data-stu-id="0cc66-120">Other error codes are contained in [D3DERR](d3derr.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cc66-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0cc66-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cc66-122">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="0cc66-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




