---
description: Contiene informazioni su un file selezionato nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).
title: Struttura FMS_GETFILESEL (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: e7ae92350e88e050b1208eed6e08f8faba811fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966396"
---
# <a name="fms_getfilesel-structure"></a>\_Struttura GETFILESEL FMS

Contiene informazioni su un file selezionato nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a>Members

<dl> <dt>

**ftTime**
</dt> <dd>

Tipo: **FILEtime**

</dd> <dd>

Data e ora di creazione del file.

</dd> <dt>

**dwSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensione, in byte, del file.

</dd> <dt>

**bAttr**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Attributi del file.

</dd> <dt>

**szName**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

Il percorso completo con terminazione null e il nome del file selezionato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




