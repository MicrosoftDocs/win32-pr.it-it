---
description: 'MFPKEY_RESIZE_INTERLACE proprietà : specifica se il flusso di input è interlacciato.'
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d0efe93901a08322a05dbed2515f76b04a214b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092879"
---
# <a name="mfpkey_resize_interlace-property"></a>Proprietà \_ INTERLACE MFPKEY RESIZE \_

Specifica se il flusso di input è interlacciato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ BOOL

## <a name="applies-to"></a>Si applica a

-   [DSP di Ridimensionamento video](videoresizer.md)

## <a name="remarks"></a>Commenti

Usare uno dei valori seguenti:



| Valore     | Descrizione |
|-----------|-------------|
| VT \_ FALSE | Progressivo |
| VT \_ TRUE  | Interlaced  |



 

Se questa proprietà non è impostata, il DSP usa il tipo di supporto di input per determinare se il video è interlacciato. È possibile impostare questa proprietà per eseguire l'override dell'impostazione del tipo di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
