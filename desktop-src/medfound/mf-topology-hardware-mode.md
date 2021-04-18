---
description: Specifica se caricare le trasformazioni di Microsoft Media Foundation basate su hardware (MFTs) nella topologia.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: Attributo MF_TOPOLOGY_HARDWARE_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec7933e9a380bbf5e66f4030a214f3f4aa93abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305367"
---
# <a name="mf_topology_hardware_mode-attribute"></a>\_ \_ Attributo modalità hardware della TOPOLOGIa MF \_

Specifica se caricare le trasformazioni di Microsoft Media Foundation basate su hardware (MFTs) nella topologia.

## <a name="data-type"></a>Tipo di dati

**[**MFTOPOLOGY \_ \_Modalità hardware**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** archiviata come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Impostare l'attributo prima di risolvere la topologia.



| Valore                                  | Descrizione                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFTOPOLOGY \_ HWMODE \_ Usa l' \_ hardware**  | Il caricatore della topologia caricherà i MFTs basati su hardware, ad esempio i decodificatori hardware, quando disponibili.<br/> Il caricatore della topologia esegue automaticamente il fallback alla decodifica software se non viene trovato alcun decodificatore hardware o se un decodificatore hardware non riesce a connettersi per qualche motivo.<br/> |
| **\_solo MFTOPOLOGY HWMODE \_ software \_** | Il caricatore della topologia caricherà solo MFTs software, inclusi i decodificatori software.                                                                                                                                                                                                    |



 

Il valore predefinito è **\_ \_ \_ solo MFTOPOLOGY HWMODE software**, per la compatibilità con le applicazioni esistenti. Il valore consigliato è **MFTOPOLOGY \_ HWMODE \_ use \_ hardware**.

Se il caricatore della topologia inserisce una MFT hardware nella topologia, imposta l'attributo dell' [ \_ \_ \_ \_ attributo dell'URL dell'enumerazione MFT](mft-enum-hardware-url-attribute.md) nel nodo della topologia. Per verificare se è presente un hardware MFT, enumerare i nodi nella topologia risolta e verificare se questo attributo è presente.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 




