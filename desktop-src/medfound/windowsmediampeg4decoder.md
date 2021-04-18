---
description: Il decodificatore Windows Media MPEG4 v1/v2 decodifica i flussi video MPEG4 v1/v2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Decodificatore Windows Media MPEG4 v1/v2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b14cf22e29c1266ac9bb3593375ee4485d79df2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320513"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a>Decoder Windows Media MPEG4 v1/v2

Il decodificatore Windows Media MPEG4 v1/v2 decodifica i flussi video MPEG4 v1/v2.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il decodificatore Windows Media MPEG4 v1/v2 è rappresentato dalla costante **CLSID \_ CMpeg4DecMediaObject**. È possibile creare un'istanza del decodificatore MPEG4 v1/v2 chiamando **CoCreateInstance**.

## <a name="formats"></a>Formati

Il decodificatore Windows Media MPEG4 v1/v2 supporta i tipi di supporti di input seguenti.

-   \_MPG4 MEDIASUBTYPE
-   \_MPG4 MEDIASUBTYPE
-   \_MP42 MEDIASUBTYPE
-   \_MP42 MEDIASUBTYPE

Il decodificatore Windows Media MPEG4 v1/v2 supporta i sottotipi di supporti di output seguenti quando funge da oggetto DMO (DirectX Media Object).

-   \_YUY2 MEDIASUBTYPE
-   \_UYVY MEDIASUBTYPE
-   \_Rgb32 MEDIASUBTYPE
-   \_RGB24 MEDIASUBTYPE
-   \_RGB565 MEDIASUBTYPE
-   \_RGB8 MEDIASUBTYPE
-   \_RGB555 MEDIASUBTYPE

Il decodificatore Windows Media MPEG4 v1/v2 supporta i sottotipi di supporti di output seguenti quando funge da trasformazione Media Foundation (MFT).

-   \_YUY2 MFVideoFormat
-   \_UYVY MFVideoFormat
-   \_Rgb32 MFVideoFormat
-   \_RGB24 MFVideoFormat
-   \_RGB565 MFVideoFormat
-   \_RGB8 MFVideoFormat
-   \_RGB555 MFVideoFormat

## <a name="remarks"></a>Commenti

L'oggetto decodificatore Windows Media MPEG4 v1/v2 espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT). L'oggetto ha lo stesso identificatore di classe (CLSID), indipendentemente dal fatto che funga da DMO o da MFT.

Un decodificatore MPEG4 v1/v2 si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione. Nella tabella seguente vengono illustrate le condizioni in base alle quali un decodificatore MPEG4 v1/v2 si comporta come DMO o MFT.



| Sistema operativo            | Comportamento del decodificatore                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un decodificatore MPEG4 v1/v2 si comporta sempre come DMO.                                                                                                                                 |
| Windows Vista e Windows 7 | Per impostazione predefinita, un decodificatore MPEG4 v1/v2 si comporta come DMO. Se si ottiene un'interfaccia [GUID del sottotipo video](video-subtype-guids.md) in un decodificatore MPEG4 v1/v2, si comporta come un MFT. |



 

Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un decodificatore funga da DMO o da un MFT. I GUID per i sottotipi di supporti non RGB sono gli stessi, indipendentemente dal fatto che un decodificatore funga da DMO o da un MFT. Per informazioni sui GUID che rappresentano sottotipi video, vedere [GUID del sottotipo video](video-subtype-guids.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MPG4DECD.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
