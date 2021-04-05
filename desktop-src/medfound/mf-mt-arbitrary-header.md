---
description: Dati specifici del tipo per un flusso binario in un file di formato Advanced Systems (ASF).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: Attributo MF_MT_ARBITRARY_HEADER (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049711"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>\_ \_ Attributo intestazione arbitraria MF mt \_

Dati specifici del tipo per un flusso binario in un file di formato Advanced Systems (ASF).

## <a name="data-type"></a>Tipo di dati

**[**Mt \_ \_Intestazione arbitraria**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** archiviata **come \[ \] byte**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.

## <a name="remarks"></a>Commenti

I file ASF possono contenere flussi con dati binari. L' \_ \_ attributo di intestazione arbitraria MF mt \_ nel tipo di supporto contiene una struttura di [**\_ \_ intestazione mt arbitraria**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) che descrive il flusso.

Oltre all' \_ \_ attributo dell'intestazione arbitraria MF mt \_ , il tipo di supporto per un flusso binario ASF contiene gli attributi seguenti:



| Attributo                                                 | Descrizione                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md) | Il valore dell'attributo è **MFMediaType \_ Binary**. |
| [\_ \_ formato arbitrario MF \_ mt](mf-mt-arbitrary-format.md)   | Contiene dati di formato aggiuntivi.                       |



 

> [!Note]  
> In Windows Media Format SDK i flussi binari sono denominati *flussi arbitrari* o *flussi di dati arbitrari*.

 

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




