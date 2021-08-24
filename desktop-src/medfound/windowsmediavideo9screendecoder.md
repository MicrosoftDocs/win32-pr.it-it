---
description: Il Windows decodificatore dello schermo di Media Video 9 decodifica i flussi codificati dal codificatore di schermo Windows Media Video 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Windows Decodificatore schermo Media Video 9 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2e081423c4c5efc2d44fdf78c7c6a94a00dae86d40d761a06ab0de07fa5d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462391"
---
# <a name="windows-media-video-9-screen-decoder"></a>Windows Decodificatore schermo Media Video 9

Il Windows decodificatore dello schermo di Media Video 9 decodifica i flussi codificati dal codificatore di schermo [**Windows Media Video 9.**](windowsmediavideo9screenencoder.md)

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il Windows decoder dello schermo di Media Video 9 è rappresentato dalla costante **\_ CLSID CMSSCDecMediaObject**. È possibile creare un'istanza del decodificatore chiamando **CoCreateInstance**.

## <a name="input-types"></a>Tipi di input

Il codice a quattro caratteri (FOURCC) per Windows contenuto codificato di Media Video Screen versione 9 è "MSS2".

I tipi di input seguenti sono supportati dal decodificatore dello schermo versione 9.

-   MEDIASUBTYPE \_ MSS2

## <a name="output-types"></a>Tipi di output

I tipi di output seguenti sono supportati dal decodificatore dello schermo versione 9 quando viene usato come oggetto multimediale DirectX (DMO).

-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

I tipi di output seguenti sono supportati dal decodificatore dello schermo versione 9 quando viene usato come Media Foundation Transform (MFT).

-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="remarks"></a>Commenti

Un oggetto decodificatore dello schermo espone [**l'interfaccia IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come oggetto directx media (DMO) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Un decodificatore dello schermo si comporta come DMO o MFT a seconda delle interfacce che si ottengono e della versione Windows in esecuzione. La tabella seguente illustra le condizioni in cui un decodificatore dello schermo si comporta come DMO o MFT.



| Sistema operativo            | Comportamento del decodificatore                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un Windows Media Screen si comporta sempre come un DMO.                                                                                                                 |
| Windows Vista e Windows 7 | Per impostazione predefinita, un Windows media screen si comporta come un DMO. Se si ottiene [**un'interfaccia IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in un decodificatore dello schermo, si comporta come un MFT. |



 

È possibile usare lo stesso CLSID (CLSID CMSSCDecMediaObject) per creare il decodificatore dello schermo versione 7 e il decodificatore dello schermo \_ versione 9. Il contenuto codificato FOURCC Windows Media Video Screen versione 7 è "MSS1". Il decodificatore dello schermo versione 7 supporta il tipo di input MEDIASUBTYPE \_ MSS1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsdecd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione di codec](codecimplementation.md)
</dt> <dt>

[Uso del codec Windows video multimediale 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Codificatore di schermo Media Video 9](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
