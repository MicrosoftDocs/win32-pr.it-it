---
description: Rappresenta il tipo di percorso usato come argomento.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: Enumerazione PATH_TYPE
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
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522953"
---
# <a name="path_type-enumeration"></a>Enumerazione del tipo di percorso \_

Rappresenta il tipo di percorso usato come argomento.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="DOS_PATH"></span><span id="dos_path"></span>**\_percorso DOS**
</dt> <dd>

Percorso standard.

</dd> <dt>

<span id="NT_PATH"></span><span id="nt_path"></span>**\_percorso NT**
</dt> <dd>

Percorso interno.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




