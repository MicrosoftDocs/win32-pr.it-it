---
title: Enumerazione ResultsDisplayStyle
description: Usato da IResultsViewer ResultsStyle per impostare o determinare la modalità di visualizzazione dei risultati.
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- Enumerazione ResultsDisplayStyle Funzionalità dell'ambiente Windows legacy
topic_type:
- apiref
api_name:
- ResultsDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a045765b53f29e978c286a14a1d82b86ffb21b5046dee606029a957ee0434c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726527"
---
# <a name="resultsdisplaystyle-enumeration"></a>Enumerazione ResultsDisplayStyle

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Usato da [**IResultsViewer::ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) per impostare o determinare la modalità di visualizzazione dei risultati.

## <a name="syntax"></a>Sintassi


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**
</dt> <dd>

Indica che i risultati vengono visualizzati come icone piccole.

</dd> <dt>

<span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**
</dt> <dd>

Indica che i risultati vengono visualizzati come icone grandi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>WdsView.idl</dt> </dl> |



 

 





