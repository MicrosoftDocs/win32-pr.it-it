---
title: AmbientAttributes. zIndex
description: L'attributo zIndex specifica o recupera l'ordine in cui viene eseguito il rendering del controllo.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- Media Player Windows AmbientAttributes. zIndex
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331494"
---
# <a name="ambientattributeszindex"></a>AmbientAttributes. zIndex

L'attributo **ZIndex** specifica o recupera l'ordine in cui viene eseguito il rendering del controllo.

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**Long**) con un valore predefinito pari a zero. L'intervallo è quello di un valore long integer con segno.

## <a name="remarks"></a>Commenti

La bitmap di sfondo di  una vista **o di una visualizzazione è** con un indice z fisso pari a zero. Se si vuole che un controllo sia dietro lo sfondo, è necessario impostare **ZIndex** su un numero negativo.

L'indice z di una **vista** o **di una vista è** un indice assoluto, mentre l'indice z di un controllo è relativo all'indice z della **vista** o della **Sottovisualizzazione** che lo contiene.

L'attributo **ZIndex** non è supportato dagli elementi **browser** e **playlist** . Non funzionerà con l'elemento **video** se *video*. senza **finestra** è impostato su false, né con l'elemento **Effects** se **Effects**. **windowed** è impostato su true.

Gli elementi **ButtonElement** utilizzano il **ZIndex** del **ButtonGroup**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





