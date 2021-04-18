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
# <a name="how-to-align-text"></a>Come allineare il testo

È possibile allineare il testo [DirectWrite](direct-write-portal.md) usando il metodo [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) dell'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , come illustrato nel codice seguente che centra il testo.


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



Il testo può essere allineato al bordo principale o finale della casella di layout oppure può essere centrato. Nella figura seguente viene illustrato il testo con l'allineamento impostato su [**DWrite \_ Text \_ Alignment \_ Leading**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWrite \_ Text \_ Alignment \_ Center**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)e [**DWrite \_ Text \_ Alignment \_ trailing**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), rispettivamente.

![illustrazione di paragrafi di testo con allineamento di primo livello, centrato e finale](images/textalignment.png)

> [!Note]  
> L'allineamento dipende dalla direzione di lettura, mentre quello precedente è per la direzione di lettura da sinistra a destra. Per la direzione di lettura da destra a sinistra, sarebbe l'opposto.

 

Un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) utilizzerà l'allineamento che è stato designato per il [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fornito dall'utente durante la creazione del layout. Per modificare l'allineamento del testo, utilizzare [**IDWriteTextLayout:: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).

 

 
