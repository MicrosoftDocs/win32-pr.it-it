---
title: Come allineare il testo
description: È possibile allineare DirectWrite testo usando il metodo SetTextAlignment dell'interfaccia IDWriteTextFormat.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a9d73443577468d794e43dc62d19e7dd24a86227ba6b5e5d8c3542cdded8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650367"
---
# <a name="how-to-align-text"></a>Come allineare il testo

È possibile [allineare DirectWrite](direct-write-portal.md) testo usando il [**metodo SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) dell'interfaccia [**IDWriteTextFormat,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) come illustrato nel codice seguente che centra il testo.


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



Il testo può essere allineato al bordo iniziale o finale della casella di layout oppure può essere centrato. La figura seguente mostra il testo con l'allineamento impostato su [**DWRITE \_ TEXT ALIGNMENT \_ \_ LEADING,**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment) [**DWRITE TEXT ALIGNMENT \_ \_ \_ CENTER**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)e [**DWRITE TEXT ALIGNMENT \_ \_ \_ TRAILING,**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)rispettivamente.

![illustrazione di paragrafi di testo con allineamento iniziale, centrato e finale](images/textalignment.png)

> [!Note]  
> L'allineamento dipende dalla direzione di lettura, il valore precedente è per la direzione di lettura da sinistra a destra. Per la direzione di lettura da destra a sinistra sarebbe l'opposto.

 

Un [**oggetto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) userà l'allineamento designato per [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fornito dall'utente durante la creazione del layout. Per modificare l'allineamento del testo, [**usare IDWriteTextLayout::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).

 

 
