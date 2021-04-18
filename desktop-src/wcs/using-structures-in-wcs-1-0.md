---
title: Uso di strutture in WCS 1,0
description: La maggior parte delle strutture usate da WCS 1,0 è molto semplice e richiede una spiegazione minima. Sono documentati nella sezione di riferimento WCS 1,0 intitolata Structures.
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- Windows Color System (WCS), strutture
- WCS (sistema di colori Windows), strutture
- Gestione colori immagine, strutture
- gestione dei colori, strutture
- colori, strutture
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d6e434ccfa6d96aa815f0c1997dc7f34178a32
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320943"
---
# <a name="using-structures-in-wcs-10"></a>Uso di strutture in WCS 1,0

La maggior parte delle strutture usate da WCS 1,0 è molto semplice e richiede una spiegazione minima. Sono documentati nella sezione di riferimento WCS 1,0 intitolata [Structures](structures.md).

Le eccezioni sono la struttura [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) utilizzata dalla funzione [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) e le strutture di Windows seguenti definite in wingdi. h:

-   [BITMAPV5HEADER](#windows-bitmap-header-structures)
-   [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [**CIE XYZ**](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [**CIEXYZTRIPLE**](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

Gli argomenti seguenti sono trattati a una lunghezza maggiore:

-   [Strutture di intestazione bitmap di Windows](#windows-bitmap-header-structures)
-   [Differenze tra le intestazioni V4 e V5](#differences-between-v4-and-v5-headers)
-   [Bitmap.exe: utilità Command-Line per la conversione delle intestazioni bitmap](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a>Strutture di intestazione bitmap di Windows

WCS 1,0 consente di collegare o incorporare i profili dei colori ICC in bitmap indipendenti dal dispositivo. Ciò consente di caratterizzare i colori DIB in modo più accurato rispetto a quanto fosse possibile utilizzando WCS in Windows 95. [BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , la nuova struttura dell'intestazione bitmap, è definita in wingdi. h nella versione di Windows 98. Ai fini dello sviluppo, viene anche incluso nel file ICM. h con i riferimenti di questo programmatore. La struttura **BITMAPV5HEADER** è la seguente:


```C++
typedef struct {
    DWORD        bV5Size;
    LONG         bV5Width;
    LONG         bV5Height;
    WORD         bV5Planes;
    WORD         bV5BitCount;
    DWORD        bV5Compression;
    DWORD        bV5SizeImage;
    LONG         bV5XPelsPerMeter;
    LONG         bV5YPelsPerMeter;
    DWORD        bV5ClrUsed;
    DWORD        bV5ClrImportant;
    DWORD        bV5RedMask;
    DWORD        bV5GreenMask;
    DWORD        bV5BlueMask;
    DWORD        bV5AlphaMask;
    DWORD        bV5CSType;
    CIEXYZTRIPLE bV5Endpoints;
    DWORD        bV5GammaRed;
    DWORD        bV5GammaGreen;
    DWORD        bV5GammaBlue;
    DWORD        bV5Intent;         // Rendering intent for bitmap 
    DWORD        bV5ProfileData;    // Offset to profile data 
    DWORD        bV5ProfileSize;    // Size of embedded profile data 
    DWORD        bV5Reserved;       // Should be zero 
} BITMAPV5HEADER, FAR *LPBITMAPV5HEADER, *PBITMAPV5HEADER;
```



Il membro **bV5CSType** può avere il profilo dei valori \_ embedded o profile \_ collegato per specificare se un profilo è incorporato o collegato alla DIB. Il membro **bV5ProfileData** è l'offset in byte dall'inizio della struttura **BITMAPV5HEADER** all'inizio dei dati del profilo. Se il profilo è incorporato, i dati del profilo sono i profili effettivi e, se sono collegati, i dati del profilo sono il nome file con terminazione null del profilo. Non può essere una stringa Unicode. Deve essere composto esclusivamente da caratteri del set di caratteri di Windows (tabella codici 1252).

Quando una DIB viene caricata in memoria, i dati del profilo (se presente) devono seguire la tabella dei colori e **bV5ProfileData** deve fornire l'offset dei dati di profilo dall'inizio della struttura **BITMAPV5HEADER** . Il valore di questo membro sarà diverso ora, perché i bit bitmap non seguono la tabella dei colori in memoria. Le applicazioni devono modificare il membro **bV5ProfileData** dopo il caricamento della DIB in memoria.

Per quanto riguarda la precedenza compressa, i dati del profilo devono seguire i bit bitmap simili al formato del file. Il membro **bV5ProfileData** deve comunque assegnare l'offset dei dati di profilo dall'inizio della struttura **BITMAPV5HEADER** .

Le applicazioni devono accedere ai dati del profilo solo quando **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** è incorporato nel profilo \_ o collegato al profilo \_ .

Se un profilo è collegato, il percorso del profilo può essere qualsiasi nome completo (incluso un percorso di rete) che può essere aperto tramite la funzione **CreateFile** di Win32.

## <a name="differences-between-v4-and-v5-headers"></a>Differenze tra le intestazioni V4 e V5

Quando si lavora con la nuova struttura bitmap, è utile riconoscere le differenze nella modalità di configurazione delle strutture **BITMAPV4HEADER** e **BITMAPV5HEADER** :



| Intestazione V4     | Significato                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **bV4CSType** | \_RGB calibrato di LCS \_ . Questo valore implica che i punti finali e gamma siano specificati nei campi appropriati. I valori fasulli provocano problemi. |
| **bV4CSType** | LCS \_ sRGB. Questo valore implica che la bitmap si trovi nello spazio dei colori di sRGB (gamma ed endpoint ignorati).                                 |
| **bV4CSType** | \_ \_ spazio colore Windows LCS \_ . Questo valore implica che la bitmap si trovi nello spazio dei colori predefinito di Windows.                                    |



 



| Intestazione V5     | Significato                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bV5CSType** | \_RGB calibrato di LCS \_ . Questo valore implica che i punti finali e gamma siano specificati nei campi appropriati. I valori fasulli provocano problemi.                         |
| **bV5CSType** | LCS \_ sRGB. Questo valore implica che la bitmap si trovi nello spazio dei colori di sRGB (gamma ed endpoint ignorati).                                                         |
| **bV5CSType** | PROFILO \_ incorporato. Questo valore implica che **bV5ProfileData** punta a un buffer di memoria che contiene il profilo da usare (i gamma e gli endpoint vengono ignorati). |
| **bV5CSType** | PROFILO \_ collegato. Questo valore implica che **bV5ProfileData** punta al nome file del profilo da usare (i gamma e gli endpoint vengono ignorati).                |
| **bV5CSType** | \_ \_ spazio colore Windows LCS \_ . Questo valore implica che la bitmap si trovi nello spazio dei colori predefinito di Windows.                                                            |



 

Per convertire le bitmap meno recenti da e verso la nuova struttura **BITMAPV5HEADER** , un file dell'utilità di conversione da riga di comando denominato Bitmap.exe è incluso nella Guida di riferimento per programmatori WCS 1,0.

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a>BitMap.exe: utilità Command-Line per la conversione delle intestazioni bitmap

Bitmap.exe è un'utilità da riga di comando che si trova nella \\ cartella bin nella cartella di installazione specificata. Modifica le intestazioni delle bitmap di Windows, consentendo di convertire le bitmap esistenti dalle strutture di intestazione **BITMAPINFOHEADER** e **BITMAPV4HEADER** alla struttura **BITMAPV5HEADER** più recente e viceversa. La sintassi della riga di comando è la seguente:


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



Le opzioni della riga di comando hanno gli effetti seguenti.



| Opzione | Significato                                                                  |
|--------|--------------------------------------------------------------------------|
| /d     | I valori predefiniti vengono immessi automaticamente nelle intestazioni convertite.       |
| /1     | Converte le bitmap specificate in **BITMAPINFOHEADER**                    |
| /4     | Converte le bitmap specificate in **BITMAPV4HEADER**                      |
| /5     | Converte le bitmap specificate in **BITMAPV5HEADER**                      |
| /f     | Forza la conversione, anche se la bitmap ha già l'intestazione corretta       |
| /s     | Converte le bitmap nella cartella specificata e in tutte le sottodirectory |



 

 

 