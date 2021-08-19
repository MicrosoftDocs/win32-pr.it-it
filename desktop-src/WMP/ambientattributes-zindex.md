---
title: AmbientAttributes.zIndex
description: L'attributo zIndex specifica o recupera l'ordine in cui viene eseguito il rendering del controllo.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- AmbientAttributes.zIndex Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0ebccb050d80371b5865316dd341c8e371d3bfd399d14545b312cf8d265bac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124041"
---
# <a name="ambientattributeszindex"></a>AmbientAttributes.zIndex

**L'attributo zIndex** specifica o recupera l'ordine in cui viene eseguito il rendering del controllo.

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un numero **di** lettura/scrittura (**long**) con un valore predefinito pari a zero. L'intervallo è quello di un oggetto long integer.

## <a name="remarks"></a>Commenti

La bitmap di sfondo di **un oggetto VIEW** o **SUBVIEW** ha un indice z fisso pari a zero. Se si vuole che un controllo sia dietro lo sfondo, **zIndex** deve essere impostato su un numero negativo.

L'indice z di **un** oggetto VIEW o SUBVIEW è un indice assoluto, mentre l'indice z di un controllo è relativo all'indice z dell'oggetto **VIEW** o **SUBVIEW** che lo contiene. 

**L'attributo zIndex** non è supportato dagli elementi **BROWSER** **e PLAYLIST.** Non funzionerà con **l'elemento VIDEO** se *VIDEO*. **windowless è** impostato su false, né con l'elemento **EFFECTS** se **EFFECTS**. **windowed** è impostato su true.

**Gli elementi BUTTONELEMENT** usano **zIndex** dei **relativi ELEMENTI BUTTONGROUP.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





