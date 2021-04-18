---
description: Imposta la media &\# 0034; bucket a perdita&\# 0034; parametri (vedere la sezione Osservazioni) per la codifica di un file di Windows Media. Impostare questo attributo usando l'interfaccia IMFASFStreamConfig.
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: Attributo MF_ASFSTREAMCONFIG_LEAKYBUCKET1 (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db383d19ff5009ccc9fc3203281e04000870474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309592"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a>\_Attributo MF ASFSTREAMCONFIG \_ LEAKYBUCKET1

Imposta i parametri medi "bucket Leak" (vedere le note) per la codifica di un file di Windows Media. Impostare questo attributo usando l'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Il valore di questo attributo è una matrice di tre **DWORD** s, nell'ordine seguente:

-   Velocità in bit, in bit al secondo.
-   Finestra buffer, in millisecondi.
-   Completezza del buffer iniziale, in byte.

Per ulteriori informazioni sul concetto di bucket con perdite, vedere l'argomento [modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md) nella documentazione di Windows Media Format SDK.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi ASF](asf-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: seblob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




