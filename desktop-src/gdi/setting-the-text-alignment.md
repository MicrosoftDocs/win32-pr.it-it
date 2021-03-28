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
# <a name="setting-the-text-alignment"></a>Impostazione dell'allineamento del testo

È possibile eseguire una query e impostare l'allineamento del testo per un contesto di dispositivo usando le funzioni [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) e [**setTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) . Le impostazioni di allineamento del testo determinano la modalità di posizionamento del testo rispetto a una posizione specificata. Il testo può essere allineato a destra o a sinistra della posizione o centrato su di esso; può anche essere allineato al di sopra o al di sotto del punto.

Nell'esempio seguente viene illustrato un metodo per determinare quale flag di allineamento orizzontale è impostato:


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



È anche possibile usare la funzione [**setTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) per aggiornare la posizione corrente quando viene chiamata una funzione di output di testo. Ad esempio, nell'esempio seguente viene usata la funzione [**setTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) per aggiornare la posizione corrente quando viene chiamata la funzione di [**testo**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) . In questo esempio il parametro *Carial* è un numero intero che specifica il numero di tipi di carattere Arial.


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
> Non usare [**setTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) con TA \_ UPDATECP quando si usa [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), perché il rendering del testo selezionato non è corretto. Se è necessario utilizzare questo flag, è possibile annullarlo e reimpostarlo come necessario per evitare il problema.

 

 

 
