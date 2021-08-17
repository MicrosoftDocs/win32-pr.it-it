---
description: Il Windows media MPEG4 V1/V2 decodifica i flussi video MPEG4 V1/V2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Windows Decodificatore MPEG4 V1/V2 multimediale (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c55d5c64cec2a0ad08978064d40c26267d7729adeee9a9f148c8e682ba168509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100933"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a>Windows Decodificatore MPEG4 V1/V2 multimediale

Il Windows media MPEG4 V1/V2 decodifica i flussi video MPEG4 V1/V2.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il Windows media MPEG4 V1/V2 è rappresentato dalla costante **CLSID \_ CMpeg4DecMediaObject**. È possibile creare un'istanza del decodificatore MPEG4 V1/V2 chiamando **CoCreateInstance.**

## <a name="formats"></a>Formati

Il Windows media MPEG4 V1/V2 supporta i tipi di supporti di input seguenti.

-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ mpg4
-   MEDIASUBTYPE \_ MP42
-   MEDIASUBTYPE \_ mp42

Il Windows media MPEG4 V1/V2 supporta i sottotipi di supporti di output seguenti quando funge da oggetto multimediale DirectX (DMO).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

Il Windows media MPEG4 V1/V2 supporta i sottotipi multimediali di output seguenti quando funge da Media Foundation Transform (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Commenti

L'oggetto decodificatore Windows Media MPEG4 V1/V2 espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come oggetto multimediale DirectX (DMO) ed espone [**l'interfaccia IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come Media Foundation Transform (MFT). L'oggetto ha lo stesso identificatore di classe (CLSID) indipendentemente dal fatto che agisca come DMO o MFT.

Un decodificatore MPEG4 V1/V2 si comporta come un DMO o un MFT a seconda delle interfacce che si ottengono e della versione di Windows in esecuzione. La tabella seguente illustra le condizioni in cui un decodificatore MPEG4 V1/V2 si comporta come un DMO o un MFT.



| Sistema operativo            | Comportamento del decodificatore                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un decodificatore MPEG4 V1/V2 si comporta sempre come un DMO.                                                                                                                                 |
| Windows Vista e Windows 7 | Per impostazione predefinita, un decodificatore MPEG4 V1/V2 si comporta come un DMO. Se si ottiene [un'interfaccia GUID](video-subtype-guids.md) sottotipo video in un decodificatore MPEG4 V1/V2, si comporta come un MFT. |



 

Gli identificatori univoci globali (GUID) per i sottotipi multimediali RGB variano a seconda che un decodificatore agiti come DMO o MFT. I GUID per sottotipi multimediali non RGB sono gli stessi, indipendentemente dal fatto che un decodificatore funge da DMO o MFT. Per informazioni sui GUID che rappresentano sottotipi video, vedere [VIDEO Subtype GUID](video-subtype-guids.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MPG4DECD.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
