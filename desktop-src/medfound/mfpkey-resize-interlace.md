---
description: 'MFPKEY_RESIZE_INTERLACE proprietà : specifica se il flusso di input è interlacciato.'
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c614865d0c8a49238b9c8d6f7714787bb22aaadaa317a8a3a0405a7f51c87be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873035"
---
# <a name="mfpkey_resize_interlace-property"></a>Proprietà \_ INTERLACE MFPKEY RESIZE \_

Specifica se il flusso di input è interlacciato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

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



 

Se questa proprietà non è impostata, DSP usa il tipo di supporto di input per determinare se il video è interlacciato. È possibile impostare questa proprietà per eseguire l'override dell'impostazione del tipo di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
