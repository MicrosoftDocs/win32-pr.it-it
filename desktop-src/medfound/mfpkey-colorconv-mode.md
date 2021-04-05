---
description: Specifica se il flusso di input è interlacciato.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: Proprietà MFPKEY_COLORCONV_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8c01a6dce595eb270b734947492deea014259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755495"
---
# <a name="mfpkey_colorconv_mode-property"></a>\_Proprietà modalità COLORCONV di MFPKEY \_

Specifica se il flusso di input è interlacciato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Calcolato dal DSP dal video di origine.

## <a name="applies-to"></a>Si applica a

-   [Convertitore di colori DSP](colorconverter.md)

## <a name="remarks"></a>Commenti

Usare uno dei valori seguenti.



| Valore | Descrizione |
|-------|-------------|
| 0     | Progressivo |
| 2     | Interlaced  |



 

Se questa proprietà non è impostata, il DSP usa il tipo di supporto di input per determinare se il video è interlacciato. È possibile impostare questa proprietà per sostituire l'impostazione del tipo di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
