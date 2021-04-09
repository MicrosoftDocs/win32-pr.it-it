---
description: Specifica le dimensioni della sezione in unità di megabyte (MB), bits o MB di riga.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: Proprietà CODECAPI_AVEncSliceControlSize (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4c3e58fa34922941ea564d42e449cefd798ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127978"
---
# <a name="codecapi_avencslicecontrolsize-property"></a>Proprietà AVEncSliceControlSize di codecapi \_

Specifica le dimensioni della sezione in unità di megabyte (MB), bits o MB di riga.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncSliceControlSize**

## <a name="remarks"></a>Commenti

**Codificatori H. 264/AVC:**

Il significato del valore di codecapis \_ AVEncSliceControlSize è controllato dalla proprietà [codecapis \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) . La tabella seguente illustra il modo in cui le \_ Proprietà codecapi AVEncSliceControlSize e codecapi \_ AVEncSliceControlMode controllano le dimensioni e il numero di sezioni in un frame.



| Impostazione AVEncSliceControlMode codecapit \_ | Significato del valore                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                       | Si tratta di un numero intero che indica le dimensioni di ogni sezione del frame in unità di macroblocchi. <br/> Il codificatore deve rifiutare l'impostazione quando il valore è maggiore del numero di macroblocchi nel frame.<br/>                                                                                                                                                                         |
| 1                                       | Si tratta di un numero intero che indica le dimensioni di ogni sezione del frame in unità di bit. <br/> Il codificatore deve avviare una nuova sezione in macroblocco che fa sì che il numero di bit nella sezione superi questo valore (pertanto le dimensioni di ogni sezione saranno sempre minori o uguali a questo valore). Ciò significa che le dimensioni dell'ultima sezione potrebbero essere notevolmente inferiori rispetto a questo valore. <br/> |
| 2                                       | Si tratta di un numero intero che indica le dimensioni di ogni sezione del frame in unità di macroblocco righe. <br/> Il codificatore deve rifiutare l'impostazione quando il valore è maggiore del numero di righe macroblocco nel frame.<br/>                                                                                                                                                                 |



 

Se l'applicazione non imposta un valore per [CODEcapis \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), il codificatore deve restituire un errore.

Il valore predefinito consigliato consiste nel disporre di una singola sezione per intero frame.

Alcuni codificatori potrebbero codificare le sezioni in parallelo e pertanto le prestazioni potrebbero essere influenzate a seconda delle impostazioni di controllo delle sezioni. Ad esempio, la codifica di un frame come una singola sezione potrebbe essere più lenta rispetto a quando il frame è stato codificato come più sezioni.

Le impostazioni di controllo sezione sono dinamiche e possono essere modificate durante la sessione di codifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                   |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




