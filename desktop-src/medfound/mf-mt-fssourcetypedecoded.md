---
description: "MF_MT_FSSourceTypeDecoded attributo : specifica se un decodificatore può usare timestamp di decodifica (DTS) durante l'impostazione dei timestamp."
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3799c11e3b921427ff4a3b05aa3d7f47e297ba14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093089"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>Attributo MF \_ MT \_ FSSourceTypeDecoded

Specifica che un tipo di supporto viene decodificato automaticamente.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**


## <a name="remarks"></a>Commenti
Un tipo di supporto è contrassegnato come attributo per indicare che non esiste nell'origine fisica ed è sintetizzato dalla pipeline. Il valore 1 (TRUE) indica che il tipo di supporto è sintetizzato. Il valore 0 (FALSE) o il valore non presente indica che non lo è.

Nella versione corrente questo attributo deve essere specificato usando il valore GUID seguente anziché la costante MD_MT_FSSourceTypeDecoded seguente:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 app \[ desktop \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 \[ \| per app UWP\]<br/>                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




