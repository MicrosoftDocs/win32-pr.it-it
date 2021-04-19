---
title: EQUALIZERSETTINGS.gainLevels
description: L'attributo gainLevels specifica o Recupera il livello di guadagno della banda corrispondente all'indice fornito.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- Media Player Windows EQUALIZERSETTINGS. gainLevels
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326130"
---
# <a name="equalizersettingsgainlevels"></a>EQUALIZERSETTINGS.gainLevels

L'attributo **gainLevels** specifica o Recupera il livello di guadagno della banda corrispondente all'indice fornito.

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore normalmente compreso tra 20 e + 20.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*
</dt> <dd>

**Numero**(**Long**) compreso tra 1 e 10 che indica l'indice della banda.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo attributo accetta un parametro, ma il relativo valore viene specificato nel codice di script allo stesso modo degli altri valori di attributo. Non può essere specificato nell'elemento EQUALIZERSETTINGS, né può essere usato con l'attributo di ascolto **wmpprop** . Al contrario, vengono forniti gli attributi a livello di guadagno numerato per queste situazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**Attributi di ascolto**](listening-attributes.md)
</dt> </dl>

 

 





