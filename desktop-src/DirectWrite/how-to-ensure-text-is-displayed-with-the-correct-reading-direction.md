---
title: Verificare che il testo venga visualizzato con la direzione di lettura corretta
description: Alcuni linguaggi, come l'arabo e l'ebraico, richiedono una direzione di lettura da destra a sinistra.
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d97eee49a830986718c04b4adab7443e488093
ms.sourcegitcommit: 43b2f5209d67eae96b17c03bac2a2afab1f4d30a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730170"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a>Verificare che il testo venga visualizzato con la direzione di lettura corretta

Alcuni linguaggi, come l'arabo e l'ebraico, richiedono una direzione di lettura da destra a sinistra. Per un oggetto in formato testo [DirectWrite](direct-write-portal.md) , la direzione di lettura predefinita è da sinistra a destra. DirectWrite non deduce automaticamente la direzione di lettura dalle impostazioni locali, quindi è necessario eseguire questa operazione manualmente.

Per prima cosa, ottenere i flag di stile estesi per la finestra in cui verrà eseguito il rendering del testo utilizzando la macro GetWindowStyleEx definita in WINDOWSX. h.


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



La macro restituisce un valore DWORD costituito da diversi flag combinati con operazioni OR bit per bit. È necessario determinare se i flag specifici che influiscono sulla direzione di lettura sono presenti.

Sono presenti 2 flag diversi correlati alla direzione di lettura: WS \_ ex \_ LAYOUTRTL e WS \_ ex \_ RTLREADING.

Utilizzare l'operatore AND bit per bit (&) con la variabile dwStyle e \_ la \_ macro WS ex LAYOUTRTL per archiviare un valore bool che indica se il layout è con mirroring.


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



Eseguire la stessa operazione per il \_ flag WS es \_ RTLREADING.


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



Impostare la direzione di lettura utilizzando il metodo [**IDWriteTextFormat:: SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) . Il valore predefinito è da sinistra a destra, quindi è necessario impostare la direzione di lettura solo se è da destra a sinistra.

> [!Note]  
> WS \_ ex \_ LAYOUTRTL rispecchia l'intero layout e implica la direzione di lettura da destra a sinistra, quindi impostare la direzione di lettura solo se è presente uno di questi flag. Se entrambi sono presenti, annullano l'uno all'altro e la direzione di lettura per il formato di testo deve essere da sinistra a destra.

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
