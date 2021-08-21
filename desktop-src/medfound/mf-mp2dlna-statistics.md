---
description: Ottiene le statistiche dal sink multimediale DLNA (Digital Living Network Alliance).
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: MF_MP2DLNA_STATISTICS attributo (Mfmp2dlna.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a80bf0682cf6e46845a968122bf512a6e9cff15df8fb8e0312e1c63c8dab0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973620"
---
# <a name="mf_mp2dlna_statistics-attribute"></a>Attributo MF \_ MP2DLNA \_ STATISTICS

Ottiene le statistiche dal sink multimediale DLNA (Digital Living Network Alliance).

## <a name="data-type"></a>Tipo di dati

**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** archiviato come **BYTE \[ \]**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

## <a name="remarks"></a>Commenti

Durante il flusso, il sink multimediale DLNA aggiorna questo attributo con le statistiche sulla codifica e il multiplexing dei flussi MPEG-2. L'applicazione può eseguire query su questo attributo in qualsiasi momento per ottenere i valori più recenti.

L'impostazione di questo attributo sul sink multimediale DLNA non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmp2dlna.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




