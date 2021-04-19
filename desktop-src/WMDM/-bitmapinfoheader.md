---
title: Struttura _BITMAPINFOHEADER
description: La \_ struttura BITMAPINFOHEADER definisce il formato di un frame video.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- Struttura di _BITMAPINFOHEADER Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481c80b6d209e0da8d00ef06d88392504bcae8e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331904"
---
# <a name="_bitmapinfoheader-structure"></a>\_Struttura BITMAPINFOHEADER

La struttura **\_ BITMAPINFOHEADER** definisce il formato di un frame video.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**Dimensioni**
</dt> <dd>

Specifica il numero di byte necessari per la struttura.

</dd> <dt>

**biWidth**
</dt> <dd>

Specifica la larghezza della bitmap in pixel.

</dd> <dt>

**bialtezza**
</dt> <dd>

Specifica l'altezza della bitmap in pixel. Se **biHeight** è positivo, la bitmap è un valore DIB bottom-up e la relativa origine è l'angolo inferiore sinistro. Se **biHeight** è negativo, la bitmap è un DIB dall'alto verso il basso e l'origine è l'angolo superiore sinistro. Se **biHeight** è un valore negativo, a indicare una DIB dall'alto verso il basso, la **bicompressione** deve essere bi \_ RGB o bi \_ campi. Non è possibile comprimere l'inizio dell'attività.

</dd> <dt>

**Biplani**
</dt> <dd>

Specifica il numero di piani per il dispositivo di destinazione. Questo valore deve essere impostato su 1.

</dd> <dt>

**biBitCount**
</dt> <dd>

Specifica il numero di bit per pixel. Il membro **biBitCount** della struttura **BITMAPINFOHEADER** determina il numero di bit che definiscono ogni pixel e il numero massimo di colori nella bitmap. Questo membro deve essere uno dei valori seguenti.



| Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | La bitmap è monocromatica e il membro bmiColors contiene due voci. Ogni bit nella matrice bitmap rappresenta un pixel. Se il bit è chiaro, il pixel viene visualizzato con il colore della prima voce nella tabella bmiColors. Se viene impostato il bit, il pixel presenta il colore della seconda voce della tabella.                                                                                                                                                                                                                                                                                                        |
| 2     | La bitmap ha quattro valori di colore possibili.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 4     | La bitmap ha un massimo di 16 colori e il membro bmiColors contiene fino a 16 voci. Ogni pixel della bitmap è rappresentato da un indice a 4 bit nella tabella dei colori. Se, ad esempio, il primo byte nella bitmap è 0x1F, il byte rappresenta due pixel. Il primo pixel contiene il colore nella seconda voce della tabella e il secondo pixel contiene il colore nella voce della tabella sedicesimo.                                                                                                                                                                                                                 |
| 8     | La bitmap ha un massimo di 256 colori e il membro bmiColors contiene fino a 256 voci. In questo caso, ogni byte della matrice rappresenta un singolo pixel.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 16    | La bitmap ha un massimo di 2 ^ 16 colori. Se il membro della bicompressione di BITMAPINFOHEADER è BI \_ RGB, il membro bmiColors è **null**. Ogni parola nella matrice bitmap rappresenta un singolo pixel. Le intensità relative di rosso, verde e blu sono rappresentate da 5 bit per ogni componente colore. Il valore per il blu è nei 5 bit meno significativi, seguito da 5 bit ciascuno per il verde e il rosso. Il bit più significativo non viene utilizzato. La tabella dei colori bmiColors viene utilizzata per l'ottimizzazione dei colori utilizzati nei dispositivi basati su tavolozza e deve contenere il numero di voci specificate dal membro biClrUsed. |
| 24    | La bitmap ha un massimo di 2 ^ 24 colori e il membro bmiColors è **null**. Ogni tripletta a 3 byte nella matrice di bitmap rappresenta le intensità relative rispettivamente di blu, verde e rosso per un pixel. La tabella dei colori bmiColors viene utilizzata per l'ottimizzazione dei colori utilizzati nei dispositivi basati su tavolozza e deve contenere il numero di voci specificate dal membro biClrUsed.                                                                                                                                                                                                                                     |
| 32    | La bitmap ha un massimo di 2 ^ 32 colori. Se il membro di biCompression è BI \_ RGB, il membro bmiColors è **null**. Ogni valore DWORD nella matrice di bitmap rappresenta le intensità relative di un pixel, rispettivamente blu, verde e rosso. Il byte elevato in ogni DWORD non viene utilizzato. La tabella dei colori bmiColors viene utilizzata per l'ottimizzazione dei colori utilizzati nei dispositivi basati su tavolozza e deve contenere il numero di voci specificate dal membro biClrUsed.                                                                                                                                                                 |



 

</dd> <dt>

**bicompressione**
</dt> <dd>

Specifica il tipo di compressione per una bitmap compressa dal basso verso l'alto. Questo membro può essere uno dei valori seguenti.



| Valore         | Descrizione                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_RGB bi       | Formato non compresso.                                                                                                                                                                                                                                                                                            |
| \_campi bi | Specifica che la bitmap non è compressa e che la tabella dei colori è costituita da tre maschere colori DWORD che specificano rispettivamente i componenti rosso, verde e blu di ogni pixel. Questa operazione è valida se utilizzata con bitmap a 16 BPP e 32-BPP. Questo valore è valido in Microsoft Windows CE versione 2,0 e successive. |



 

</dd> <dt>

**biSizeImage**
</dt> <dd>

Specifica la dimensione, in byte, dell'immagine. Questo valore può essere impostato su zero per le \_ bitmap RGB bi.

</dd> <dt>

**biXPelsPerMeter**
</dt> <dd>

Specifica la risoluzione orizzontale in pixel per contatore del dispositivo di destinazione per la bitmap. Un'applicazione può usare questo valore per selezionare una bitmap da un gruppo di risorse che corrisponde meglio alle caratteristiche del dispositivo corrente.

</dd> <dt>

**biYPelsPerMeter**
</dt> <dd>

Specifica la risoluzione verticale, in pixel per contatore, del dispositivo di destinazione per la bitmap.

</dd> <dt>

**biClrUsed**
</dt> <dd>

Specifica il numero di indici di colori nella tabella dei colori che vengono effettivamente utilizzati dalla bitmap. Se questo valore è zero, la bitmap usa il numero massimo di colori corrispondente al valore del membro **biBitCount** per la modalità di compressione specificata da **biCompression**.

</dd> <dt>

**biClrImportant**
</dt> <dd>

Specifica il numero di indici di colore necessari per visualizzare la bitmap. Se questo valore è zero, tutti i colori sono obbligatori.

Se biClrUsed è diverso da zero e il membro biBitCount è inferiore a 16, il membro biClrUsed specifica il numero effettivo di colori a cui il motore di grafica o il driver di dispositivo accede. Se biBitCount è maggiore o uguale a 16, il membro biClrUsed specifica la dimensione della tabella dei colori utilizzata per ottimizzare le prestazioni delle tavolozze dei colori di sistema. Se biBitCount è uguale a 16 o 32, la tavolozza dei colori ottimale inizia immediatamente dopo le tre maschere DWORD.

Se la bitmap è una bitmap compressa, ovvero una bitmap in cui la matrice bitmap segue immediatamente la \_ struttura BITMAPINFOHEADER e a cui fa riferimento un solo puntatore, il membro biClrUsed deve essere pari a zero o alla dimensione effettiva della tabella dei colori.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura è contenuta all'interno di una struttura **\_ VIDEOINFOHEADER** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](structures.md)
</dt> <dt>

[**\_VIDEOINFOHEADER**](-videoinfoheader.md)
</dt> </dl>

 

 





