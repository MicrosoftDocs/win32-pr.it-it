---
title: Attributo ShadowFilePath
description: L'attributo ShadowFilePath è il percorso completo di un file shadow.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- Attributo ShadowFilePath Windows Media Player
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf1e8f2eb5cb810004ea219aac62973377111902071beb78eca051df19877f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002151"
---
# <a name="shadowfilepath-attribute"></a>Attributo ShadowFilePath

**L'attributo ShadowFilePath** è il percorso completo di un file shadow.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)

## <a name="remarks"></a>Commenti

Un *file shadow viene* creato come parte di una conversione del formato di file. È la copia di un file che il lettore usa quando l'utente sincronizza il contenuto dal computer a un dispositivo che richiede che il contenuto sia nel formato di file originale. Questo attributo è impostato perché il file convertito punti al percorso del file shadow.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni sul processo di conversione**](about-the-conversion-process.md)
</dt> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> </dl>

 

 





