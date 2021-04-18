---
description: Specifica se il flusso di input è interlacciato.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Proprietà MFPKEY_RESIZE_INTERLACE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a27504bd6da92bc48fee04afc999568a514fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310609"
---
# <a name="mfpkey_resize_interlace-property"></a>MFPKEY \_ Ridimensiona la \_ Proprietà interlacciamento

Specifica se il flusso di input è interlacciato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="applies-to"></a>Si applica a

-   [Ridimensionamento video DSP](videoresizer.md)

## <a name="remarks"></a>Commenti

Usare uno dei valori seguenti:



| Valore     | Descrizione |
|-----------|-------------|
| VT \_ false | Progressivo |
| VT \_ true  | Interlaced  |



 

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

 

 
