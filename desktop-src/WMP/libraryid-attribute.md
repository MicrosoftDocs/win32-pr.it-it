---
title: Attributo IDLibreria
description: L'attributo IDLibreria è l'identificatore della libreria a cui appartiene l'elemento.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- Attributo IDLibreria Windows Media Player
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ae9e5ad097bc188b8de1e76a09448c57aa9b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327771"
---
# <a name="libraryid-attribute"></a>Attributo IDLibreria

L'attributo **IDLibreria** è l'identificatore della libreria a cui appartiene l'elemento.

## <a name="applies-to"></a>Si applica a

-   [**Elementi audio**](audio-item-attributes.md)
-   [**Elementi foto**](photo-item-attributes.md)
-   [**Elementi della playlist**](playlist-attributes-ref.md)
-   [**Elementi video**](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Un elemento multimediale può appartenere alla libreria locale dell'utente corrente oppure può appartenere a una libreria resa disponibile da un altro utente nella rete domestica o in Internet.

Il valore di questo attributo corrisponde al valore restituito dal metodo [**IWMPLibrary2:: GetItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





