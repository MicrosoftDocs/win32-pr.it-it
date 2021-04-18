---
description: Tipo di questo elemento. Di sola lettura.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Proprietà Item. ItemType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9b70f7a1698ecdb4de023786f21a6ef9d55f681d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312408"
---
# <a name="itemitemtype-property"></a>Proprietà Item. ItemType

Tipo di questo elemento. Di sola lettura.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a>Valore proprietà

Sono possibili i seguenti valori:



| Valore  | Descrizione                                     |
|--------|-------------------------------------------------|
| device | L'elemento è un dispositivo hardware WIA.              |
| folder | L'elemento è una cartella che contiene altri elementi. |
| file   | L'elemento è un'immagine o un file audio.             |
| Audio  | L'elemento è un clip audio.                      |
| image  | L'elemento è un'immagine.                           |



 

## <a name="remarks"></a>Commenti

Un elemento può avere più di un tipo. Ogni immagine, ad esempio, è di tipo "image" e "file". **ItemType** restituisce una stringa che include tutti i tipi validi per l'elemento, separati da punti e virgola. Ad esempio, "image; file". Non sono presenti spazi in questa stringa e non è presente un punto e virgola alla fine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




