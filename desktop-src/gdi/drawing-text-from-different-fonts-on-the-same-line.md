---
description: Stili di tipi diversi all'interno di una famiglia di caratteri possono avere larghezze diverse.
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: Disegno di testo da diversi tipi di carattere nella stessa riga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2eae2a7a332bd929b9a965462ce802734679f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226699"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a>Disegno di testo da diversi tipi di carattere nella stessa riga

Stili di tipi diversi all'interno di una famiglia di caratteri possono avere larghezze diverse. Gli stili grassetto e corsivo di una famiglia, ad esempio, sono sempre più ampi dello stile Roman per le dimensioni del punto specificato. Quando si visualizzano o stampano diversi stili di tipo su una sola riga, è necessario tenere traccia della larghezza della riga per evitare che i caratteri vengano visualizzati o stampati uno sopra l'altro.

È possibile usare due funzioni per recuperare la larghezza (o l'extent) del testo nel tipo di carattere corrente. La funzione [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) calcola la larghezza e l'altezza di una stringa di caratteri. Se la stringa contiene uno o più caratteri di tabulazione, la larghezza della stringa si basa su una matrice specificata di posizioni di interruzione di tabulazione. La funzione [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) calcola la larghezza e l'altezza di una riga di testo.

Quando necessario, il sistema sintetizza un tipo di carattere cambiando le bitmap dei caratteri. Per sintetizzare un carattere in un tipo di carattere in grassetto, il sistema disegna il carattere due volte: in corrispondenza del punto iniziale e di nuovo un pixel a destra del punto iniziale. Per sintetizzare un carattere in un tipo di carattere corsivo, il sistema disegna due righe di pixel nella parte inferiore della cella di caratteri, sposta il punto iniziale di un pixel a destra, disegna le due righe successive e continua fino a quando non viene disegnato il carattere. Spostando i pixel, ogni carattere viene tagliato a destra. La quantità di cesoia è una funzione dell'altezza del carattere.

Un modo per scrivere una riga di testo contenente più tipi di carattere consiste nell'usare la funzione [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) dopo ogni chiamata a [Text](/windows/desktop/api/Wingdi/nf-wingdi-textouta) out e aggiungere la lunghezza a una posizione corrente. Nell'esempio seguente viene scritta la riga "Questa è una stringa di esempio". utilizzando caratteri in grassetto per "This is a", passa a caratteri italici per "Sample", quindi torna ai caratteri in grassetto per "String". Una volta stampate tutte le stringhe, vengono ripristinati i caratteri predefiniti del sistema.


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



In questo esempio, la funzione [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) Inizializza i membri di una struttura di [dimensioni](/previous-versions//dd145106(v=vs.85)) con la lunghezza e l'altezza della stringa specificata. La funzione [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) recupera la sporgenza per il tipo di carattere corrente. Poiché la sporgenza è zero se il tipo di carattere è un tipo di carattere TrueType, il valore di sporgenza non modifica la posizione della stringa. Per i tipi di carattere raster, tuttavia, è importante usare il valore di sporgenza.

La sporgenza viene sottratta dalla stringa in grassetto una volta, per portare i caratteri successivi alla fine della stringa se il tipo di carattere è un tipo di carattere raster. Poiché la sporgenza interessa sia l'inizio che la fine della stringa in corsivo in un tipo di carattere raster, i glifi iniziano a destra della posizione specificata e terminano a sinistra dell'endpoint della cella dell'ultimo carattere. La funzione [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) recupera l'ambito delle celle di tipo carattere, non l'extent dei glifi. Per tenere conto della sporgenza nella stringa in corsivo raster, l'esempio sottrae la sporgenza prima di inserire la stringa e la sottrae prima di inserire i caratteri successivi.

La funzione [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) aggiunge ulteriore spazio ai caratteri break in una riga di testo. È possibile utilizzare la funzione [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) per determinare l'estensione di una stringa, quindi sottrarla dalla quantità totale di spazio che la riga deve occupare e utilizzare la funzione [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) per distribuire lo spazio aggiuntivo tra i caratteri di interruzioni della stringa. La funzione [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) aggiunge ulteriore spazio a ogni cella di caratteri nel tipo di carattere selezionato, incluso il carattere di rottura. È possibile utilizzare la funzione [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) per determinare la quantità corrente di spazio aggiuntivo aggiunto alle celle di caratteri. l'impostazione predefinita è zero.

È possibile inserire caratteri con una maggiore precisione utilizzando la funzione [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) o [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) per recuperare le larghezze dei singoli caratteri in un tipo di carattere. La funzione [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) è più precisa della funzione [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) , ma può essere utilizzata solo con i tipi di carattere TrueType.

La spaziatura ABC consente anche a un'applicazione di eseguire un allineamento del testo molto accurato. Ad esempio, quando l'applicazione Allinea a destra un tipo di carattere raster Roman senza usare la spaziatura ABC, la larghezza di avanzamento viene calcolata come larghezza del carattere. Ciò significa che gli spazi vuoti a destra del glifo nella bitmap sono allineati, non il glifo stesso. Con le larghezze ABC, le applicazioni hanno maggiore flessibilità nel posizionamento e nella rimozione di spazi vuoti durante l'allineamento del testo, perché contengono informazioni che consentono loro di controllare con precisione la spaziatura tra i caratteri.

 

 
