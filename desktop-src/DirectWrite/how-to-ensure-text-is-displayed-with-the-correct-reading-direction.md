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
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a><span data-ttu-id="fc20c-103">Verificare che il testo venga visualizzato con la direzione di lettura corretta</span><span class="sxs-lookup"><span data-stu-id="fc20c-103">Ensure text is displayed with the correct reading direction</span></span>

<span data-ttu-id="fc20c-104">Alcuni linguaggi, come l'arabo e l'ebraico, richiedono una direzione di lettura da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="fc20c-104">Some languages, such as Arabic and Hebrew, require a right-to-left reading direction.</span></span> <span data-ttu-id="fc20c-105">Per un oggetto in formato testo [DirectWrite](direct-write-portal.md) , la direzione di lettura predefinita è da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="fc20c-105">For a [DirectWrite](direct-write-portal.md) text format object, the default reading direction is left-to-right.</span></span> <span data-ttu-id="fc20c-106">DirectWrite non deduce automaticamente la direzione di lettura dalle impostazioni locali, quindi è necessario eseguire questa operazione manualmente.</span><span class="sxs-lookup"><span data-stu-id="fc20c-106">DirectWrite does not automatically infer the reading direction from the locale, so you must do this yourself.</span></span>

<span data-ttu-id="fc20c-107">Per prima cosa, ottenere i flag di stile estesi per la finestra in cui verrà eseguito il rendering del testo utilizzando la macro GetWindowStyleEx definita in WINDOWSX. h.</span><span class="sxs-lookup"><span data-stu-id="fc20c-107">First, get the extended style flags for the window that the text will be rendered to by using the GetWindowStyleEx macro defined in windowsx.h.</span></span>


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



<span data-ttu-id="fc20c-108">La macro restituisce un valore DWORD costituito da diversi flag combinati con operazioni OR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="fc20c-108">The macro returns a DWORD value made up of several flags combined with bitwise OR operations.</span></span> <span data-ttu-id="fc20c-109">È necessario determinare se i flag specifici che influiscono sulla direzione di lettura sono presenti.</span><span class="sxs-lookup"><span data-stu-id="fc20c-109">You must determine if the specific flags affecting reading direction are there.</span></span>

<span data-ttu-id="fc20c-110">Sono presenti 2 flag diversi correlati alla direzione di lettura: WS \_ ex \_ LAYOUTRTL e WS \_ ex \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="fc20c-110">There are 2 different flags that are related to the reading direction: WS\_EX\_LAYOUTRTL and WS\_EX\_RTLREADING.</span></span>

<span data-ttu-id="fc20c-111">Utilizzare l'operatore AND bit per bit (&) con la variabile dwStyle e \_ la \_ macro WS ex LAYOUTRTL per archiviare un valore bool che indica se il layout è con mirroring.</span><span class="sxs-lookup"><span data-stu-id="fc20c-111">Use the bitwise AND operator (&) with the dwStyle variable and the WS\_EX\_LAYOUTRTL macro to store a BOOL value that indicates if the layout is mirrored.</span></span>


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



<span data-ttu-id="fc20c-112">Eseguire la stessa operazione per il \_ flag WS es \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="fc20c-112">Do the same thing for the WS\_EX\_RTLREADING flag.</span></span>


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



<span data-ttu-id="fc20c-113">Impostare la direzione di lettura utilizzando il metodo [**IDWriteTextFormat:: SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) .</span><span class="sxs-lookup"><span data-stu-id="fc20c-113">Set the reading direction by using the [**IDWriteTextFormat::SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) method.</span></span> <span data-ttu-id="fc20c-114">Il valore predefinito è da sinistra a destra, quindi è necessario impostare la direzione di lettura solo se è da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="fc20c-114">The default is left-to-right, so you only need to set the reading direction if it is right-to-left.</span></span>

> [!Note]  
> <span data-ttu-id="fc20c-115">WS \_ ex \_ LAYOUTRTL rispecchia l'intero layout e implica la direzione di lettura da destra a sinistra, quindi impostare la direzione di lettura solo se è presente uno di questi flag.</span><span class="sxs-lookup"><span data-stu-id="fc20c-115">WS\_EX\_LAYOUTRTL mirrors the whole layout and implies right-to-left reading direction, so set the reading direction only if one of these flags is present.</span></span> <span data-ttu-id="fc20c-116">Se entrambi sono presenti, annullano l'uno all'altro e la direzione di lettura per il formato di testo deve essere da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="fc20c-116">If both are present, they cancel one another out and the reading direction for the text format should be left-to-right.</span></span>

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
