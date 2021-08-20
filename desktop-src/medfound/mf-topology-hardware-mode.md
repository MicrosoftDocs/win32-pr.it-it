---
description: Specifica se caricare le trasformazioni Microsoft Media Foundation hardware (MFT) nella topologia.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: MF_TOPOLOGY_HARDWARE_MODE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52da08dc1da36072f02627ec632bb8caf189c1748545c1ded5c3e4ebdedc1234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875668"
---
# <a name="mf_topology_hardware_mode-attribute"></a>Attributo MF \_ TOPOLOGY \_ HARDWARE \_ MODE

Specifica se caricare le trasformazioni Microsoft Media Foundation hardware (MFT) nella topologia.

## <a name="data-type"></a>Tipo di dati

**[**MFTOPOLOGY \_ MODALITÀ \_ HARDWARE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** archiviata come **UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**Topologia IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Impostare l'attributo prima di risolvere la topologia.



| Valore                                  | Descrizione                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFTOPOLOGY \_ HWMODE \_ USE \_ HARDWARE**  | Il caricatore della topologia carica MFT basati su hardware, ad esempio decodificatori hardware, quando disponibile.<br/> Il caricatore della topologia esegue automaticamente il fall back alla decodifica software se non viene trovato alcun decodificatore hardware o se un decodificatore hardware non riesce a connettersi per qualche motivo.<br/> |
| **MFTOPOLOGY \_ HWMODE \_ SOFTWARE \_ ONLY** | Il caricatore della topologia carica solo MFT software, inclusi i decodificatori software.                                                                                                                                                                                                    |



 

Il valore predefinito è **MFTOPOLOGY \_ HWMODE \_ SOFTWARE \_ ONLY**, per la compatibilità con le applicazioni esistenti. Il valore consigliato è **MFTOPOLOGY \_ HWMODE \_ USE \_ HARDWARE**.

Se il caricatore della topologia inserisce un MFT hardware nella topologia, imposta l'attributo [MFT \_ ENUM \_ HARDWARE URL \_ \_ Attribute](mft-enum-hardware-url-attribute.md) nel nodo della topologia. Per verificare se è presente un MFT hardware, enumerare i nodi nella topologia risolta e verificare se questo attributo è presente.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 




