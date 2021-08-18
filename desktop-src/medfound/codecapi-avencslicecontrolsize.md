---
description: Specifica le dimensioni della sezione in unità di megabyte (MB), bit o MB di riga.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: CODECAPI_AVEncSliceControlSize proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d068d8b2c5fc15fdb82c3ffe068e6926d28228a19367114067e02ebc44b03726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035349"
---
# <a name="codecapi_avencslicecontrolsize-property"></a>CODECAPI \_ AVEncSliceControlSize - proprietà

Specifica le dimensioni della sezione in unità di megabyte (MB), bit o MB di riga.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncSliceControlSize**

## <a name="remarks"></a>Commenti

**Codificatori H.264/AVC:**

Il significato del valore di CODECAPI \_ AVEncSliceControlSize è controllato dalla [proprietà CODECAPI \_ AVEncSliceControlMode.](codecapi-avencslicecontrolmode.md) La tabella seguente illustra come le proprietà CODECAPI \_ AVEncSliceControlSize e CODECAPI AVEncSliceControlMode controllano le dimensioni e il numero di sezioni in un \_ frame.



| Impostazione CODECAPI \_ AVEncSliceControlMode | Significato del valore                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                       | Numero intero che indica le dimensioni di ogni sezione nel frame in unità di blocco di macro. <br/> Il codificatore deve rifiutare l'impostazione quando il valore è maggiore del numero di blocchi macro nel frame.<br/>                                                                                                                                                                         |
| 1                                       | Numero intero che indica le dimensioni di ogni sezione nel frame in unità di bit. <br/> Il codificatore deve avviare una nuova sezione in corrispondenza del macroblock che fa in modo che il numero di bit nella sezione superi questo valore , quindi le dimensioni di ogni sezione saranno sempre minori o uguali a questo valore. Ciò significa che le dimensioni dell'ultima sezione potrebbero essere notevolmente inferiori rispetto a questo valore. <br/> |
| 2                                       | Numero intero che indica le dimensioni di ogni sezione nel frame in unità di righe del blocco macro. <br/> Il codificatore deve rifiutare l'impostazione quando il valore è maggiore del numero di righe del blocco macro nel frame.<br/>                                                                                                                                                                 |



 

Se l'applicazione non imposta un valore per [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), il codificatore deve restituire un errore.

L'impostazione predefinita consigliata è avere una singola sezione per l'intero frame.

Alcuni codificatori potrebbero codificare le sezioni in parallelo e quindi le prestazioni potrebbero essere influenzate a seconda delle impostazioni di controllo delle sezioni. Ad esempio, la codifica di un frame come singola sezione potrebbe essere più lenta rispetto a quando il frame è stato codificato come più sezioni.

Le impostazioni del controllo sezione sono dinamiche e possono essere modificate durante la sessione di codifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                   |
| Server minimo supportato<br/> | Windows Server 2012 App desktop R2 \[ \| per app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




