---
description: Il decodificatore Windows Media MP3 decodifica i file audio codificati nei formati seguenti.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Windows Media MP3 decoder (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332290"
---
# <a name="windows-media-mp3-decoder"></a>Decoder Windows Media MP3

Il decodificatore Windows Media MP3 decodifica i file audio codificati nei formati seguenti.

-   ISO/IEC 11172-3 (MPEG-1 audio) Layer 3
-   ISO/IEC 13818-3 (MPEG-2 audio) Layer 3, estensione frequenza di campionamento bassa

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il decodificatore Windows Media MP3 è rappresentato dalla costante **CLSID \_ CMP3DecMediaObject**. È possibile creare un'istanza del decodificatore MP3 chiamando **CoCreateInstance**.

## <a name="interfaces"></a>Interfacce

Un oggetto decoder MP3 espone l'interfaccia **IMediaObject** in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia **IMFTransform** in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Un decodificatore Windows Media MP3 si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione. Nella tabella seguente vengono illustrate le condizioni in base alle quali un decodificatore Windows Media MP3 si comporta come DMO o MFT.



| Sistema operativo | Comportamento del decodificatore                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Un decodificatore Windows Media MP3 si comporta sempre come DMO.                                                                                                                                           |
| Windows Vista    | Per impostazione predefinita, un decodificatore Windows Media MP3 si comporta come DMO. Se si ottiene un'interfaccia **IMFTransform** o un'interfaccia **IPropertyStore** su un decodificatore Windows Media MP3, si comporta come una MFT. |
| Windows 7        | Per impostazione predefinita, un decodificatore Windows Media MP3 si comporta come DMO. Se si ottiene un'interfaccia **IMFTransform** in un decodificatore Windows Media MP3, si comporta come un MFT.                                    |



 

## <a name="input-formats"></a>Formati di input

Nella tabella seguente viene illustrato il tag di formato audio che rappresenta il tipo di input supportato dal decodificatore Windows Media MP3.



| Costante tag di formato      | Valore del tag di formato | Formato audio     |
|--------------------------|------------------|------------------|
| \_Formato Wave \_ MPEGLAYER3 | 0x55             | MPEG Layer 3 ISO |



 

## <a name="output-formats"></a>Formati di output

La tabella seguente illustra i tag di formato audio che rappresentano i tipi di output supportati dal decodificatore Windows Media MP3.



| Costante tag di formato       | Valore del tag di formato | Formato audio                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| \_PCM in formato Wave \_         | 0x0001           | Formato PCM (se usato come DMO o MFT)                                   |
| \_formato Wave \_ IEEE \_ float | 0x0003           | Virgola mobile IEEE (se usato come MFT)                                   |
| \_formato Wave \_ estendibile  | 0xFFFE           | Formato PCM/IEEE nella struttura **WAVEFORMATEXTENSIBLE** (se usato come MFT) |



 

Il decodificatore Windows Media MP3 supporta ed enumera i tipi di supporti di output seguenti.

-   Tipo di output con lo stesso frequenza di campionamento e numero di canali del tipo di input.
-   Output mono per input stereo.
-   Tipi di output con profondità di bit di 8 e 16.
-   Output a virgola mobile, se il decodificatore si comporta come un MFT.

Il decodificatore Windows Media MP3 supporta, ma non enumera, i seguenti tipi di supporti di output.

-   Tipo di output con metà della frequenza di campionamento del tipo di input.
-   Tipo di output con un quarto della frequenza di campionamento del tipo di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Mp3dmod.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione del codec](codecimplementation.md)
</dt> </dl>

 

 




