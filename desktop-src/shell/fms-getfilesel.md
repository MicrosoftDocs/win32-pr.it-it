---
description: Contiene informazioni su un file selezionato nella finestra attiva di File Manager (la finestra della directory o la finestra Risultati ricerca).
title: FMS_GETFILESEL struttura (Wfext.h)
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
ms.openlocfilehash: b1188840299a101081c5c29d0e5658963ca7a72e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842222"
---
# <a name="fms_getfilesel-structure"></a>Struttura \_ FMS GETFILESEL

Contiene informazioni su un file selezionato nella finestra di Gestione file attiva (la finestra della directory o la finestra Risultati ricerca).

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

Tipo: **FILETIME**

</dd> <dd>

Ora e data di creazione del file.

</dd> <dt>

**dwSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensione, in byte, del file.

</dd> <dt>

**bAttr**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Attributi del file.

</dd> <dt>

**Szname**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

Percorso completo con terminazione Null e nome file del file selezionato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




