---
description: Rappresenta il tipo di percorso utilizzato come argomento.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: PATH_TYPE enumerazione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c05e71e485eaaf3ff309dc3a0df3d792ccd18c1438964d387afe969adbfd3fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058601"
---
# <a name="path_type-enumeration"></a>Enumerazione PATH \_ TYPE

Rappresenta il tipo di percorso utilizzato come argomento.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="DOS_PATH"></span><span id="dos_path"></span>**PERCORSO \_ DOS**
</dt> <dd>

Percorso standard.

</dd> <dt>

<span id="NT_PATH"></span><span id="nt_path"></span>**NT \_ PATH**
</dt> <dd>

Percorso interno.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




