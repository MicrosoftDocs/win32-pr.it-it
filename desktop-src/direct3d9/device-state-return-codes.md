---
description: Elenco di alcuni dei possibili codici restituiti per metodi e funzioni.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cd860fcc8268bf2b63a9498b9960da359ca210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999338"
---
# <a name="s_present"></a><span data-ttu-id="7b873-103">S \_ PRESENT</span><span class="sxs-lookup"><span data-stu-id="7b873-103">S\_PRESENT</span></span>

<span data-ttu-id="7b873-104">Elenco di alcuni dei possibili codici restituiti per metodi e funzioni.</span><span class="sxs-lookup"><span data-stu-id="7b873-104">A list of some of the possible return codes for methods and functions.</span></span>



| <span data-ttu-id="7b873-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="7b873-105">\#define</span></span>                  | <span data-ttu-id="7b873-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b873-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b873-107">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="7b873-107">S\_OK</span></span>                     | <span data-ttu-id="7b873-108">Il dispositivo viene eseguito normalmente e può essere usato per il rendering.</span><span class="sxs-lookup"><span data-stu-id="7b873-108">The device is running normally and can be used for rendering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7b873-109">S \_ PRESENTE \_ OCCLUDED</span><span class="sxs-lookup"><span data-stu-id="7b873-109">S\_PRESENT\_OCCLUDED</span></span>      | <span data-ttu-id="7b873-110">L'area della presentazione è occlusa.</span><span class="sxs-lookup"><span data-stu-id="7b873-110">The presentation area is occluded.</span></span> <span data-ttu-id="7b873-111">Occlusione significa che la finestra di presentazione è ridotta a icona o che un altro dispositivo è entrato nella modalità schermo intero sullo stesso monitor della finestra di presentazione e la finestra di presentazione è completamente su tale monitor.</span><span class="sxs-lookup"><span data-stu-id="7b873-111">Occlusion means that the presentation window is minimized or another device entered the fullscreen mode on the same monitor as the presentation window and the presentation window is completely on that monitor.</span></span> <span data-ttu-id="7b873-112">L'occlusione non si verifica se l'area client è coperta da un'altra finestra.</span><span class="sxs-lookup"><span data-stu-id="7b873-112">Occlusion will not occur if the client area is covered by another Window.</span></span><br/> <span data-ttu-id="7b873-113">Le applicazioni occluded possono continuare il rendering e tutte le chiamate avranno esito positivo, ma la finestra di presentazione occlusa non verrà aggiornata.</span><span class="sxs-lookup"><span data-stu-id="7b873-113">Occluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated.</span></span> <span data-ttu-id="7b873-114">Preferibilmente, l'applicazione deve interrompere il rendering nella finestra di presentazione usando il dispositivo e continuare a chiamare [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) fino a quando non viene restituito S OK o \_ S PRESENT MODE \_ \_ \_ CHANGED.</span><span class="sxs-lookup"><span data-stu-id="7b873-114">Preferably the application should stop rendering to the presentation window using the device and keep calling [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) until S\_OK or S\_PRESENT\_MODE\_CHANGED returns.</span></span><br/> |
| <span data-ttu-id="7b873-115">MODALITÀ S \_ \_ PRESENT \_ MODIFICATA</span><span class="sxs-lookup"><span data-stu-id="7b873-115">S\_PRESENT\_MODE\_CHANGED</span></span> | <span data-ttu-id="7b873-116">La modalità di visualizzazione del desktop è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="7b873-116">The desktop display mode has been changed.</span></span> <span data-ttu-id="7b873-117">L'applicazione può continuare il rendering, ma potrebbe esserci una conversione/estensione del colore.</span><span class="sxs-lookup"><span data-stu-id="7b873-117">The application can continue rendering, but there might be color conversion/stretching.</span></span> <span data-ttu-id="7b873-118">Selezionare un formato di buffer nascosto simile alla modalità di visualizzazione corrente e chiamare Reset per ricreare le catene di scambio.</span><span class="sxs-lookup"><span data-stu-id="7b873-118">Pick a back buffer format similar to the current display mode, and call Reset to recreate the swap chains.</span></span> <span data-ttu-id="7b873-119">Il dispositivo lascia questo stato dopo la chiamata a Reset.</span><span class="sxs-lookup"><span data-stu-id="7b873-119">The device will leave this state after a Reset is called.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="7b873-120">Altri codici di errore sono contenuti in [D3DERR](d3derr.md).</span><span class="sxs-lookup"><span data-stu-id="7b873-120">Other error codes are contained in [D3DERR](d3derr.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b873-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b873-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b873-122">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="7b873-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




