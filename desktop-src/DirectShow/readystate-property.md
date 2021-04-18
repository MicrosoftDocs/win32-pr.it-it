---
description: La proprietà ReadyState Recupera il ReadyState dell'oggetto MSWebDVD.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: Proprietà ReadyState (ocidl. h)
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
ms.openlocfilehash: a52b20349c58e8bd44458266da6a0a33ea149c98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326989"
---
# <a name="readystate-property"></a>Proprietà ReadyState

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `ReadyState` proprietà recupera il readyState dell'oggetto **mswebdvd** .

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il ReadyState del controllo.



| Codice restituito | Descrizione                                               |
|-------------|-----------------------------------------------------------|
| 0           | Stato di inizializzazione predefinito.                             |
| 1           | È in corso il caricamento delle proprietà dell'oggetto.                         |
| 2           | L'oggetto è stato inizializzato.                              |
| 3           | L'oggetto è interattivo, ma non tutti i relativi dati sono disponibili. |
| 4           | L'oggetto ha ricevuto tutti i dati.                         |



 

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura e non prevede alcun valore predefinito.

Qualsiasi oggetto incorporato in una pagina Web espone la `ReadyState` Proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Ocidl. h</dt> </dl> |



 

 




