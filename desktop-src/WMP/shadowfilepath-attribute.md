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
ms.openlocfilehash: ef79271995e9817315fb918049fc22491e232a5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327365"
---
# <a name="shadowfilepath-attribute"></a>Attributo ShadowFilePath

L'attributo **ShadowFilePath** è il percorso completo di un file shadow.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)

## <a name="remarks"></a>Commenti

Un *file shadow* viene creato come parte di una conversione del formato di file. Si tratta della copia di un file usato dal giocatore quando l'utente Sincronizza il contenuto dal computer a un dispositivo che richiede che il contenuto sia nel formato di file originale. Questo attributo è impostato per il file convertito in modo che punti al percorso del file shadow.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni sul processo di conversione**](about-the-conversion-process.md)
</dt> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





