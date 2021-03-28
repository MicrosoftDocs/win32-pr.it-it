---
description: In alcuni casi, un'applicazione deve essere in grado di enumerare i tipi di carattere disponibili e selezionare quella più appropriata per una determinata operazione.
ms.assetid: 18db1b03-6e3c-4be3-b637-a21bf41cc080
title: Enumerazione dei tipi di carattere installati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dee38ccf9807371181388536f1230d222d448bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226697"
---
# <a name="enumerating-the-installed-fonts"></a>Enumerazione dei tipi di carattere installati

In alcuni casi, un'applicazione deve essere in grado di enumerare i tipi di carattere disponibili e selezionare quella più appropriata per una determinata operazione. Un'applicazione può enumerare i tipi di carattere disponibili chiamando la funzione [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) o [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) . Queste funzioni inviano informazioni sui tipi di carattere disponibili a una funzione di callback fornita dall'applicazione. La funzione di callback riceve informazioni nelle strutture [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) e [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) . La struttura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) contiene informazioni su un tipo di carattere TrueType. Quando la funzione di callback riceve informazioni su un tipo di carattere non TrueType, le informazioni sono contenute in una struttura [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) . Utilizzando queste informazioni, un'applicazione può limitare le scelte dell'utente solo ai tipi di carattere disponibili.

La funzione [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) è simile alla funzione [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) ma include alcune funzionalità aggiuntive. **EnumFontFamilies** consente a un'applicazione di sfruttare gli stili disponibili con i tipi di carattere TrueType. Le applicazioni nuove e aggiornate devono usare **EnumFontFamilies** anziché **EnumFonts**.

I tipi di carattere TrueType sono organizzati intorno a un nome di carattere tipografico (ad esempio, Courier New) e nomi di stile, ad esempio corsivo, grassetto e in grassetto. La funzione [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) enumera tutti gli stili associati a un nome di famiglia specificato, non semplicemente gli attributi grassetto e corsivo. Ad esempio, quando il sistema include un tipo di carattere TrueType denominato Courier New Extra Bold, **EnumFontFamilies** lo elenca con gli altri tipi di carattere Courier New. Le funzionalità di **EnumFontFamilies** sono utili per i tipi di carattere con stili diversi o insoliti e per i tipi di carattere che superano i confini internazionali.

Se un'applicazione non fornisce un nome di carattere tipografico, le funzioni [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) e [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) forniscono informazioni su un tipo di carattere in ogni famiglia disponibile. Per enumerare tutti i tipi di carattere in un contesto di dispositivo, l'applicazione può specificare **null** per il nome del carattere tipografico, compilare un elenco dei caratteri tipografici disponibili e quindi enumerare ogni carattere in ogni carattere tipografico.

Nell'esempio seguente viene usata la funzione [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) per recuperare il numero di famiglie di tipi di carattere raster, Vector e TrueType disponibili.


```C++
    UINT uAlignPrev; 
    int aFontCount[] = { 0, 0, 0 }; 
    char szCount[8];
        HRESULT hr;
        size_t * pcch; 
 
    EnumFontFamilies(hdc, (LPCTSTR) NULL, 
        (FONTENUMPROC) EnumFamCallBack, (LPARAM) aFontCount); 
 
    uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
 
    MoveToEx(hdc, 10, 50, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of raster fonts: ", 24); 
    itoa(aFontCount[0], szCount, 10); 
        
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 75, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of vector fonts: ", 24); 
    itoa(aFontCount[1], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 100, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of TrueType fonts: ", 26); 
    itoa(aFontCount[2], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    SetTextAlign(hdc, uAlignPrev); 
 
BOOL CALLBACK EnumFamCallBack(LPLOGFONT lplf, LPNEWTEXTMETRIC lpntm, DWORD FontType, LPVOID aFontCount) 
{ 
    int far * aiFontCount = (int far *) aFontCount; 
 
    // Record the number of raster, TrueType, and vector  
    // fonts in the font-count array.  
 
    if (FontType & RASTER_FONTTYPE) 
        aiFontCount[0]++; 
    else if (FontType & TRUETYPE_FONTTYPE) 
        aiFontCount[2]++; 
    else 
        aiFontCount[1]++; 
 
    if (aiFontCount[0] || aiFontCount[1] || aiFontCount[2]) 
        return TRUE; 
    else 
        return FALSE; 
 
    UNREFERENCED_PARAMETER( lplf ); 
    UNREFERENCED_PARAMETER( lpntm ); 
} 
```



Questo esempio usa due maschere, \_ FONTTYPE raster e \_ FONTTYPE TrueType, per determinare il tipo di carattere enumerato. Se \_ è impostato il bit FONTTYPE raster, il tipo di carattere è un tipo di carattere raster. Se \_ è impostato il bit FONTTYPE di TrueType, il tipo di carattere è un tipo di carattere TrueType. Se non è impostato alcun bit, il tipo di carattere è un tipo di carattere vettoriale. Una terza maschera, DEVICE \_ FONTTYPE, viene impostata quando un dispositivo (ad esempio, una stampante laser) supporta il download di tipi di carattere TrueType; è zero se il dispositivo è una scheda video, una stampante a matrice punto o un altro dispositivo raster. Un'applicazione può anche usare il dispositivo \_ FONTTYPE mask per distinguere i tipi di carattere raster forniti da GDI dai tipi di carattere specificati dal dispositivo. Il sistema è in grado di simulare gli attributi Bold, Italic, Underline e Strike per i tipi di carattere raster forniti da GDI, ma non per i tipi di carattere forniti dal dispositivo.

Un'applicazione può anche controllare BITS 1 e 2 nel membro **tmPitchAndFamily** della struttura [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) per identificare un tipo di carattere TrueType. Se bit 1 è 0 e bit 2 è 1, il tipo di carattere è un tipo di carattere TrueType.

I tipi di carattere vettoriali vengono categorizzati come \_ set di caratteri OEM anziché come set di caratteri ANSI \_ . Alcune applicazioni identificano i tipi di carattere vettoriali usando queste informazioni, controllando il membro **tmCharSet** della struttura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) . Questa categorizzazione in genere impedisce al mapper dei tipi di carattere di scegliere tipi di carattere vettoriali, a meno che non vengano richiesti specificamente. (La maggior parte delle applicazioni non usa più tipi di carattere vettoriali perché i tratti sono singole righe e richiedono più tempo per disegnarli rispetto ai tipi di carattere TrueType, che offrono molte delle stesse funzionalità di ridimensionamento e rotazione necessarie per i tipi di carattere vettoriali).

 

 
