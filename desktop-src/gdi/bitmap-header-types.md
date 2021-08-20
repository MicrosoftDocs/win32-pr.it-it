---
description: Tipi di intestazione bitmap
ms.assetid: 6df4655a-f707-4893-b6e6-f7e4d7f67b4e
title: Tipi di intestazione bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c88839947845cc45633cbc07b7c36aec727318c91910bfc277680b1946080531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966411"
---
# <a name="bitmap-header-types"></a>Tipi di intestazione bitmap

La bitmap ha quattro tipi di intestazione di base:

-   [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader)
-   [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))
-   [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)
-   [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)

I quattro tipi di intestazioni bitmap si differenziano in base al membro **Size,** che è il primo **DWORD** in ognuna delle strutture.

La [**struttura BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) è una struttura [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) estesa, ovvero una [**struttura BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) estesa. Tuttavia, **BITMAPINFOHEADER e** [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) hanno solo il membro **Size** in comune con altre strutture di intestazione bitmap.

I [**formati BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) e [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) sono stati sostituiti rispettivamente dai formati [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) e [**BITMAPV5HEADER.**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) I **formati BITMAPCOREHEADER e** **BITMAPV4HEADER** vengono presentati per motivi di completezza e compatibilità con le versioni precedenti.

Il formato per un DIB è il seguente (per altre informazioni, vedere [Bitmap Archiviazione](bitmap-storage.md) ):

-   struttura [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader)
-   Una struttura [**BITMAPCOREHEADER,**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) [**BITMAPINFOHEADER,**](/previous-versions//dd183376(v=vs.85)) [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)o [**BITMAPV5HEADER.**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)
-   una tabella dei colori facoltativa, ovvero un set di [**strutture RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) o un set di [**strutture RGBTRIPLE.**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple)
-   dati bitmap
-   dati del profilo facoltativi

Una tabella dei colori descrive il modo in cui i valori dei pixel corrispondono ai valori di colore RGB. RGB è un modello per descrivere i colori prodotti dall'emissione di luce.

*I dati del* profilo si riferiscono al nome del file di profilo (profilo collegato) o ai bit effettivi del profilo (profilo incorporato). Il formato di file inserisce i dati del profilo alla fine del file. I dati del profilo vengono inseriti subito dopo la tabella dei colori (se presente). Tuttavia, se la funzione riceve un DIB compresso, i dati del profilo vengono dopo i bit della bitmap, ad esempio nel formato di file .

I dati del profilo esistono solo per [**le strutture BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) in cui **bV5CSType** è PROFILE \_ LINKED o PROFILE \_ EMBEDDED. Per le funzioni che ricevono DIB compressi, i dati del profilo vengono visualizzati dopo i dati bitmap.

Un dispositivo a colori è qualsiasi dispositivo che usa le tavolozze per assegnare i colori. L'esempio classico di un dispositivo svasato è uno schermo in esecuzione con una profondità di colore a 8 bit (ovvero 256 colori). La visualizzazione in questa modalità usa una piccola tabella dei colori per assegnare colori a una bitmap. I colori in una bitmap vengono assegnati al colore più vicino nella tavolozza in uso nel dispositivo. Il dispositivo non crea una tavolozza ottimale per la visualizzazione della bitmap. usa semplicemente qualsiasi elemento presente nella tavolozza corrente. Le applicazioni sono responsabili della creazione di una tavolozza e della sua selezione nel sistema. In generale, le bitmap a 16, 24 e 32 bit per pixel (bpp) non contengono tabelle dei colori (ovvero tavolozza ottimali per la bitmap); In questo caso, l'applicazione è responsabile della generazione di una tavolozza ottimale. Tuttavia, le bitmap da 16, 24 e 32 bpp possono contenere tabelle dei colori ottimali per la visualizzazione nei dispositivi con slittamento; in questo caso l'applicazione deve solo creare una tavolozza basata sulla tabella dei colori presente nel file bitmap.

Le bitmap con dimensioni 1, 4 o 8 bpp devono avere una tabella dei colori con dimensioni massime basate su bpp. La dimensione massima per 1, 4 e 8 bitmap bpp è 2 alla potenza del bpp. Pertanto, una bitmap da 1 bpp ha un massimo di due colori, la bitmap a 4 bpp ha un massimo di 16 colori e la bitmap 8 bpp ha un massimo di 256 colori.

Le bitmap a 16, 24 o 32 bpp non richiedono tabelle dei colori, ma possono richiedere di specificare i colori per i dispositivi con slittamenti. Se è presente una tabella dei colori per una bitmap a 16, 24 o 32 bpp, il membro **biClrUsed** specifica le dimensioni della tabella dei colori e la tabella dei colori deve contenere tale numero di colori. Se **biClrUsed è** zero, non è presente alcuna tabella dei colori.

Le maschere di campo di bit rosso, verde e blu per le bitmap BI BITFIELD seguono immediatamente le strutture \_ [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)e [**BITMAPV5HEADER.**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) Le **strutture BITMAPV4HEADER** e **BITMAPV5HEADER** contengono membri aggiuntivi per le maschere rosse, verdi e blu, come indicato di seguito.



| Membro        | Significato                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| **Maschera rossa**   | Maschera di colore che specifica il componente rosso di ogni pixel, valida solo se il membro **Compression** è impostato su BI \_ BITFIELDS.   |
| **Maschera verde** | Maschera colore che specifica il componente verde di ogni pixel, valida solo se il membro **Compression** è impostato su BI \_ BITFIELDS. |
| **Maschera blu**  | Maschera colore che specifica il componente blu di ogni pixel, valida solo se il membro **Compression** è impostato su BI \_ BITFIELDS.  |



 

Quando il membro **biCompression** di [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) è impostato su BI BITFIELDS e la funzione riceve un argomento di tipo \_ **LPBITMAPINFO,** le maschere di colore seguiranno immediatamente l'intestazione. La tabella dei colori, se presente, seguirà le maschere di colore. [**Le bitmap BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) non supportano le maschere di colore.

Per impostazione predefinita, i dati bitmap sono in formato bottom-up. Bottom-up significa che la prima riga di analisi nei dati bitmap è l'ultima riga di analisi da visualizzare. Ad esempio, lo<sup>0°</sup> pixel della linea di analisi<sup>0</sup> dei dati bitmap di una bitmap di 10 pixel per 10 pixel sarà il<sup>0°</sup> pixel della nona riga di analisi dell'immagine visualizzata o stampata.<sup></sup> Le bitmap in formato RLE (Run-Length Encoded) e [**bitmap BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) non possono essere bitmap dall'alto verso il basso. Le righe di analisi sono **allineate con DWORD,** ad eccezione delle bitmap compresse con RLE. Devono essere riempiti per le larghezze delle righe di analisi, in byte, che non sono divisibile in modo uniforme per quattro, ad eccezione delle bitmap compresse RLE. Ad esempio, una bitmap da 24 bpp da 10x10 pixel avrà due byte di riempimento alla fine di ogni riga di analisi.

 

 
