---
description: Il decodificatore Windows Media MPEG-4 v3 decodifica i flussi video MPEG-4 v3.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Windows Media MPEG-4 v3 decoder (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ee98a0a3c4b221da6f2000e32d4c75bc3e3a93b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320575"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a>Decodificatore Windows Media MPEG-4 v3

Il decodificatore Windows Media MPEG-4 v3 decodifica i flussi video MPEG-4 v3.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il decodificatore MPEG-4 V3 di Windows è rappresentato dalla costante **CLSID \_ CMpeg43DecMediaObject**. È possibile creare un'istanza del decodificatore MPEG-4 v3 chiamando **CoCreateInstance**.

## <a name="formats"></a>Formati

Il decodificatore Windows Media MPEG-4 V3 supporta i tipi di supporti di input seguenti.

-   \_Mp43 MEDIASUBTYPE
-   \_Mp43 MEDIASUBTYPE

Il decodificatore Windows Media MPEG-4 V3 supporta i sottotipi di supporti di output seguenti quando funge da oggetto DMO (DirectX Media Object).

-   \_YUY2 MEDIASUBTYPE
-   \_UYVY MEDIASUBTYPE
-   \_Rgb32 MEDIASUBTYPE
-   \_RGB24 MEDIASUBTYPE
-   \_RGB565 MEDIASUBTYPE
-   \_RGB8 MEDIASUBTYPE
-   \_RGB555 MEDIASUBTYPE

Il decodificatore Windows Media MPEG-4 V3 supporta i sottotipi di supporti di output seguenti quando funge da trasformazione Media Foundation (MFT).

-   \_YUY2 MFVideoFormat
-   \_UYVY MFVideoFormat
-   \_Rgb32 MFVideoFormat
-   \_RGB24 MFVideoFormat
-   \_RGB565 MFVideoFormat
-   \_RGB8 MFVideoFormat
-   \_RGB555 MFVideoFormat

## <a name="remarks"></a>Commenti

L'oggetto decodificatore Windows Media MPEG-4 v3 espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT). L'oggetto ha lo stesso identificatore di classe (CLSID), indipendentemente dal fatto che funga da DMO o da MFT.

Il decodificatore MPEG-4 V3 si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione. Nella tabella seguente vengono illustrate le condizioni in base alle quali un decodificatore MPEG-4 V3 si comporta come DMO o MFT.



| Sistema operativo            | Comportamento del decodificatore                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Il decodificatore MPEG-4 V3 si comporta sempre come DMO.                                                                                                                      |
| Windows Vista e Windows 7 | Per impostazione predefinita, il decodificatore MPEG-4 V3 si comporta come DMO. Se si ottiene un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sul decodificatore MPEG-4 v3, si comporta come un MFT. |



 

Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un decodificatore funga da DMO o da un MFT. I GUID per i sottotipi di supporti non RGB sono gli stessi, indipendentemente dal fatto che un decodificatore funga da DMO o da un MFT. Per informazioni sui GUID che rappresentano sottotipi di supporti, vedere GUID del [sottotipo video](video-subtype-guids.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP43DECD.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
