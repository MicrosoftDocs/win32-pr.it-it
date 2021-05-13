---
description: Contiene informazioni sull'unità selezionata nella finestra di Gestione file attiva (la finestra della directory o la finestra Risultati ricerca).
title: FMS_GETDRIVEINFO (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: 107e12e1076a2fc928ecb9b578ab01d64898a83a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842232"
---
# <a name="fms_getdriveinfo-structure"></a>Struttura \_ FMS GETDRIVEINFO

Contiene informazioni sull'unità selezionata nella finestra di Gestione file attiva (la finestra della directory o la finestra Risultati ricerca).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**dwTotalSpace**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Quantità totale di spazio di archiviazione, in byte, sul disco associato all'unità.

</dd> <dt>

**dwFreeSpace**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Quantità di spazio di archiviazione disponibile, in byte, sul disco associato all'unità.

</dd> <dt>

**szPath**
</dt> <dd>

Tipo: **TCHAR \[ 260 \]**

</dd> <dd>

Percorso con terminazione Null della directory corrente.

</dd> <dt>

**szVolume**
</dt> <dd>

Tipo: **TCHAR \[ 14 \]**

</dd> <dd>

Etichetta del volume con terminazione Null del disco associato all'unità.

</dd> <dt>

**szShare**
</dt> <dd>

Tipo: **TCHAR \[ 128 \]**

</dd> <dd>

Nome con terminazione Null della risorsa di rete (se l'accesso all'unità avviene tramite una rete).

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
</dt> <dt>

[**FM \_ GETDRIVEINFO**](fm-getdriveinfo.md)
</dt> </dl>

 

 




