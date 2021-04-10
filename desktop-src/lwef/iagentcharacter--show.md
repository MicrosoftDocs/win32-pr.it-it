---
title: IAgentCharacter Show
description: IAgentCharacter Show
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997a9879d564644085bd92e4515460c3dde33208
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046747"
---
# <a name="iagentcharactershow"></a><span data-ttu-id="471eb-103">IAgentCharacter:: Show</span><span class="sxs-lookup"><span data-stu-id="471eb-103">IAgentCharacter::Show</span></span>

<span data-ttu-id="471eb-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="471eb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="471eb-105">Visualizza un carattere.</span><span class="sxs-lookup"><span data-stu-id="471eb-105">Displays a character.</span></span>

-   <span data-ttu-id="471eb-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="471eb-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="471eb-107">Quando la funzione restituisce, *pdwReqID* contiene l'ID della richiesta.</span><span class="sxs-lookup"><span data-stu-id="471eb-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="471eb-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span><span class="sxs-lookup"><span data-stu-id="471eb-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="471eb-109">Visualizzazione del flag di animazione stato.</span><span class="sxs-lookup"><span data-stu-id="471eb-109">Showing state animation flag.</span></span> <span data-ttu-id="471eb-110">Se questo parametro è **true**, l'animazione di stato che **Visualizza** viene riprodotta dopo aver reso visibile il carattere; Se **false**, l'animazione non viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="471eb-110">If this parameter is **True**, the **Showing** state animation plays after making the character visible; if **False**, the animation does not play.</span></span>

</dd> <dt>

<span data-ttu-id="471eb-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="471eb-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="471eb-112">Indirizzo di una variabile che riceve l'ID della richiesta di [**visualizzazione**](/windows/desktop/lwef/iagentcharacter--show) .</span><span class="sxs-lookup"><span data-stu-id="471eb-112">Address of a variable that receives the [**Show**](/windows/desktop/lwef/iagentcharacter--show) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="471eb-113">Evitare di impostare il parametro *bFast* su **true** senza prima riprodurre un'animazione. in caso contrario, è possibile che venga visualizzato il frame di caratteri, ma che non sia presente alcuna immagine da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="471eb-113">Avoid setting the *bFast* parameter to **True** without playing an animation beforehand, otherwise, the character frame may be displayed, but have no image to display.</span></span> <span data-ttu-id="471eb-114">In particolare, si noti che se si chiama [**MoveTo**](iagentcharacter--moveto.md) quando il carattere non è visibile, non viene eseguita alcuna animazione.</span><span class="sxs-lookup"><span data-stu-id="471eb-114">In particular, note that if you call [**MoveTo**](iagentcharacter--moveto.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="471eb-115">Se pertanto si chiama il metodo **show** con *Bfast* impostato su **true**, non verrà visualizzata alcuna immagine.</span><span class="sxs-lookup"><span data-stu-id="471eb-115">Therefore, if you call the **Show** method with *bFast* set to **True**, no image will be displayed.</span></span> <span data-ttu-id="471eb-116">In modo analogo, se si chiama [**Nascondi**](/windows/desktop/lwef/iagentcharacter--hide), quindi **Mostra** con *bFast* impostato su **true**, non sarà presente alcuna immagine visibile.</span><span class="sxs-lookup"><span data-stu-id="471eb-116">Similarly, if you call [**Hide**](/windows/desktop/lwef/iagentcharacter--hide), then **Show** with *bFast* set to **True**, there will be no visible image.</span></span>

<span data-ttu-id="471eb-117">Quando si utilizza il protocollo HTTP per accedere ai dati di tipo carattere e animazione, utilizzare il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per garantire la disponibilità dell'animazione **di visualizzazione dello stato prima** di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="471eb-117">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Showing** state animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="471eb-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="471eb-118">See Also</span></span>

[<span data-ttu-id="471eb-119">**IAgentCharacter:: Hide**</span><span class="sxs-lookup"><span data-stu-id="471eb-119">**IAgentCharacter::Hide**</span></span>](iagentcharacter--hide.md)


 

 