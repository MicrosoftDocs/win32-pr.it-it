---
description: Il Windows decodificatore MPEG-4 V3 multimediale decodifica i flussi video MPEG-4 V3.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Windows Decodificatore MPEG-4 V3 multimediale (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 975351d04b0876b5f1793d442e41d54a585062bd1fed778902fee5c4c83dcd6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100918"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a>Windows Decodificatore MPEG-4 V3 multimediale

Il Windows decodificatore MPEG-4 V3 multimediale decodifica i flussi video MPEG-4 V3.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il Windows decodificatore MPEG-4 V3 è rappresentato dalla costante **CLSID \_ CMpeg43DecMediaObject**. È possibile creare un'istanza del decodificatore MPEG-4 V3 chiamando **CoCreateInstance**.

## <a name="formats"></a>Formati

Il Windows media MPEG-4 V3 supporta i tipi di supporti di input seguenti.

-   MEDIASUBTYPE \_ MP43
-   MEDIASUBTYPE \_ mp43

Il Windows media MPEG-4 V3 supporta i sottotipi di supporti di output seguenti quando funge da oggetto multimediale DirectX (DMO).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

Il Windows media MPEG-4 V3 supporta i sottotipi di supporti di output seguenti quando funge da Media Foundation Transform (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Commenti

L'oggetto decodificatore MPEG-4 V3 di Windows Media espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come oggetto directx media (DMO) ed espone [**l'interfaccia IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT). L'oggetto ha lo stesso identificatore di classe (CLSID) indipendentemente dal fatto che funge da DMO o MFT.

Il decodificatore MPEG-4 V3 si comporta come un DMO o un MFT a seconda delle interfacce che si ottengono e della versione di Windows in esecuzione. La tabella seguente illustra le condizioni in cui un decodificatore MPEG-4 V3 si comporta come DMO o MFT.



| Sistema operativo            | Comportamento del decodificatore                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Il decodificatore MPEG-4 V3 si comporta sempre come un DMO.                                                                                                                      |
| Windows Vista e Windows 7 | Per impostazione predefinita, il decodificatore MPEG-4 V3 si comporta come un DMO. Se si ottiene [**un'interfaccia IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) nel decodificatore MPEG-4 V3, si comporta come un MFT. |



 

Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un decodificatore funge da DMO o MFT. I GUID per i sottotipi multimediali non RGB sono gli stessi, indipendentemente dal fatto che un decodificatore agirà come DMO o MFT. Per informazioni sui GUID che rappresentano i sottotipi multimediali, vedere [GUID di sottotipo video](video-subtype-guids.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP43DECD.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
