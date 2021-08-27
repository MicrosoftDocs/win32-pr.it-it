---
description: "MF_MT_FSSourceTypeDecoded attributo : specifica se un decodificatore può usare timestamp di decodifica (DTS) durante l'impostazione dei timestamp."
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae25fce343d0c24f7b0a79e2623e7c3e2d0f9272b2f95a825860860ff6f88c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113761"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>Attributo \_ MF MT \_ FSSourceTypeDecoded

Specifica che un tipo di supporto viene decodificato automaticamente.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**


## <a name="remarks"></a>Commenti
Un tipo di supporto è contrassegnato come attributo per indicare che non esiste nell'origine fisica e viene sintetizzato dalla pipeline. Il valore 1 (TRUE) indica che il tipo di supporto è sintetizzato. Il valore 0 (FALSE) o il valore non presente indica che non lo è.

Nella versione corrente questo attributo deve essere specificato usando il valore GUID seguente anziché la MD_MT_FSSourceTypeDecoded costante:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




