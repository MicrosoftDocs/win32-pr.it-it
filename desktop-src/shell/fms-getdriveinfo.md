---
description: Contiene informazioni sull'unità selezionata nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).
title: Struttura FMS_GETDRIVEINFO (Wfext. h)
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
ms.openlocfilehash: b19b54d89f74fa122effa5853beb2961e0ddf1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979698"
---
# <a name="fms_getdriveinfo-structure"></a>\_Struttura GETDRIVEINFO FMS

Contiene informazioni sull'unità selezionata nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).

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

percorso con terminazione null della directory corrente.

</dd> <dt>

**szVolume**
</dt> <dd>

Tipo: **TCHAR \[ 14 \]**

</dd> <dd>

Etichetta del volume con terminazione null del disco associato all'unità.

</dd> <dt>

**szShare**
</dt> <dd>

Tipo: **TCHAR \[ 128 \]**

</dd> <dd>

Nome con terminazione null della risorsa di rete (se l'unità è accessibile tramite una rete).

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
</dt> <dt>

[**\_GETDRIVEINFO FM**](fm-getdriveinfo.md)
</dt> </dl>

 

 




