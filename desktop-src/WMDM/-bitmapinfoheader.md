---
title: _BITMAPINFOHEADER struttura
description: La \_ struttura BITMAPINFOHEADER definisce il formato di un fotogramma video.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- _BITMAPINFOHEADER struttura di Windows Media Device Manager
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
ms.openlocfilehash: 5f2d0da3d05fe050f32d5a35bbbe7de558e1c4962fa84a958855b2960e343942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586885"
---
# <a name="_bitmapinfoheader-structure"></a>\_Struttura BITMAPINFOHEADER

La **\_ struttura BITMAPINFOHEADER** definisce il formato di un fotogramma video.

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

**biSize**
</dt> <dd>

Specifica il numero di byte richiesti dalla struttura .

</dd> <dt>

**biWidth**
</dt> <dd>

Specifica la larghezza della bitmap, in pixel.

</dd> <dt>

**biHeight**
</dt> <dd>

Specifica l'altezza della bitmap, in pixel. Se **biHeight** è positivo, la bitmap è un DIB dal basso verso l'alto e l'origine è l'angolo inferiore sinistro. Se **biHeight** è negativo, la bitmap è un DIB dall'alto verso il basso e l'origine è l'angolo superiore sinistro. Se **biHeight** è negativo, a indicare un DIB dall'alto verso il basso, **biCompression** deve essere BI RGB o \_ BI \_ BITFIELDS. I DIB dall'alto verso il basso non possono essere compressi.

</dd> <dt>

**Biplani**
</dt> <dd>

Specifica il numero di piani per il dispositivo di destinazione. Questo valore deve essere impostato su 1.

</dd> <dt>

**biBitCount**
</dt> <dd>

Specifica il numero di bit per pixel. Il **membro biBitCount** della struttura **BITMAPINFOHEADER** determina il numero di bit che definiscono ogni pixel e il numero massimo di colori nella bitmap. Questo membro deve essere uno dei valori seguenti.



| Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | La bitmap è monocromatica e il membro bmiColors contiene due voci. Ogni bit nella matrice di bitmap rappresenta un pixel. Se il bit è chiaro, il pixel viene visualizzato con il colore della prima voce nella tabella bmiColors; Se il bit è impostato, il pixel ha il colore della seconda voce nella tabella.                                                                                                                                                                                                                                                                                                        |
| 2     | La bitmap ha quattro valori di colore possibili.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 4     | La bitmap ha un massimo di 16 colori e il membro bmiColors contiene fino a 16 voci. Ogni pixel nella bitmap è rappresentato da un indice a 4 bit nella tabella dei colori. Ad esempio, se il primo byte nella bitmap è 0x1F, il byte rappresenta due pixel. Il primo pixel contiene il colore nella seconda voce di tabella e il secondo pixel contiene il colore nella sedicesima voce della tabella.                                                                                                                                                                                                                 |
| 8     | La bitmap ha un massimo di 256 colori e il membro bmiColors contiene fino a 256 voci. In questo caso, ogni byte nella matrice rappresenta un singolo pixel.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 16    | La bitmap ha un massimo di 2^16 colori. Se il membro biCompression di BITMAPINFOHEADER è BI \_ RGB, il membro bmiColors è **NULL.** Ogni parola nella matrice di bitmap rappresenta un singolo pixel. Le intensità relative di rosso, verde e blu sono rappresentate con 5 bit per ogni componente del colore. Il valore per il blu è nei 5 bit meno significativi, seguiti da 5 bit ciascuno per il verde e il rosso. Il bit più significativo non viene usato. La tabella dei colori bmiColors viene usata per ottimizzare i colori usati nei dispositivi basati sulla tavolozza e deve contenere il numero di voci specificato dal membro biClrUsed. |
| 24    | La bitmap ha un massimo di 2^24 colori e il membro bmiColors è **NULL.** Ogni tripletta a 3 byte nella matrice di bitmap rappresenta rispettivamente l'intensità relativa di blu, verde e rosso per un pixel. La tabella dei colori bmiColors viene usata per ottimizzare i colori usati nei dispositivi basati sulla tavolozza e deve contenere il numero di voci specificato dal membro biClrUsed.                                                                                                                                                                                                                                     |
| 32    | La bitmap ha un massimo di 2^32 colori. Se il membro biCompression è BI \_ RGB, il membro bmiColors è **NULL.** Ogni valore DWORD nella matrice di bitmap rappresenta rispettivamente l'intensità relativa di blu, verde e rosso per un pixel. Il byte più alto in ogni DWORD non viene usato. La tabella dei colori bmiColors viene usata per ottimizzare i colori usati nei dispositivi basati sulla tavolozza e deve contenere il numero di voci specificato dal membro biClrUsed.                                                                                                                                                                 |



 

</dd> <dt>

**biCompression**
</dt> <dd>

Specifica il tipo di compressione per una bitmap compressa dal basso verso l'alto (i DIB dall'alto verso il basso non possono essere compressi). Questo membro può essere uno dei valori seguenti.



| Valore         | Descrizione                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BI \_ RGB       | Formato non compresso.                                                                                                                                                                                                                                                                                            |
| BI \_ BITFIELDS | Specifica che la bitmap non è compressa e che la tabella dei colori è costituita da tre maschere di colore DWORD che specificano rispettivamente i componenti rosso, verde e blu di ogni pixel. Questa opzione è valida se usata con bitmap a 16 e 32 bpp. Questo valore è valido in Microsoft Windows CE versione 2.0 e successive. |



 

</dd> <dt>

**biSizeImage**
</dt> <dd>

Specifica le dimensioni dell'immagine, in byte. Può essere impostato su zero per le \_ bitmap RGB bi.

</dd> <dt>

**biXPelsPerMeter**
</dt> <dd>

Specifica la risoluzione orizzontale, in pixel per contatore, del dispositivo di destinazione per la bitmap. Un'applicazione può usare questo valore per selezionare una bitmap da un gruppo di risorse che meglio corrisponde alle caratteristiche del dispositivo corrente.

</dd> <dt>

**biYPelsPerMeter**
</dt> <dd>

Specifica la risoluzione verticale, in pixel per contatore, del dispositivo di destinazione per la bitmap.

</dd> <dt>

**biClrUsed**
</dt> <dd>

Specifica il numero di indici dei colori nella tabella dei colori effettivamente utilizzati dalla bitmap. Se questo valore è zero, la bitmap usa il numero massimo di colori corrispondente al valore del membro **biBitCount** per la modalità di compressione specificata da **biCompression.**

</dd> <dt>

**biClrImportant**
</dt> <dd>

Specifica il numero di indici di colore necessari per la visualizzazione della bitmap. Se questo valore è zero, sono necessari tutti i colori.

Se biClrUsed è diverso da zero e il membro biBitCount è minore di 16, il membro biClrUsed specifica il numero effettivo di colori a cui accede il motore di grafica o il driver di dispositivo. Se biBitCount è maggiore o uguale a 16, il membro biClrUsed specifica le dimensioni della tabella dei colori usata per ottimizzare le prestazioni delle tavolozze dei colori di sistema. Se biBitCount è uguale a 16 o 32, la tavolozza dei colori ottimale inizia immediatamente dopo le tre maschere DWORD.

Se la bitmap è compressa (una bitmap in cui la matrice bitmap segue immediatamente la struttura BITMAPINFOHEADER e vi fa riferimento un singolo puntatore), il membro biClrUsed deve essere zero o la dimensione effettiva della tabella dei \_ colori.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura è contenuta all'interno **\_ di una struttura VIDEOINFOHEADER.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](structures.md)
</dt> <dt>

[**\_VIDEOINFOHEADER**](-videoinfoheader.md)
</dt> </dl>

 

 





