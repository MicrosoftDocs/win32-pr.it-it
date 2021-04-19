---
title: STARTTIME (elemento)
description: L'elemento STARTTIME definisce un indice temporale da cui Windows Media Player avvierà il rendering del flusso.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- Elemento STARTTIME Media Player Windows
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326296"
---
# <a name="starttime-element"></a>STARTTIME (elemento)

L'elemento **StartTime** definisce un indice temporale da cui Windows Media Player avvierà il rendering del flusso.

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attributi

**Valore** (obbligatorio)

Indice temporale (in ore, minuti, secondi e centesimi di secondo) dal quale Windows Media Player avvia la riproduzione di un flusso definito nell'elemento associato.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **voce**, **ref** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento definisce un indice temporale nel contenuto in cui Windows Media Player deve avviare il rendering del flusso. Questo elemento può essere usato solo con contenuto archiviato su richiesta che è stato indicizzato.

## <a name="examples"></a>Esempio


```XML
<STARTTIME VALUE="1:30.0" />
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------|
| Versione<br/> | Windows Media Player versione 70 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





