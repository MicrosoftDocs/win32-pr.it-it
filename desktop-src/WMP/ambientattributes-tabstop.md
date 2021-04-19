---
title: AmbientAttributes. tabStop
description: L'attributo tabStop specifica o recupera un valore che indica se il controllo è nell'ordine di tabulazione. Per impostare l'ordine di tabulazione, inserire il controllo nello script generale prima o dopo altri tag di controllo.
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- Media Player di Windows AmbientAttributes. tabStop
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4005fc26a2bc5f928cde0f5ed67ec2098cf3e6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332146"
---
# <a name="ambientattributestabstop"></a>AmbientAttributes. tabStop

L'attributo **TabStop** specifica o recupera un valore che indica se il controllo è nell'ordine di tabulazione. Per impostare l'ordine di tabulazione, inserire il controllo nello script generale prima o dopo altri tag di controllo.

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | Il controllo è nell'ordine di tabulazione (il controllo avrà una tabulazione: requisito di accessibilità). |
| false | Il controllo non è nell'ordine di tabulazione.                                                       |



 

## <a name="remarks"></a>Commenti

L'attributo **TabStop** non è applicabile all'elemento **Effects** .

Il valore predefinito di questo attributo è true per tutti gli elementi eccetto **menu** e **testo**, il cui valore predefinito è false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





