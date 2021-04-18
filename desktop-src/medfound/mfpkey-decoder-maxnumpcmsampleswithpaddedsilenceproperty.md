---
description: Specifica il numero massimo di campioni PCM aggiuntivi che potrebbero essere restituiti alla fine di dopo la decodifica di un file.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: Proprietà MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310640"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a>\_Proprietà MaxNumPCMSamplesWithPaddedSilence del decodificatore MFPKEY \_

Specifica il numero massimo di campioni PCM aggiuntivi che potrebbero essere restituiti alla fine di dopo la decodifica di un file.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

2048

## <a name="remarks"></a>Commenti

Questa proprietà può essere usata per stimare il silenzio artificiale che viene inserito tra i brani Man mano che vengono inseriti nel decodificatore uno dopo l'altro.

Per i decodificatori senza perdita di Windows Media Audio 10 Professional e Windows Media Audio 9, questa proprietà è sempre uguale a 0.

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

 

 
