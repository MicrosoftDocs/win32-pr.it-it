---
title: Informazioni sull'oggetto PlayerApplication
description: Informazioni sull'oggetto PlayerApplication
ms.assetid: 4b77bf16-d7e1-4119-91c2-46136db13e81
keywords:
- Windows Media Player, oggetto PlayerApplication
- Modello a oggetti di Windows Media Player, oggetto PlayerApplication
- modello a oggetti, oggetto PlayerApplication
- Controllo ActiveX Windows Media Player, oggetto PlayerApplication
- Controllo ActiveX, oggetto PlayerApplication
- Controllo ActiveX Windows Media Player Mobile, oggetto PlayerApplication
- Windows Media Player Mobile, oggetto PlayerApplication
- Oggetto PlayerApplication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d197614ba75a51bdc8ec5398ca757e410f918a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856597"
---
# <a name="about-the-playerapplication-object"></a><span data-ttu-id="359d6-111">Informazioni sull'oggetto PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="359d6-111">About the PlayerApplication Object</span></span>

<span data-ttu-id="359d6-112">L'oggetto **PlayerApplication** viene usato per la comunicazione remota di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="359d6-112">The **PlayerApplication** object is used for remoting Windows Media Player.</span></span> <span data-ttu-id="359d6-113">Fornisce la funzionalità necessaria per passare da un controllo Media Player remoto di Windows alla modalità completa del lettore.</span><span class="sxs-lookup"><span data-stu-id="359d6-113">It provides the functionality required to switch between a remoted Windows Media Player control and the full mode of the Player.</span></span>

<span data-ttu-id="359d6-114">La comunicazione remota consente a un controllo Media Player Windows incorporato in un'applicazione C++ di utilizzare lo stesso motore di riproduzione del lettore.</span><span class="sxs-lookup"><span data-stu-id="359d6-114">Remoting enables a Windows Media Player control embedded in a C++ application to use the same playback engine as the Player.</span></span> <span data-ttu-id="359d6-115">Ciò significa che in genere si userà l'oggetto **PlayerApplication** nel codice C++ usando le interfacce com.</span><span class="sxs-lookup"><span data-stu-id="359d6-115">This means that usually you will use the **PlayerApplication** object in C++ code using the COM interfaces.</span></span> <span data-ttu-id="359d6-116">Esiste tuttavia un caso particolare in cui è possibile incorporare il controllo Media Player di Windows che visualizza un'interfaccia di Media Player Windows come interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="359d6-116">There is a special case, however, where you can embed the Windows Media Player control that displays a Windows Media Player skin as its user interface.</span></span> <span data-ttu-id="359d6-117">In questo caso, **PlayerApplication** può essere programmato usando JScript nel codice di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="359d6-117">In this case, **PlayerApplication** can be programmed using JScript in the skin code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="359d6-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="359d6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="359d6-119">**Modello a oggetti del lettore per i linguaggi di scripting**</span><span class="sxs-lookup"><span data-stu-id="359d6-119">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="359d6-120">**Oggetto PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="359d6-120">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> </dl>

 

 




