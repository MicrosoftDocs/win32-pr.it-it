---
description: Contiene informazioni utilizzate da Gestione file per aggiungere un menu personalizzato fornito da una DLL di estensione di File Manager. La struttura fornisce anche un valore delta che la DLL di estensione può usare per modificare il menu personalizzato dopo che File Manager ha caricato il menu.
title: FMS_LOAD struttura (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: efd1777704c775db84c7dabf54b9e06c81535fb4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842192"
---
# <a name="fms_load-structure"></a>Struttura FMS \_ LOAD

Contiene informazioni utilizzate da Gestione file per aggiungere un menu personalizzato fornito da una DLL di estensione di File Manager. La struttura fornisce anche un valore delta che la DLL di estensione può usare per modificare il menu personalizzato dopo che File Manager ha caricato il menu.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a>Members

<dl> <dt>

**dwSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Lunghezza, in byte, della struttura .

</dd> <dt>

**szMenuName**
</dt> <dd>

Tipo: **TCHAR \[ MENU TEXT \_ \_ LEN \]**

</dd> <dd>

Nome con terminazione Null per una voce di menu visualizzata sulla barra dei menu in File Manager.

</dd> <dt>

**Hmenu**
</dt> <dd>

Tipo: **HMENU**

</dd> <dd>

Identificatore del menu a comparsa aggiunto alla barra dei menu in File Manager.

</dd> <dt>

**wMenuDelta**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

Valore delta della voce di menu. Per evitare conflitti con le proprie voci di menu, File Manager rinumera gli identificatori delle voci di menu nel menu a comparsa identificato dal membro **hMenu** aggiungendo questo valore delta a ogni identificatore. Una DLL di estensione che deve modificare una voce di menu deve identificare la voce aggiungendo il valore delta all'identificatore della voce di menu. Il valore di questo membro può variare da sessione a sessione.

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

 

 




