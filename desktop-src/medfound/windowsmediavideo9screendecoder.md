---
description: Il decodificatore di Windows Media Video 9 dello schermo decodifica i flussi codificati dal codificatore dello schermo Windows Media Video 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Decodificatore dello schermo Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327979"
---
# <a name="windows-media-video-9-screen-decoder"></a>Decodificatore dello schermo Windows Media Video 9

Il decodificatore di Windows Media Video 9 dello schermo decodifica i flussi codificati dal [**codificatore dello schermo Windows Media video 9**](windowsmediavideo9screenencoder.md).

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il decodificatore della schermata Windows Media Video 9 è rappresentato dalla costante **CLSID \_ CMSSCDecMediaObject**. È possibile creare un'istanza del decodificatore chiamando **CoCreateInstance**.

## <a name="input-types"></a>Tipi di input

Il codice di quattro caratteri (FOURCC) per il contenuto codificato Windows Media Video schermata versione 9 è "MSS2".

I tipi di input seguenti sono supportati dal decodificatore dello schermo versione 9.

-   \_Mss2 MEDIASUBTYPE

## <a name="output-types"></a>Tipi di output

I tipi di output seguenti sono supportati dal decodificatore dello schermo versione 9 quando viene usato come DMO (DirectX Media Object).

-   \_RGB24 MEDIASUBTYPE
-   \_Rgb32 MEDIASUBTYPE
-   \_ARGB32 MEDIASUBTYPE
-   \_RGB565 MEDIASUBTYPE
-   \_RGB555 MEDIASUBTYPE
-   \_RGB8 MEDIASUBTYPE

I tipi di output seguenti sono supportati dal decodificatore dello schermo versione 9 quando viene usato come trasformazione Media Foundation (MFT).

-   \_RGB24 MFVideoFormat
-   \_Rgb32 MFVideoFormat
-   \_ARGB32 MFVideoFormat
-   \_RGB565 MFVideoFormat
-   \_RGB555 MFVideoFormat
-   \_RGB8 MFVideoFormat

## <a name="remarks"></a>Commenti

Un oggetto decodificatore dello schermo espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Un decodificatore dello schermo si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione. Nella tabella seguente vengono illustrate le condizioni in base alle quali un decodificatore dello schermo si comporta come DMO o MFT.



| Sistema operativo            | Comportamento del decodificatore                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un decodificatore Windows Media Screen si comporta sempre come DMO.                                                                                                                 |
| Windows Vista e Windows 7 | Per impostazione predefinita, un decodificatore Windows Media Screen si comporta come DMO. Se si ottiene un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) su un decodificatore dello schermo, si comporta come un MFT. |



 

È possibile utilizzare lo stesso CLSID (CLSID \_ CMSSCDecMediaObject) per creare il decodificatore dello schermo versione 7 e il decodificatore della schermata versione 9. Il FOURCC per il contenuto codificato Windows Media Video schermata versione 7 è "MSS1". Il decodificatore della schermata versione 7 supporta il \_ tipo di input MSS1 di MEDIASUBTYPE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsdecd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione del codec](codecimplementation.md)
</dt> <dt>

[Uso del codec della schermata Windows Media Video 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Codificatore dello schermo Windows Media Video 9](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
