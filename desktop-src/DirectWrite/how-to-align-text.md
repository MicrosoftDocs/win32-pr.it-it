---
title: Come allineare il testo
description: È possibile allineare il testo DirectWrite usando il Metodo SetTextAlignment dell'interfaccia IDWriteTextFormat.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb765860f2fbaac94409aa9ec20c2269beb45cbb
ms.sourcegitcommit: 3b9424e1dcd951b2a73e47de3c7f4d734de4263b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "106334309"
---
# <a name="how-to-align-text"></a><span data-ttu-id="fe9db-103">Come allineare il testo</span><span class="sxs-lookup"><span data-stu-id="fe9db-103">How to Align Text</span></span>

<span data-ttu-id="fe9db-104">È possibile allineare il testo [DirectWrite](direct-write-portal.md) usando il metodo [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) dell'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , come illustrato nel codice seguente che centra il testo.</span><span class="sxs-lookup"><span data-stu-id="fe9db-104">You can align [DirectWrite](direct-write-portal.md) text by using the [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) method of the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface, as shown in the following code that centers the text.</span></span>


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



<span data-ttu-id="fe9db-105">Il testo può essere allineato al bordo principale o finale della casella di layout oppure può essere centrato.</span><span class="sxs-lookup"><span data-stu-id="fe9db-105">The text can be aligned to the leading or trailing edge of the layout box, or it can be centered.</span></span> <span data-ttu-id="fe9db-106">Nella figura seguente viene illustrato il testo con l'allineamento impostato su [**DWrite \_ Text \_ Alignment \_ Leading**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWrite \_ Text \_ Alignment \_ Center**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)e [**DWrite \_ Text \_ Alignment \_ trailing**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="fe9db-106">The following illustration shows text with the alignment set to [**DWRITE\_TEXT\_ALIGNMENT\_LEADING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWRITE\_TEXT\_ALIGNMENT\_CENTER**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), and [**DWRITE\_TEXT\_ALIGNMENT\_TRAILING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectively.</span></span>

![illustrazione di paragrafi di testo con allineamento di primo livello, centrato e finale](images/textalignment.png)

> [!Note]  
> <span data-ttu-id="fe9db-108">L'allineamento dipende dalla direzione di lettura, mentre quello precedente è per la direzione di lettura da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="fe9db-108">The alignment is dependent on reading direction, the above is for left-to-right reading direction.</span></span> <span data-ttu-id="fe9db-109">Per la direzione di lettura da destra a sinistra, sarebbe l'opposto.</span><span class="sxs-lookup"><span data-stu-id="fe9db-109">For right-to-left reading direction it would be the opposite.</span></span>

 

<span data-ttu-id="fe9db-110">Un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) utilizzerà l'allineamento che è stato designato per il [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fornito dall'utente durante la creazione del layout.</span><span class="sxs-lookup"><span data-stu-id="fe9db-110">An [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object will use the alignment that has been designated for the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provided by you when creating the layout.</span></span> <span data-ttu-id="fe9db-111">Per modificare l'allineamento del testo, utilizzare [**IDWriteTextLayout:: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).</span><span class="sxs-lookup"><span data-stu-id="fe9db-111">To change the text alignment, use [**IDWriteTextLayout::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).</span></span>

 

 
