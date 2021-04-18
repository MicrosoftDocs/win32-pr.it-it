---
description: GuidNames è una matrice globale nella libreria di classi base DirectShow che contiene le stringhe che rappresentano i GUID definiti in UUIDs. h. Questa matrice è utile per la generazione dell'output di debug.
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: GuidNames (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328167"
---
# <a name="guidnames"></a>GuidNames

`GuidNames` è una matrice globale nella libreria di classi base DirectShow che contiene stringhe che rappresentano i GUID definiti in UUIDs. h. Questa matrice è utile per la generazione dell'output di debug.

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="guid"></span><span id="GUID"></span>*GUID*
</dt> <dd>

Specifica qualsiasi valore GUID definito nel file di intestazione UUIDs. h.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare questa matrice globale per restituire costanti GUID come stringhe. Il codice seguente, ad esempio, stampa la stringa "MEDIATYPE \_ video" nella console:


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



Se il GUID non corrisponde, viene restituita la stringa "nome GUID sconosciuto". Non tutti i GUID DirectShow sono definiti in UUIDs. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 




