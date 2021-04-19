---
description: Il decodificatore Voice Windows Media Audio decodifica i flussi codificati dal codificatore Voice Windows Media Audio.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Decodificatore Windows Media Audio Voice (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326964"
---
# <a name="windows-media-audio-voice-decoder"></a>Decodificatore Voice Windows Media Audio

Il decodificatore Voice Windows Media Audio decodifica i flussi codificati dal [**codificatore voice Windows Media Audio**](windowsmediaaudiovoiceencoder.md).

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il decodificatore Voice Windows Media Audio è rappresentato dalla costante **CLSID \_ CWMSPDecMediaObject**. È possibile creare un'istanza del decodificatore vocale chiamando **CoCreateInstance**.

## <a name="input-formats"></a>Formati di input

Windows Media Audio contenuto con codifica Voice viene identificato dal tag di formato 0x00A.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmod.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Uso del codec Windows Media Audio Voice](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Codificatore Voice Windows Media Audio](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




