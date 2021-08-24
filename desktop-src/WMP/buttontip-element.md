---
title: Elemento ButtonTip
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. | Elemento ButtonTip
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- Elemento ButtonTip Windows Media Player
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7fb4a162a8e77fea7548265825af6c6cbda75dbafadf05fe32cb664c4d563f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764301"
---
# <a name="buttontip-element"></a>Elemento ButtonTip

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

**L'elemento ButtonTip** specifica la stringa di testo visualizzata quando l'utente punta a un pulsante del riquadro attività.

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento                                              |
|-----------------|------------------------------------------------------|
| Elementi padre | **ServiceTask1,** **ServiceTask2,** **ServiceTask3** |
| Elementi figlio  | nessuno                                                 |



 

## <a name="remarks"></a>Osservazioni

Questo elemento è facoltativo per ogni istanza di **ServiceTask1,** **ServiceTask2** o **ServiceTask3.** Se questo elemento non viene fornito, Windows Media Player il testo del pulsante come valore predefinito.

> [!Note]  
> Windows Media Player 10 include tre riquadri attività in cui un negozio online può visualizzare le pagine Web. Lo Store online può scegliere di usare uno, due o tutti e tre i riquadri attività. Windows Media Player 11 ha un solo riquadro attività, che l'utente può visualizzare facendo clic sulla scheda **Negozi** online. Windows Media Player 11 ignora gli elementi **ServiceTask2** e **ServiceTask3.**

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





