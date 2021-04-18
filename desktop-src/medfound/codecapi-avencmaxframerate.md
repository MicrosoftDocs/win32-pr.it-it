---
description: Imposta la frequenza massima di input in tempo reale dei fotogrammi video che vengono inseriti nel codificatore.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: Proprietà CODECAPI_AVEncMaxFrameRate (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c04d1fd1297f299db133cd98bd493c968fcc29c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305497"
---
# <a name="codecapi_avencmaxframerate-property"></a>Proprietà AVEncMaxFrameRate di codecapi \_

Imposta la frequenza massima di input in tempo reale dei fotogrammi video che vengono inseriti nel codificatore.

## <a name="data-type"></a>Tipo di dati

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncMaxFrameRate**

## <a name="remarks"></a>Commenti

Questa proprietà consente al chiamante di specificare la frequenza massima di input in tempo reale dei fotogrammi video inviati al codificatore. In questo modo, il codificatore indica la velocità di elaborazione dei frame in arrivo. Questa operazione è utile per i codificatori che si configurano in una particolare configurazione dello stato di alimentazione in base alla risoluzione e alla frequenza dei fotogrammi del video di origine.

La frequenza dei fotogrammi è espressa come rapporto. I 32 bit superiori del valore dell'attributo contengono il numeratore e i 32 bit inferiori contengono il denominatore. Se, ad esempio, la frequenza dei fotogrammi è di 30 fotogrammi al secondo (fps), il rapporto è 30/1. Se la frequenza dei fotogrammi è 29,97 fps, il rapporto è 30000/1001.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

