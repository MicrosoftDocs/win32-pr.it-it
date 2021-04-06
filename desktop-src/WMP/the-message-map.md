---
title: Mappa messaggi
description: Mappa messaggi
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- Plug-in di Windows Media Player, mappa messaggi
- plug-in, mappa messaggi
- plug-in dell'interfaccia utente, mappa messaggi
- Plug-in dell'interfaccia utente, mappa messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7fc04caf752383368ab6e51ae19c82e8c3515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044824"
---
# <a name="the-message-map"></a><span data-ttu-id="c25c6-107">Mappa messaggi</span><span class="sxs-lookup"><span data-stu-id="c25c6-107">The Message Map</span></span>

<span data-ttu-id="c25c6-108">La finestra del plug-in risponde a vari eventi chiamando metodi mappati ai messaggi di evento corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="c25c6-108">The plug-in window responds to various events by calling methods that are mapped to corresponding event messages.</span></span> <span data-ttu-id="c25c6-109">La procedura guidata fornisce un mapping affinché OnPaint e OnEraseBackground vengano chiamati nei momenti appropriati.</span><span class="sxs-lookup"><span data-stu-id="c25c6-109">The wizard provides a mapping so that OnPaint and OnEraseBackground will be called at the appropriate times.</span></span> <span data-ttu-id="c25c6-110">Per creare il pulsante **Cerca** e rispondere ai clic, la sezione della mappa messaggi viene modificata come segue:</span><span class="sxs-lookup"><span data-stu-id="c25c6-110">To create the **Search** button and to respond to clicks from it, the message map section is modified as follows:</span></span>


```C++
BEGIN_MSG_MAP(CPluginWindow)
    MESSAGE_HANDLER(WM_PAINT, OnPaint)
    MESSAGE_HANDLER(WM_ERASEBKGND, OnEraseBackground)
    MESSAGE_HANDLER(WM_CREATE, OnCreate)
    COMMAND_ID_HANDLER(IDC_SEARCH, OnSearch)
END_MSG_MAP()

```



## <a name="related-topics"></a><span data-ttu-id="c25c6-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c25c6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c25c6-112">**Implementazione di CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="c25c6-112">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




