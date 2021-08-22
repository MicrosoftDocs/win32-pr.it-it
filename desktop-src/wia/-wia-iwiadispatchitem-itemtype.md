---
description: Tipo di questo elemento. Di sola lettura.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Proprietà Item.ItemType
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
ms.openlocfilehash: 3cbf60c935a88a62786c7c516ec0e768d65019c02d4419c44d928cee704a67b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450781"
---
# <a name="itemitemtype-property"></a>Proprietà Item.ItemType

Tipo di questo elemento. Di sola lettura.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a>Valore proprietà

Sono possibili i valori seguenti:



| Valore  | Descrizione                                     |
|--------|-------------------------------------------------|
| device | L'elemento è un dispositivo hardware WIA.              |
| folder | L'elemento è una cartella che contiene altri elementi. |
| file   | L'elemento è un file di immagine o audio.             |
| Audio  | L'elemento è un clip audio.                      |
| image  | L'elemento è un'immagine.                           |



 

## <a name="remarks"></a>Commenti

Un elemento può avere più di un tipo. Ad esempio, ogni immagine è di entrambi i tipi "image" e "file". **ItemType** restituisce una stringa che include tutti i tipi validi per l'elemento, separati da punti e virgola. Ad esempio, "image;file". In questa stringa non sono presenti spazi e alla fine non è presente un punto e virgola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




