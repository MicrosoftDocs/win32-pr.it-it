---
description: È possibile eseguire una query e impostare l'allineamento del testo per un contesto di dispositivo usando le funzioni GetTextAlign e SetTextAlign.
ms.assetid: 7fdfbadb-827a-4b42-9b9a-b9e46389e13c
title: Impostazione dell'allineamento del testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538a8da060f9d854890ea004c855e2317986fd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979447"
---
# <a name="setting-the-text-alignment"></a><span data-ttu-id="3d5ae-103">Impostazione dell'allineamento del testo</span><span class="sxs-lookup"><span data-stu-id="3d5ae-103">Setting the Text Alignment</span></span>

<span data-ttu-id="3d5ae-104">È possibile eseguire una query e impostare l'allineamento del testo per un contesto di dispositivo usando le funzioni [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) e [**setTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) .</span><span class="sxs-lookup"><span data-stu-id="3d5ae-104">You can query and set the text alignment for a device context by using the [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) and [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) functions.</span></span> <span data-ttu-id="3d5ae-105">Le impostazioni di allineamento del testo determinano la modalità di posizionamento del testo rispetto a una posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="3d5ae-105">The text-alignment settings determine how text is positioned relative to a specified location.</span></span> <span data-ttu-id="3d5ae-106">Il testo può essere allineato a destra o a sinistra della posizione o centrato su di esso; può anche essere allineato al di sopra o al di sotto del punto.</span><span class="sxs-lookup"><span data-stu-id="3d5ae-106">Text can be aligned to the right or left of the position or centered over it; it can also be aligned above or below the point.</span></span>

<span data-ttu-id="3d5ae-107">Nell'esempio seguente viene illustrato un metodo per determinare quale flag di allineamento orizzontale è impostato:</span><span class="sxs-lookup"><span data-stu-id="3d5ae-107">The following example shows a method for determining which horizontal alignment flag is set:</span></span>


```C++
switch ((TA_LEFT | TA_RIGHT | TA_CENTER) & GetTextAlign(hdc)) 
{ 
    case TA_LEFT: 
       . 
       . 
       . 
    case TA_RIGHT: 
       . 
       . 
       . 
    case TA_CENTER: 
       . 
       . 
       . 
} 
```



<span data-ttu-id="3d5ae-108">È anche possibile usare la funzione [**setTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) per aggiornare la posizione corrente quando viene chiamata una funzione di output di testo.</span><span class="sxs-lookup"><span data-stu-id="3d5ae-108">You can also use the [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) function to update the current position when a text-output function is called.</span></span> <span data-ttu-id="3d5ae-109">Ad esempio, nell'esempio seguente viene usata la funzione [**setTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) per aggiornare la posizione corrente quando viene chiamata la funzione di [**testo**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) .</span><span class="sxs-lookup"><span data-stu-id="3d5ae-109">For instance, the following example uses the [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) function to update the current position when the [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) function is called.</span></span> <span data-ttu-id="3d5ae-110">In questo esempio il parametro *Carial* è un numero intero che specifica il numero di tipi di carattere Arial.</span><span class="sxs-lookup"><span data-stu-id="3d5ae-110">In this example, the *cArial* parameter is an integer that specifies the number of Arial fonts.</span></span>


```C++
UINT uAlignPrev; 
char szCount[8];
HRESULT hr;
size_t * pcch; 
 
uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
MoveToEx(hdc, 10, 50, (LPPOINT) NULL); 
TextOut(hdc, 0, 0, "Number of Arial fonts: ", 23); 
itoa(cArial, szCount, 10); 

hr = StringCchLength(szCount, 9, pcch);
if (FAILED(hr))
{
// TODO: write error handler 
}
 
TextOut(hdc, 0, 0, (LPSTR) szCount, *pcch); 
SetTextAlign(hdc, uAlignPrev); 
```



> [!Note]  
> <span data-ttu-id="3d5ae-111">Non usare [**setTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) con TA \_ UPDATECP quando si usa [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), perché il rendering del testo selezionato non è corretto.</span><span class="sxs-lookup"><span data-stu-id="3d5ae-111">You should not use [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) with TA\_UPDATECP when you are using [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), because selected text is not rendered correctly.</span></span> <span data-ttu-id="3d5ae-112">Se è necessario utilizzare questo flag, è possibile annullarlo e reimpostarlo come necessario per evitare il problema.</span><span class="sxs-lookup"><span data-stu-id="3d5ae-112">If you must use this flag, you can unset and reset it as necessary to avoid the problem.</span></span>

 

 

 
