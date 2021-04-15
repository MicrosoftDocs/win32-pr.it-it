---
description: Transizione di cancellazione SMPTE
ms.assetid: 9271bd4b-57b1-4b1b-bfee-d6ae5f49a154
title: Transizione di cancellazione SMPTE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47de62c450ff0d75f72e5fac466801991b987834
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521713"
---
# <a name="smpte-wipe-transition"></a>Transizione di cancellazione SMPTE

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

La transizione di cancellazione SMPTE produce uno dei cancellamenti standard definiti dalla società di Motion Picture and Television Engineers (SMPTE) nel documento SMPTE 258M-1993, ad eccezione della divisione quad.

![transizione cancellazione in corso](images/trans-wipe.png)

ID classe (CLSID): {DE75D012-7A65-11D2-8CEA-00A0C9441E20}

Nome variabile CLSID: CLSID \_ DxtJpeg

Nome descrittivo: "DxtJpeg"

Proprietà



| Proprietà       | Type   | Predefinito  | Descrizione                                                                                                                                                                                                                                                                                                      |
|----------------|--------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ColoreBordo    | long   | 0x000000 | Colore del bordo intorno ai bordi del pattern di cancellazione. Il valore di questo attributo è un numero esadecimale con formato 0x *RRGGBB*, dove *RR* è il valore rosso, *GG* è il valore verde e *BB* è il valore blu. (Pertanto, i puri rossi, verdi e blu sono rispettivamente 0xFF000, 0x00FF00 e 0x0000FF). |
| BorderSoftness | long   | 0        | Larghezza dell'area sfocata intorno ai bordi del pattern di cancellazione. Specificare zero per nessuna area sfocata.                                                                                                                                                                                                              |
| SpessoreBordo    | long   | 0        | Larghezza del bordo a tinta unita lungo i bordi del pattern di cancellazione. Specificare zero per nessun bordo.                                                                                                                                                                                                                       |
| MaskName       | BSTR   | **NULL** | Se non è **null**, specifica il nome di un file JPEG da usare come maschera di cancellazione anziché una cancellazione standard incorporata. Il file deve contenere una sfumatura monocromatica a 8 bit per pixel. La sfumatura viene utilizzata come maschera per definire la progressione della cancellazione.                                                                 |
| MaskNum        | long   | 1        | Codice di cancellazione SMPTE standard che specifica lo stile di cancellazione da usare. Per un elenco di codici di cancellazione e degli schemi associati, vedere il documento SMPTE 258M-1993.                                                                                                                                                            |
| OffsetX        | long   | 0        | Offset orizzontale dell'origine della cancellazione dal centro dell'immagine. Valido solo per i valori **MaskNum** compresi tra 101 e 131.                                                                                                                                                                                         |
| OffsetY        | long   | 0        | Offset verical dell'origine della cancellazione dal centro dell'immagine. Valido solo per i valori **MaskNum** compresi tra 101 e 131.                                                                                                                                                                                            |
| ReplicateX     | long   | 0        | Numero di volte in cui replicare il pattern di cancellazione orizzontalmente. Valido solo per i valori **MaskNum** compresi tra 101 e 131.                                                                                                                                                                                                |
| Replica     | long   | 0        | Numero di volte in cui replicare il pattern di cancellazione verticalmente. Valido solo per i valori **MaskNum** compresi tra 101 e 131.                                                                                                                                                                                                  |
| ScaleX         | double | 1.0      | Valore in base al quale estendere orizzontalmente la cancellazione come percentuale della definizione di cancellazione originale. Valido solo per i valori **MaskNum** compresi tra 101 e 131.                                                                                                                                                         |
| ScaleY         | double | 1.0      | Valore in base al quale estendere verticalmente la cancellazione, come percentuale della definizione di cancellazione originale. Valido solo per i valori **MaskNum** compresi tra 101 e 131.                                                                                                                                                           |



 

## <a name="remarks"></a>Commenti

Questa transizione supporta le salviettine SMPTE standard seguenti:



| Number | Descrizione                   | Number | Descrizione                                 |
|--------|-------------------------------|--------|---------------------------------------------|
| 1      | Ridimensionamento orizzontale                    | 211    | Radiale, da sinistra a destra, in alto                     |
| 2      | Vertical                      | 212    | Radiale, verso il basso, a destra                      |
| 3      | In alto a sinistra                    | 213    | Radiale, da sinistra a destra, dall'alto in basso              |
| 4      | In alto a destra                   | 214    | Radiale, verso il basso, a sinistra e a destra                 |
| 5      | In basso a destra                   | 221    | Radiale, superiore                                 |
| 6      | In basso a sinistra                    | 222    | Radiale, a destra                               |
| 7      | Quattro angoli                  | 223    | Radiale, inferiore                              |
| 8      | Quattro quadrati                  | 224    | Radiale, a sinistra                                |
| 21     | Porte fienile, verticali          | 225    | Radiale, superiore in senso orario, inferiore in senso orario     |
| 22     | Door Barn, orizzontale        | 226    | Radiale, a sinistra in senso orario, a destra     |
| 23     | In alto al centro                    | 227    | Radiale, superiore in senso orario, inferiore antiorario |
| 24     | A destra al centro                  | 228    | Radiale, sinistro in senso orario, a destra |
| 25     | In basso al centro                 | 231    | Radiale, superiore Split                           |
| 26     | A sinistra al centro                   | 232    | Radiale, divisione destra                         |
| 41     | Diagonale, NW a SE            | 233    | Radiale, divisione inferiore                        |
| 42     | Diagonale, NE a SW            | 234    | Radiale, divisione sinistra                          |
| 43     | Triangoli, superiore/inferiore         | 235    | Divisione radiale, superiore inferiore                    |
| 44     | Triangoli, a sinistra o a destra         | 236    | Divisione radiale, da sinistra a destra                    |
| 45     | Stripe diagonale, da SW a NE     | 241    | Radiale, angolo superiore sinistro                     |
| 46     | Striscia diagonale, NW per SE     | 242    | Radiale, angolo inferiore sinistro                  |
| 47     | Cross                         | 243    | Radiale, angolo inferiore destro                 |
| 48     | Casella Diamond                   | 244    | Radiale, angolo superiore destro                    |
| 61     | Cuneo, superiore                    | 245    | Radiale, in alto a sinistra, in basso a destra              |
| 62     | Cuneo, a destra                  | 246    | Radiale, in basso a sinistra, in alto a destra              |
| 63     | Cuneo, inferiore                 | 251    | Radiale centrale, superiore                          |
| 64     | Cuneo, a sinistra                   | 252    | Radiale centrale, a sinistra                         |
| 65     | V                             | 253    | Radiale centrale, inferiore                       |
| 66     | V, a destra                      | 254    | Radiale centrale, a destra                        |
| 67     | V, invertito                   | 261    | Box radiale, a destra                           |
| 68     | V, a sinistra                       | 262    | Box radiale, superiore                             |
| 71     | Dente di sega, a sinistra                | 263    | Radiale centrale, superiore, inferiore                  |
| 72     | Dente di sega, superiore                 | 264    | Radiale centrale, a sinistra, a destra                  |
| 73     | Dente di sega, verticale            | 301    | Matrice, orizzontale                          |
| 74     | Dente di sega, orizzontale          | 302    | Matrice, verticale                            |
| 101    | Box                           | 303    | Matrix, diagonale, in alto a sinistra                  |
| 102    | Diamond                       | 304    | Matrix, diagonale, in alto a destra                 |
| 103    | Triangolo, su                  | 305    | Matrix, diagonale, in basso a destra              |
| 104    | Triangolo, a destra               | 306    | Matrix, diagonale, in basso a sinistra               |
| 105    | Triangolo, in basso              | 310    | Matrix, in senso orario superiore sinistro                  |
| 106    | Triangolo, a sinistra                | 311    | Matrix, in senso orario superiore destro                 |
| 107    | Freccia a capo, su                | 312    | Matrix, in senso orario in basso a destra              |
| 108    | Freccia di direzione, a destra             | 313    | Matrix, in senso orario in basso a sinistra               |
| 109    | Freccia giù              | 314    | Matrix, superiore sinistro in senso antiorario              |
| 110    | Freccia a sinistra              | 315    | Matrix, in senso antiorario superiore destro             |
| 111    | Pentagono, su                  | 316    | Matrix, antiorario in basso a destra          |
| 112    | Pentagono, giù                | 317    | Matrix, in basso a sinistra           |
| 113    | Esagono                       | 320    | Matrix, verticale in alto a sinistra, in alto a destra        |
| 114    | Esagono, ruotato              | 321    | Matrix, verticale in basso a sinistra, in basso a destra  |
| 119    | Circle                        | 322    | Matrix, verticale in alto a sinistra, in basso a destra     |
| 120    | Ovale, orizzontale              | 323    | Matrix, verticale in basso a sinistra, in alto a destra     |
| 121    | Ovale, verticale                | 324    | Matrix, orizzontale in alto a sinistra, in basso a sinistra    |
| 122    | Occhio, orizzontale               | 325    | Matrix, orizzontale in alto a destra, in basso a destra  |
| 123    | Occhio, verticale                 | 326    | Matrix, orizzontale in alto a sinistra, in basso a destra   |
| 124    | Rettangolo arrotondato, orizzontale | 327    | Matrix, orizzontale in alto a destra, in basso a sinistra   |
| 125    | Rettangolo arrotondato, verticale   | 328    | Matrix, diagonale in basso a sinistra, in alto a destra     |
| 127    | stella a 4 punte                  | 329    | Matrix, diagonale in alto a sinistra, in basso a destra     |
| 128    | stella a 4 punte                  | 340    | Matrice, doppia spirale superiore                   |
| 129    | stella a 6 punte                  | 341    | Matrice, spirale doppia inferiore                |
| 130    | Cuore                         | 342    | Matrice, doppia spirale sinistra                  |
| 131    | Serratura                       | 343    | Matrix, doppia spirale a destra                 |
| 201    | Radiale, 12 ore            | 344    | Matrix, spirale quadre, dall'alto in basso             |
| 202    | Radiale, 3 ore             | 345    | Matrix, spirale quadre, sinistra-destra             |
| 203    | Radiale, 06:00             | 350    | Cascata, a sinistra                             |
| 204    | Radiale, 9.00             | 351    | Cascata, a destra                            |
| 205    | Radiale, 12 + 6 ore        | 352    | Waterfall, orizzontale, a sinistra                 |
| 206    | Radiale, 3 + 9 ore         | 353    | Waterfall, orizzontale, a destra                |
| 207    | Radiale, a 4 vie                 | 409    | Maschera casuale                                 |



 

 

 



