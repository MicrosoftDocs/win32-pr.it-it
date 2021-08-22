---
description: È possibile eseguire query e impostare l'allineamento del testo per un contesto di dispositivo usando le funzioni GetTextAlign e SetTextAlign.
ms.assetid: 7fdfbadb-827a-4b42-9b9a-b9e46389e13c
title: Impostazione dell'allineamento del testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78edffa9febaee0fd624cc97c4a908da349ad65526799e1c4bd3450137b62a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468421"
---
# <a name="setting-the-text-alignment"></a>Impostazione dell'allineamento del testo

È possibile eseguire query e impostare l'allineamento del testo per un contesto di dispositivo usando le [**funzioni GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) [**e SetTextAlign.**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) Le impostazioni di allineamento del testo determinano la modalità di posizionamento del testo rispetto a una posizione specificata. Il testo può essere allineato a destra o a sinistra della posizione o centrato su di esso; può anche essere allineato sopra o sotto il punto.

L'esempio seguente illustra un metodo per determinare quale flag di allineamento orizzontale è impostato:


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



È anche possibile usare la [**funzione SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) per aggiornare la posizione corrente quando viene chiamata una funzione di output di testo. Ad esempio, l'esempio seguente usa la [**funzione SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) per aggiornare la posizione corrente quando viene chiamata la funzione [**TextOut.**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) In questo esempio il parametro *cArial* è un numero intero che specifica il numero di tipi di carattere Arial.


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
> Non usare [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) con TA UPDATECP quando si usa \_ [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), perché il rendering del testo selezionato non viene eseguito correttamente. Se è necessario usare questo flag, è possibile annullarne l'impostazione e reimpostarlo in base alle esigenze per evitare il problema.

 

 

 
