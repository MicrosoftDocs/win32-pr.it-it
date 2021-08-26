---
description: Specifica la dominanza del campo per un fotogramma video interlacciato.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: MFSampleExtension_BottomFieldFirst attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ab0a9847977ea25d93190911bbf2280629f0219eba3d4c4ddfb492e9fdcd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113071"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a>Attributo BottomFieldFirst di MFSampleExtension \_

Specifica la dominanza del campo per un fotogramma video interlacciato. Questo attributo si applica agli esempi di supporti.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**Esempio IMF**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Se il fotogramma video è interlacciato e l'esempio contiene due campi interleaved, questo attributo indica quale campo viene visualizzato per primo. Se **TRUE,** il campo inferiore è il primo nel tempo. Se **FALSE,** il primo campo è il primo.

Se il frame è interlacciato e l'esempio contiene un singolo campo, questo attributo indica il campo contenuto nell'esempio. Se **TRUE,** l'esempio contiene il campo inferiore. Se **FALSE,** l'esempio contiene il campo superiore.

Se il frame è progressivo, questo attributo descrive come ordinare i campi quando l'output è interlacciato. Se **TRUE,** il campo inferiore deve essere restituito per primo. Se **FALSE,** il primo campo deve essere restituito per primo.

Se questo attributo non è impostato, il tipo di supporto descrive la dominanza del campo.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> <dt>

[Interlacciamento video](video-interlacing.md)
</dt> </dl>

 

 




