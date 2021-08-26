---
title: Assicurarsi che il testo sia visualizzato con la direzione di lettura corretta
description: Alcune lingue, ad esempio arabo ed ebraico, richiedono una direzione di lettura da destra a sinistra.
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3774e4d237863a218cadf5206e4dc4921bceaeaa06c00ab81057f80dd8ee6549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982171"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a>Assicurarsi che il testo sia visualizzato con la direzione di lettura corretta

Alcune lingue, ad esempio arabo ed ebraico, richiedono una direzione di lettura da destra a sinistra. Per un [DirectWrite](direct-write-portal.md) formato testo, la direzione di lettura predefinita è da sinistra a destra. DirectWrite non deduce automaticamente la direzione di lettura dalle impostazioni locali, pertanto è necessario eseguire questa operazione manualmente.

Per prima cosa, ottenere i flag di stile estesi per la finestra in cui verrà eseguito il rendering del testo usando la macro GetWindowStyleEx definita in windowsx.h.


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



La macro restituisce un valore DWORD costituito da diversi flag combinati con operazioni OR bit per bit. È necessario determinare se sono presenti flag specifici che influiscono sulla direzione di lettura.

Esistono due flag diversi correlati alla direzione di lettura: WS \_ EX \_ LAYOUTRTL e WS \_ EX \_ RTLREADING.

Usare l'operatore AND bit per bit (&) con la variabile dwStyle e la macro WS EX LAYOUTRTL per archiviare un valore BOOL che indica se il layout è \_ \_ speculare.


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



Eseguire la stessa operazione per il flag WS \_ EX \_ RTLREADING.


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



Impostare la direzione di lettura usando il [**metodo IDWriteTextFormat::SetReadingDirection.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) Il valore predefinito è da sinistra a destra, quindi è necessario impostare la direzione di lettura solo se è da destra a sinistra.

> [!Note]  
> WS EX LAYOUTRTL rispecchia l'intero layout e implica la direzione di lettura da destra a sinistra, quindi impostare la direzione di lettura solo se è presente uno \_ \_ di questi flag. Se sono presenti entrambi, si annullano l'un l'altro e la direzione di lettura per il formato del testo deve essere da sinistra a destra.

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
