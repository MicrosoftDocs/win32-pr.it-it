---
title: Elemento STARTTIME
description: L'elemento STARTTIME definisce un indice temporale dal quale Windows Media Player il rendering del flusso.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- Elemento STARTTIME Windows Media Player
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9138b05b949098c59996c69143059de5cb5b25cafcd8da7d922de120d586b356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568793"
---
# <a name="starttime-element"></a>Elemento STARTTIME

**L'elemento STARTTIME** definisce un indice temporale dal quale Windows Media Player il rendering del flusso.

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attributi

**VALUE** (obbligatorio)

Indice di tempo (in ore, minuti, secondi e centesimi di secondo) da cui Windows Media Player la riproduzione di un flusso definito nell'elemento associato.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **ENTRY**, **REF** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento definisce un indice temporale nel contenuto in cui Windows Media Player avviare il rendering del flusso. Questo elemento può essere usato solo con il contenuto archiviato su richiesta indicizzato.

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

[**Windows Informazioni di riferimento su elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sul metafile multimediale**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





