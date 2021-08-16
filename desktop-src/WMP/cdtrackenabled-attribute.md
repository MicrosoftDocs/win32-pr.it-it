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
ms.openlocfilehash: 8a86c94c2c1b44327cdbfb35544c3e0b5b34d25885215d78dbec0ec084d056e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342684"
---
# <a name="cdtrackenabled-attribute"></a>Attributo CDTrackEnabled

**L'attributo CDTrackEnabled** indica se la traccia è abilitata per la riproduzione.

## <a name="applies-to"></a>Si applica a

-   [Tracce CD](cd-track-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato solo nella cache della libreria.

Quando si riproduce un CD in Windows Media Player, l'utente può selezionare una traccia e specificare che non deve essere riprodotta. Questo valore di questo attributo è True se la traccia può essere riprodotta oppure False se l'utente ha specificato che la traccia non deve essere riprodotta.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





