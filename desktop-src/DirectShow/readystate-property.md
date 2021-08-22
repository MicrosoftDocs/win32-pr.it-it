---
description: La proprietà ReadyState recupera l'elemento ReadyState dell'oggetto MSWebDVD.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: Proprietà ReadyState (Ocidl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: 029798e66d8ed69dc18bbb23dafc8b047d770f1bc91ac1b86ca7bdb09963c2e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072785"
---
# <a name="readystate-property"></a>Proprietà ReadyState

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `ReadyState` proprietà recupera l'elemento ReadyState **dell'oggetto MSWebDVD.**

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta l'elemento ReadyState del controllo.



| Codice restituito | Descrizione                                               |
|-------------|-----------------------------------------------------------|
| 0           | Stato di inizializzazione predefinito.                             |
| 1           | L'oggetto sta caricando le relative proprietà.                         |
| 2           | L'oggetto è stato inizializzato.                              |
| 3           | L'oggetto è interattivo, ma non tutti i relativi dati sono disponibili. |
| 4           | L'oggetto ha ricevuto tutti i dati.                         |



 

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura senza alcun valore predefinito.

Qualsiasi oggetto incorporato in una pagina Web espone la `ReadyState` proprietà .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Ocidl.h</dt> </dl> |



 

 




