---
description: Imposta i parametri peak &\# 0034;leaky bucket&0034; (vedere Note) per la codifica di un \# file Windows Media. Questi parametri vengono usati per la velocità in bit di picco. Impostare questo attributo usando l'interfaccia IMFASFStreamConfig.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: MF_ASFSTREAMCONFIG_LEAKYBUCKET2 attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a540cab766cbd6a6a7246139d0e19e12c89e5ed837d40cdc3e10d9589f72ebe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060841"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a>Attributo \_ LEAKYBUCKET2 di MF ASFSTREAMCONFIG \_

Imposta i parametri di picco "bucket di perdita" (vedere Osservazioni) per la codifica di un Windows file multimediale. Questi parametri vengono usati per la velocità in bit di picco. Impostare questo attributo usando [**l'interfaccia IMFASFStreamConfig.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Il valore di questo attributo è una matrice di **tre DWORD** nell'ordine seguente:

-   Velocità in bit, in bit al secondo.
-   Finestra del buffer, in millisecondi.
-   Fullness iniziale del buffer, in byte.

Per altre informazioni sul concetto di bucket di perdita, vedere l'argomento [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) nella documentazione di Windows Media Format SDK.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi ASF](asf-attributes.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**PERDITA \_ DI MF ASFSTREAMCONFIGYBUCKET1 \_**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




