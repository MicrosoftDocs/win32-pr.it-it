---
description: Tipi di intestazione bitmap
ms.assetid: 6df4655a-f707-4893-b6e6-f7e4d7f67b4e
title: Tipi di intestazione bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5910b0fb5be1166e807db1f3362186a206abc2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880333"
---
# <a name="bitmap-header-types"></a>Tipi di intestazione bitmap

La bitmap ha quattro tipi di intestazione di base:

-   [**STRUTTURA BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader)
-   [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))
-   [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)
-   [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)

I quattro tipi di intestazioni bitmap sono distinti dal membro **size** , che è il primo **DWORD** in ogni struttura.

La struttura [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) è una struttura [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) estesa, ovvero una struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) estesa. Tuttavia, **BITMAPINFOHEADER** e [**struttura BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) hanno solo il membro **size** in comune con altre strutture di intestazione bitmap.

I formati [**struttura BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) e [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) sono stati sostituiti rispettivamente dai formati [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) e [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) . I formati **struttura BITMAPCOREHEADER** e **BITMAPV4HEADER** vengono presentati per completezza e compatibilità con le versioni precedenti.

Il formato di una DIB è il seguente (per altre informazioni, vedere [bitmap storage](bitmap-storage.md) ):

-   struttura [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader)
-   [**struttura BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader), [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)o una struttura [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .
-   tabella dei colori facoltativa, ovvero un set di strutture [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) o un set di strutture [**RGBTRIPLE**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple) .
-   dati bitmap
-   dati di profilo facoltativi

Una tabella colori descrive il modo in cui i valori dei pixel corrispondono ai valori dei colori RGB. RGB è un modello per la descrizione dei colori prodotti dalla creazione di una luce.

I *dati del profilo* fanno riferimento al nome del file di profilo (profilo collegato) o ai bit di profilo effettivi (profilo incorporato). Il formato del file inserisce i dati del profilo alla fine del file. I dati del profilo vengono posizionati subito dopo la tabella dei colori (se presente). Tuttavia, se la funzione riceve una DIB compressa, i dati del profilo vengono inseriti dopo i bit bitmap, ad esempio nel formato del file.

I dati del profilo sono disponibili solo per le strutture [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) in cui **bV5CSType** è collegato al profilo \_ o incorporato nel profilo \_ . Per le funzioni che ricevono la precedenza compressa, i dati del profilo vengono restituiti dopo i dati bitmap.

Un dispositivo pallettizzati è un dispositivo che usa tavolozze per assegnare colori. L'esempio classico di un dispositivo pallettizzati è una visualizzazione in esecuzione in profondità di colore a 8 bit, ovvero 256 colori. La visualizzazione in questa modalità usa una tabella dei colori di piccole dimensioni per assegnare colori a una bitmap. I colori in una bitmap vengono assegnati al colore più vicino nella tavolozza usata dal dispositivo. Il dispositivo pallettizzati non crea una tavolozza ottimale per la visualizzazione della bitmap; Usa semplicemente tutti gli strumenti presenti nella tavolozza corrente. Le applicazioni sono responsabili della creazione di una tavolozza e della relativa selezione nel sistema. In generale, le bitmap a 16, 24 e 32 bit per pixel (BPP) non contengono tabelle colori (noto anche come tavolozze ottimali per la bitmap); in questo caso, l'applicazione è responsabile della generazione di una tavolozza ottimale. Tuttavia, le bitmap a 16, 24 e 32-BPP possono contenere tabelle dei colori ottimali per la visualizzazione su dispositivi pallettizzati. in questo caso l'applicazione deve solo creare una tavolozza basata sulla tabella dei colori presente nel file bitmap.

Le bitmap che sono da 1 a 4 o 8 BPP devono avere una tabella dei colori con una dimensione massima basata sul BPP. La dimensione massima per le bitmap da 1, 4 e 8 BPP è 2 alla potenza del BPP. Una bitmap da 1 BPP, quindi, ha un massimo di due colori, la bitmap di 4 BPP è costituita da un massimo di 16 colori e la bitmap da 8 BPP ha un massimo di 256 colori.

Le bitmap che sono 16, 24 o 32-BPP non richiedono tabelle dei colori, ma possono avere per specificare i colori per i dispositivi pallettizzati. Se è presente una tabella dei colori per la bitmap a 16, 24 o 32-BPP, il membro **biClrUsed** specifica le dimensioni della tabella dei colori e la tabella dei colori deve contenere molti colori. Se **biClrUsed** è zero, non è presente alcuna tabella colori.

Le maschere bit rosse, verdi e blu per le \_ bitmap bit di BI seguono immediatamente le strutture [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)e [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) . Le strutture **BITMAPV4HEADER** e **BITMAPV5HEADER** contengono membri aggiuntivi per le maschere rosse, verdi e blu, come indicato di seguito.



| Membro        | Significato                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| **RedMask**   | Maschera di colore che specifica il componente rosso di ogni pixel, valido solo se il membro di **compressione** è impostato su bi \_ campi.   |
| **GreenMask** | Maschera di colore che specifica il componente verde di ogni pixel, valido solo se il membro di **compressione** è impostato su bi \_ campi. |
| **BlueMask**  | Maschera di colore che specifica il componente blu di ogni pixel, valido solo se il membro di **compressione** è impostato su bi \_ campi.  |



 

Quando il membro della **bicompressione** di [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) è impostato su bi \_ campi e la funzione riceve un argomento di tipo **LPBITMAPINFO**, le maschere dei colori seguiranno immediatamente l'intestazione. La tabella dei colori, se presente, seguirà le maschere dei colori. Le bitmap [**struttura BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) non supportano le maschere colori.

Per impostazione predefinita, i dati bitmap sono al di sotto del formato. Il bottom-up indica che la prima riga di analisi nei dati bitmap è l'ultima riga da visualizzare. Ad esempio, il valore<sup>0 del pixel della</sup> riga<sup>0 dell'</sup> analisi dei dati bitmap di una bitmap di 10 pixel per 10 pixel sarà il 0<sup>°</sup> pixel della riga di analisi 9<sup>°</sup> dell'immagine visualizzata o stampata. Le bitmap in formato RLE (Run-Length codificate) e le bitmap [**struttura BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) non possono essere bitmap dall'alto verso il basso. Le righe di analisi sono allineate a **DWORD** , ad eccezione delle bitmap compresse da RLE. Devono essere riempiti per le larghezze di riga di analisi, in byte, che non sono divisibili equamente per quattro, ad eccezione delle bitmap compresse RLE. Ad esempio, una bitmap da 10 a 10 pixel a 24 BPP avrà due byte di riempimento alla fine di ogni riga di analisi.

 

 
