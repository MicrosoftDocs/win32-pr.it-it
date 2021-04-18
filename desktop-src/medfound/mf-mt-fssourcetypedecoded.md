---
description: Specifica se un decodificatore può utilizzare i timestamp di decodifica (DTS) quando si configurano i timestamp.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ad80b0b7b29677ed0bee2f86a2c12c56c08441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319607"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>\_Attributo MF mt \_ FSSourceTypeDecoded

Specifica che un tipo di supporto è decodificato automaticamente.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**


## <a name="remarks"></a>Commenti
Un tipo di supporto è contrassegnato come un attributo per indicare che non esiste nell'origine fisica ed è sintetizzato dalla pipeline. Il valore 1 (TRUE) indica che il tipo di supporto è sintetizzato. Il valore 0 (FALSE) o il valore non presente indica che non lo è.

Nella versione corrente, questo attributo deve essere specificato usando il valore GUID seguente anziché la costante MD_MT_FSSourceTypeDecoded:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




