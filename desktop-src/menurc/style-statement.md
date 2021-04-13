---
title: Istruzione STYLE
description: Definisce lo stile della finestra della finestra di dialogo. Lo stile della finestra specifica se la casella è un popup o una finestra figlio.
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- Menu di istruzioni di stile e altre risorse
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398964"
---
# <a name="style-statement"></a><span data-ttu-id="d8fbf-105">Istruzione STYLE</span><span class="sxs-lookup"><span data-stu-id="d8fbf-105">STYLE statement</span></span>

<span data-ttu-id="d8fbf-106">Definisce lo stile della finestra della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="d8fbf-106">Defines the window style of the dialog box.</span></span> <span data-ttu-id="d8fbf-107">Lo stile della finestra specifica se la casella è un popup o una finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="d8fbf-107">The window style specifies whether the box is a pop-up or a child window.</span></span>

``` syntax
STYLE style
```

<dl> <dt>

<span data-ttu-id="d8fbf-108"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="d8fbf-108"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="d8fbf-109">Stile della finestra.</span><span class="sxs-lookup"><span data-stu-id="d8fbf-109">The window style.</span></span> <span data-ttu-id="d8fbf-110">Questo parametro può essere un valore intero o una combinazione di valori di stile della finestra, ad esempio **WS \_ Caption** e **WS \_ SYSMENU**, e i valori di stile della finestra di dialogo (ad esempio **DS \_ Center**).</span><span class="sxs-lookup"><span data-stu-id="d8fbf-110">This parameter can be an integer value or a combination of window style values (such as **WS\_CAPTION** and **WS\_SYSMENU**) and dialog box style values (such as **DS\_CENTER**).</span></span>

</dd> </dl>

<span data-ttu-id="d8fbf-111">Per un elenco degli stili della finestra, vedere [stili di finestra](/windows/desktop/winmsg/window-styles).</span><span class="sxs-lookup"><span data-stu-id="d8fbf-111">For a list of window styles, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span> <span data-ttu-id="d8fbf-112">Per un elenco degli stili della finestra di dialogo, vedere [stili di modelli](../dlgbox/about-dialog-boxes.md)di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="d8fbf-112">For a list of dialog box styles, see [Dialog Box Template Styles](../dlgbox/about-dialog-boxes.md).</span></span> <span data-ttu-id="d8fbf-113">Se si utilizzano i valori di stile della finestra o della finestra di dialogo, è necessario includere Windows. h.</span><span class="sxs-lookup"><span data-stu-id="d8fbf-113">If you use the window or dialog box style values, you must include Windows.h.</span></span>

 

 