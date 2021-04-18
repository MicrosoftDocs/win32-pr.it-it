---
title: Elemento ButtonTip
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento ButtonTip
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- Finestra elementi ButtonTip Media Player
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ab94794232ade6f924b87fd3f4d73d4452d544
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324836"
---
# <a name="buttontip-element"></a>Elemento ButtonTip

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'elemento **ButtonTip** specifica la stringa di testo visualizzata quando l'utente fa riferimento a un pulsante del riquadro attività.

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
| Elementi padre | **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |
| Elementi figlio  | nessuno                                                 |



 

## <a name="remarks"></a>Osservazioni

Questo elemento è facoltativo per ogni istanza di **ServiceTask1**, **ServiceTask2** o **ServiceTask3**. Se questo elemento non viene specificato, Windows Media Player usa il testo del pulsante come valore predefinito.

> [!Note]  
> Windows Media Player 10 include tre riquadri attività in cui un negozio online può visualizzare le pagine Web. Lo Store online può scegliere di usare uno, due o tutti e tre i riquadri attività. Windows Media Player 11 dispone di un solo riquadro attività, che l'utente può visualizzare facendo clic sulla scheda **Store online** . Windows Media Player 11 ignora gli elementi **ServiceTask2** e **ServiceTask3** .

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





