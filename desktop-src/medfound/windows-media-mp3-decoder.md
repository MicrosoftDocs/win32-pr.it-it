---
description: Il Windows decodificatore MP3 multimediale decodifica i file audio codificati nei formati seguenti.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Windows Decodificatore MP3 multimediale (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58788a00ddaa43686c3cb4be4a52292edb3fe6c6f81fabbc5b4f3e75c47f0f24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737000"
---
# <a name="windows-media-mp3-decoder"></a>Windows Decodificatore MP3 multimediale

Il Windows decodificatore MP3 multimediale decodifica i file audio codificati nei formati seguenti.

-   ISO/IEC 11172-3 (MPEG-1 Audio) Livello 3
-   ISO/IEC 13818-3 (MPEG-2 Audio) Livello 3, estensione a bassa frequenza di campionamento

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il decodificatore MP3 Windows media è rappresentato dalla costante **CLSID \_ CMP3DecMediaObject**. È possibile creare un'istanza del decodificatore MP3 chiamando **CoCreateInstance**.

## <a name="interfaces"></a>Interfacce

Un oggetto decodificatore MP3 espone **l'interfaccia IMediaObject** in modo che l'oggetto possa essere usato come oggetto multimediale DirectX (DMO) ed espone l'interfaccia **IMFTransform** in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Un Windows Media MP3 si comporta come un DMO o un MFT a seconda delle interfacce che si ottengono e della versione di Windows in esecuzione. La tabella seguente illustra le condizioni in cui un Windows Media MP3 si comporta come DMO o MFT.



| Sistema operativo | Comportamento del decodificatore                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Un Windows media MP3 si comporta sempre come un DMO.                                                                                                                                           |
| Windows Vista    | Per impostazione predefinita, un Windows media MP3 si comporta come un DMO. Se si ottiene **un'interfaccia IMFTransform** o **un'interfaccia IPropertyStore** in un decodificatore MP3 Windows Media, si comporta come MFT. |
| Windows 7        | Per impostazione predefinita, un Windows media MP3 si comporta come un DMO. Se si ottiene **un'interfaccia IMFTransform** in un Windows decoder MP3 di Media, si comporta come un MFT.                                    |



 

## <a name="input-formats"></a>Formati di input

Nella tabella seguente viene illustrato il tag del formato audio che rappresenta il tipo di input supportato dal Windows decoder MP3 multimediale.



| Costante tag di formato      | Formatta il valore del tag | Formato audio     |
|--------------------------|------------------|------------------|
| FORMATO \_ WAVE \_ MPEGLAYER3 | 0x55             | ISO MPEG Layer 3 |



 

## <a name="output-formats"></a>Formati di output

La tabella seguente illustra i tag di formato audio che rappresentano i tipi di output supportati dal Windows decoder MP3 multimediale.



| Costante tag di formato       | Formatta il valore del tag | Formato audio                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| FORMATO \_ WAVE \_ PCM         | 0x0001           | Formato PCM (se usato come DMO o MFT)                                   |
| FORMATO \_ WAVE \_ IEEE \_ FLOAT | 0x0003           | Virgola mobile IEEE (se usata come MFT)                                   |
| FORMATO \_ WAVE \_ ESTENDIBILE  | 0xFFFE           | Formato PCM/IEEE nella **struttura WAVEFORMATEXTENSIBLE** (se usato come MFT) |



 

Il Windows media MP3 supporta ed enumera i tipi di supporti di output seguenti.

-   Tipo di output con la stessa frequenza di campionamento e lo stesso numero di canali del tipo di input.
-   Output mono per l'input stereo.
-   Tipi di output con profondità in bit di 8 e 16.
-   Output a virgola mobile, se il decodificatore si comporta come MFT.

Il Windows media MP3 supporta, ma non enumera, i tipi di supporti di output seguenti.

-   Tipo di output con metà della frequenza di campionamento del tipo di input.
-   Tipo di output con un quarto della frequenza di campionamento del tipo di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Mp3dmod.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione di codec](codecimplementation.md)
</dt> </dl>

 

 




