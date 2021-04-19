---
title: Elemento Description
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Description (elemento)
ms.assetid: 4d9ff447-e5a4-46b1-b599-87202077abfb
keywords:
- Elemento Description Media Player Windows
topic_type:
- apiref
api_name:
- Description Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4318a7936f4713d3ff89a2fa73731eea0cdd97db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326023"
---
# <a name="description-element"></a>Elemento Description

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'elemento **Description** specifica una descrizione di marketing dello Store online visualizzata durante la prima esperienza dell'utente con un'installazione di Windows Media Player.

``` syntax
<Description>
    text string
</Description>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

La lunghezza della descrizione deve essere minore o uguale a 255 caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





