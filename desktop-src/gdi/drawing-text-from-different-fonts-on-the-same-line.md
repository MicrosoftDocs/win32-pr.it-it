---
description: Stili di tipo diversi all'interno di una famiglia di caratteri possono avere larghezze diverse.
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: Disegno di testo da tipi di carattere diversi sulla stessa riga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad28f13c94e568073504f07e8722e5d688cb12aa1b376b0f52fad752574e6f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038049"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a>Disegno di testo da tipi di carattere diversi sulla stessa riga

Stili di tipo diversi all'interno di una famiglia di caratteri possono avere larghezze diverse. Ad esempio, gli stili grassetto e corsivo di una famiglia sono sempre più larghi dello stile romano per una dimensione in punti specificata. Quando si visualizzano o si stampano diversi stili di tipo su una singola riga, è necessario tenere traccia della larghezza della riga per evitare che i caratteri vengono visualizzati o stampati uno sopra l'altro.

È possibile usare due funzioni per recuperare la larghezza (o l'extent) del testo nel tipo di carattere corrente. La [funzione GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) calcola la larghezza e l'altezza di una stringa di caratteri. Se la stringa contiene uno o più caratteri di tabulazione, la larghezza della stringa è basata su una matrice specificata di posizioni di tabulazione. La [funzione GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) calcola la larghezza e l'altezza di una riga di testo.

Quando necessario, il sistema sintetizza un tipo di carattere modificando le bitmap dei caratteri. Per sintetizzare un carattere in grassetto, il sistema disegna il carattere due volte: nel punto iniziale e di nuovo un pixel a destra del punto iniziale. Per sintetizzare un carattere in corsivo, il sistema disegna due righe di pixel nella parte inferiore della cella del carattere, sposta il punto iniziale di un pixel a destra, disegna le due righe successive e continua fino a quando il carattere non viene disegnato. Spostando i pixel, ogni carattere sembra essere spostato a destra. La quantità di setra è una funzione dell'altezza del carattere.

Un modo per scrivere una riga di testo che contiene più tipi di carattere è usare la funzione [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) dopo ogni chiamata a [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) e aggiungere la lunghezza a una posizione corrente. L'esempio seguente scrive la riga "This is a sample string". usando i caratteri in grassetto per "This is a", passa al corsivo per "sample", quindi torna ai caratteri in grassetto per "string". Dopo la stampa di tutte le stringhe, vengono ripristinati i caratteri predefiniti del sistema.


```C++
int XIncrement; 
int YStart; 
TEXTMETRIC tm; 
HFONT hfntDefault, hfntItalic, hfntBold; 
SIZE sz; 
LPSTR lpszString1 = "This is a "; 
LPSTR lpszString2 = "sample "; 
LPSTR lpszString3 = "string."; 
HRESULT hr;
size_t * pcch;
 
// Create a bold and an italic logical font.  
 
hfntItalic = MyCreateFont(); 
hfntBold = MyCreateFont(); 
 
 
// Select the bold font and draw the first string  
// beginning at the specified point (XIncrement, YStart).  
 
XIncrement = 10; 
YStart = 50; 
hfntDefault = SelectObject(hdc, hfntBold); 
hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
TextOut(hdc, XIncrement, YStart, lpszString1, *pcch); 
 
// Compute the length of the first string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
GetTextExtentPoint32(hdc, lpszString1, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Retrieve the overhang value from the TEXTMETRIC  
// structure and subtract it from the x-increment.  
// (This is only necessary for non-TrueType raster  
// fonts.)  
 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang; 
 
// Select an italic font and draw the second string  
// beginning at the point (XIncrement, YStart).  
 
hfntBold = SelectObject(hdc, hfntItalic); 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang;
hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
TextOut(hdc, XIncrement, YStart, lpszString2, *pcch); 
 
// Compute the length of the second string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
GetTextExtentPoint32(hdc, lpszString2, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Reselect the bold font and draw the third string  
// beginning at the point (XIncrement, YStart).  
 
SelectObject(hdc, hfntBold);
hr = StringCchLength(lpszString3, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
TextOut(hdc, XIncrement - tm.tmOverhang, YStart, lpszString3, 
            *pcch); 
 
// Reselect the original font.  
 
SelectObject(hdc, hfntDefault); 
 
// Delete the bold and italic fonts.  
 
DeleteObject(hfntItalic); 
DeleteObject(hfntBold); 
```



In questo esempio la [funzione GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) inizializza i membri di una struttura [SIZE](/previous-versions//dd145106(v=vs.85)) con la lunghezza e l'altezza della stringa specificata. La [funzione GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) recupera l'overhang per il tipo di carattere corrente. Poiché l'overhang è zero se il tipo di carattere è un tipo di carattere TrueType, il valore overhang non modifica la posizione della stringa. Per i tipi di carattere raster, tuttavia, è importante usare il valore overhang.

L'overhang viene sottratto una volta dalla stringa in grassetto per avvicinare i caratteri successivi alla fine della stringa se il tipo di carattere è raster. Poiché l'overhang influisce sia sull'inizio che sulla fine della stringa in corsivo in un tipo di carattere raster, i glifi iniziano a destra della posizione specificata e terminano a sinistra dell'endpoint dell'ultima cella di caratteri. La [**funzione GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) recupera l'estensione delle celle di caratteri, non l'estensione dei glifi. Per fare in modo che l'overhang sia presente nella stringa raster italic, l'esempio sottrae l'overhang prima di posizionare la stringa e la sottrae di nuovo prima di inserire i caratteri successivi.

La [funzione SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) aggiunge spazio aggiuntivo ai caratteri di interruzione in una riga di testo. È possibile usare la funzione [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) per determinare l'estensione di una stringa, quindi sottrarre tale estensione dalla quantità totale di spazio che la riga deve occupare e usare la funzione [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) per distribuire lo spazio aggiuntivo tra i caratteri di interruzione nella stringa. La [funzione SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) aggiunge spazio aggiuntivo a ogni cella di caratteri nel tipo di carattere selezionato, incluso il carattere di interruzione. È possibile usare la [funzione GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) per determinare la quantità corrente di spazio aggiuntivo da aggiungere alle celle di caratteri. L'impostazione predefinita è zero.

È possibile inserire caratteri con maggiore precisione usando la [funzione GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) o [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) per recuperare la larghezza dei singoli caratteri in un tipo di carattere. La [**funzione GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) è più accurata rispetto alla funzione [**GetCharWidth32,**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) ma può essere usata solo con i tipi di carattere TrueType.

La spaziatura ABC consente inoltre a un'applicazione di eseguire un allineamento del testo molto accurato. Ad esempio, quando l'applicazione allinea a destra un tipo di carattere raster roman senza usare la spaziatura ABC, la larghezza di avanzamento viene calcolata come larghezza del carattere. Ciò significa che lo spazio vuoto a destra del glifo nella bitmap è allineato, non il glifo stesso. Usando le larghezze ABC, le applicazioni offrono maggiore flessibilità nel posizionamento e nella rimozione degli spazi vuoti durante l'allineamento del testo, perché dispongono di informazioni che consentono di controllare in modo fine la spaziatura tra caratteri.

 

 
