---
description: Transizione di cancellazione SMPTE
ms.assetid: 9271bd4b-57b1-4b1b-bfee-d6ae5f49a154
title: Transizione di cancellazione SMPTE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40db8097b61d1b750f8e17067bda08f94a54504c8e990656b7416d84a9a1c089
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050437"
---
# <a name="smpte-wipe-transition"></a>Transizione di cancellazione SMPTE

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

La transizione SMPTE Wipe produce una delle cancellazioni standard definite dalla Society of Motion Picture and Television Engineers (SMPTE) nel documento SMPTE 258M-1993, ad eccezione della divisione quad.

![Transizione di cancellazione dei dati in corso](images/trans-wipe.png)

ID classe (CLSID): {DE75D012-7A65-11D2-8CEA-00A0C9441E20}

Nome variabile CLSID: CLSID \_ DxtJpeg

Nome descrittivo: "DxtJpeg"

Proprietà



| Proprietà       | Type   | Predefinito  | Descrizione                                                                                                                                                                                                                                                                                                      |
|----------------|--------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ColoreBordo    | long   | 0x000000 | Colore del bordo intorno ai bordi del modello di cancellazione. Il valore di questo attributo è un numero esadecimale con formato 0x *RRGGBB*, dove *RR* è il valore rosso, *GG* è il valore verde e *BB* è il valore blu. Di conseguenza, rosso puro, verde e blu sono 0xFF000, 0x00FF00 e 0x0000FF, rispettivamente. |
| BorderSoftness | long   | 0        | Larghezza dell'area sfocata intorno ai bordi del modello di cancellazione. Specificare zero per nessuna area sfocata.                                                                                                                                                                                                              |
| SpessoreBordo    | long   | 0        | Larghezza del bordo a tinta unita lungo i bordi del modello di cancellazione. Specificare zero per nessun bordo.                                                                                                                                                                                                                       |
| MaskName       | BSTR   | **NULL** | Se non **è NULL,** specifica il nome di un file JPEG da usare come maschera di cancellazione anziché una cancellazione predefinita standard. Il file deve contenere una sfumatura monocromatica a 8 bit per pixel. La sfumatura viene usata come maschera per definire la progressione della cancellazione.                                                                 |
| MaskNum        | long   | 1        | Codice di cancellazione SMPTE standard che specifica lo stile di cancellazione da usare. Per un elenco dei codici di cancellazione e dei relativi schemi associati, vedere il documento SMPTE 258M-1993.                                                                                                                                                            |
| OffsetX        | long   | 0        | Offset orizzontale dell'origine di cancellazione dal centro dell'immagine. Valido solo per i valori **di MaskNum** da 101 a 131.                                                                                                                                                                                         |
| OffsetY        | long   | 0        | Offset verico dell'origine di cancellazione dal centro dell'immagine. Valido solo per i valori **di MaskNum** da 101 a 131.                                                                                                                                                                                            |
| ReplicateX     | long   | 0        | Numero di volte in cui replicare orizzontalmente il modello di cancellazione. Valido solo per i valori **di MaskNum** da 101 a 131.                                                                                                                                                                                                |
| Replica     | long   | 0        | Numero di volte in cui replicare verticalmente il modello di cancellazione. Valido solo per i valori **di MaskNum** da 101 a 131.                                                                                                                                                                                                  |
| Scalex         | double | 1.0      | Quantità in base alla quale estendere la cancellazione orizzontalmente, come percentuale della definizione di cancellazione originale. Valido solo per i valori **di MaskNum** da 101 a 131.                                                                                                                                                         |
| Scaley         | double | 1.0      | Quantità in base alla quale estendere verticalmente la cancellazione, come percentuale della definizione di cancellazione originale. Valido solo per i valori **di MaskNum** da 101 a 131.                                                                                                                                                           |



 

## <a name="remarks"></a>Commenti

Questa transizione supporta le cancellazioni SMPTE standard seguenti:



| Number | Descrizione                   | Number | Descrizione                                 |
|--------|-------------------------------|--------|---------------------------------------------|
| 1      | Ridimensionamento orizzontale                    | 211    | Radiale, a sinistra a destra, in alto                     |
| 2      | Vertical                      | 212    | Radiale, verso l'alto verso il basso, a destra                      |
| 3      | In alto a sinistra                    | 213    | Radiale, a sinistra a destra, in alto in basso              |
| 4      | In alto a destra                   | 214    | Radiale, verso l'alto, a sinistra a destra                 |
| 5      | In basso a destra                   | 221    | Radiale, in alto                                 |
| 6      | In basso a sinistra                    | 222    | Radiale, a destra                               |
| 7      | Quattro angoli                  | 223    | Radiale, inferiore                              |
| 8      | Quattro quadrati                  | 224    | Radiale, a sinistra                                |
| 21     | Porte del barn, verticali          | 225    | Radiale, in alto in senso orario, in senso orario inferiore     |
| 22     | Porte barn, orizzontali        | 226    | Radiale, in senso orario a sinistra, a destra in senso orario     |
| 23     | In alto al centro                    | 227    | Radiale, in alto in senso orario, in senso antiorario inferiore |
| 24     | Centro a destra                  | 228    | Radiale, in senso orario a sinistra, a destra in senso antiorario |
| 25     | In basso al centro                 | 231    | Radiale, divisione superiore                           |
| 26     | Centro a sinistra                   | 232    | Radiale, divisione a destra                         |
| 41     | Diagonale, da NW a edizione Standard            | 233    | Radiale, divisione inferiore                        |
| 42     | Diagonale, da NE a SW            | 234    | Radiale, divisione a sinistra                          |
| 43     | Triangoli, in alto/in basso         | 235    | Radiale, divisione in alto in basso                    |
| 44     | Triangoli, a sinistra/a destra         | 236    | Radiale, divisione a sinistra a destra                    |
| 45     | Striscia diagonale, da SW a NE     | 241    | Radiale, angolo superiore sinistro                     |
| 46     | Striscia diagonale, da NW a edizione Standard     | 242    | Radiale, angolo inferiore sinistro                  |
| 47     | Cross                         | 243    | Radiale, angolo inferiore destro                 |
| 48     | Diamond Box                   | 244    | Radiale, angolo superiore destro                    |
| 61     | Cuneo, in alto                    | 245    | Radiale, in alto a sinistra, in basso a destra              |
| 62     | Cuneo, a destra                  | 246    | Radiale, in basso a sinistra, in alto a destra              |
| 63     | Cuneo, inferiore                 | 251    | Radiale centrale, in alto                          |
| 64     | Cuneo, a sinistra                   | 252    | Radiale centrale, a sinistra                         |
| 65     | V                             | 253    | Radiale centrale, inferiore                       |
| 66     | V, a destra                      | 254    | Radiale centrale, a destra                        |
| 67     | V, invertito                   | 261    | Riquadro radiale, a destra                           |
| 68     | V, a sinistra                       | 262    | Riquadro radiale, in alto                             |
| 71     | Sawtooth, a sinistra                | 263    | Radiale centrale, superiore, inferiore                  |
| 72     | Sawtooth, top                 | 264    | Radiale centrale, a sinistra, a destra                  |
| 73     | Sega, verticale            | 301    | Matrice, orizzontale                          |
| 74     | Sega, orizzontale          | 302    | Matrice, verticale                            |
| 101    | Casella                           | 303    | Matrice, diagonale, in alto a sinistra                  |
| 102    | Diamond                       | 304    | Matrice, diagonale, in alto a destra                 |
| 103    | Triangolo verso l'alto                  | 305    | Matrice, diagonale, in basso a destra              |
| 104    | Triangolo, a destra               | 306    | Matrice, diagonale, in basso a sinistra               |
| 105    | Triangolo, inferiore              | 310    | Matrice, in senso orario in alto a sinistra                  |
| 106    | Triangolo a sinistra                | 311    | Matrice, in senso orario in alto a destra                 |
| 107    | Freccia a capo, su                | 312    | Matrice, in senso orario in basso a destra              |
| 108    | Freccia a capo, a destra             | 313    | Matrice, in senso orario in basso a sinistra               |
| 109    | Freccia a capo, giù              | 314    | Matrice, in senso antiorario in alto a sinistra              |
| 110    | Freccia a capo, a sinistra              | 315    | Matrice, in senso antiorario in alto a destra             |
| 111    | Pentagono, su                  | 316    | Matrice, in senso antiorario in basso a destra          |
| 112    | Freccia verso il basso                | 317    | Matrice, in senso antiorario in basso a sinistra           |
| 113    | Esagono                       | 320    | Matrice, verticale in alto a sinistra, in alto a destra        |
| 114    | Esagono, ruotato              | 321    | Matrice, verticale in basso a sinistra, in basso a destra  |
| 119    | Circle                        | 322    | Matrice, verticale in alto a sinistra, in basso a destra     |
| 120    | Ovale, orizzontale              | 323    | Matrice, verticale in basso a sinistra, in alto a destra     |
| 121    | Ovale, verticale                | 324    | Matrice, orizzontale in alto a sinistra, in basso a sinistra    |
| 122    | Occhio, orizzontale               | 325    | Matrice, orizzontale in alto a destra, in basso a destra  |
| 123    | Occhio, verticale                 | 326    | Matrice, orizzontale in alto a sinistra, in basso a destra   |
| 124    | Rettangolo arrotondato, orizzontale | 327    | Matrice, orizzontale in alto a destra, in basso a sinistra   |
| 125    | Rettangolo arrotondato, verticale   | 328    | Matrice, diagonale in basso a sinistra, in alto a destra     |
| 127    | Stella a 4 punti                  | 329    | Matrice, diagonale in alto a sinistra, in basso a destra     |
| 128    | Stella a 4 punti                  | 340    | Matrice, top double double double                   |
| 129    | Stella a 6 punti                  | 341    | Matrice, double double bottom                |
| 130    | Cuore                         | 342    | Matrice, doppia a sinistra                  |
| 131    | Keyhole                       | 343    | Matrix, right double double matrix                 |
| 201    | Radiale, ore 12            | 344    | Matrice, quadruplo, dall'alto verso il basso             |
| 202    | Radiale, ore 3             | 345    | Matrice, quadruplo, sinistra-destra             |
| 203    | Radiale, ore 6             | 350    | A cascata, a sinistra                             |
| 204    | Radiale, ore 9             | 351    | Cascata, destra                            |
| 205    | Radiale, 12 + 6 ore        | 352    | Cascata, orizzontale, sinistra                 |
| 206    | Radiale, 3 + 9 ore         | 353    | Cascata, orizzontale, destra                |
| 207    | Radiale, 4-way                 | 409    | Maschera casuale                                 |



 

 

 



