---
title: Attributo CDTrackEnabled
description: L'attributo CDTrackEnabled indica se la traccia è abilitata per la riproduzione.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- Attributo CDTrackEnabled Windows Media Player
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333129"
---
# <a name="cdtrackenabled-attribute"></a>Attributo CDTrackEnabled

L'attributo **CDTrackEnabled** indica se la traccia è abilitata per la riproduzione.

## <a name="applies-to"></a>Si applica a

-   [Tracce CD](cd-track-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato solo nella cache della libreria.

Quando si riproduce un CD in Windows Media Player, l'utente può selezionare una traccia e specificare che non deve essere riprodotta. Questo valore di questo attributo è true se la traccia può essere riprodotta oppure false se l'utente ha specificato che la traccia non deve essere riprodotta.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





