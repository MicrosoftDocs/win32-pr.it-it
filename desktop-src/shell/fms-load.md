---
description: Contiene informazioni utilizzate da Gestione file per aggiungere un menu personalizzato fornito da una DLL di estensione di file Manager. La struttura fornisce inoltre un valore Delta che può essere utilizzato dalla DLL di estensione per modificare il menu personalizzato dopo che il menu è stato caricato da file Manager.
title: Struttura FMS_LOAD (Wfext. h)
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
ms.openlocfilehash: 1745c4e34ac124e9990602350db6479ce287be8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977087"
---
# <a name="fms_load-structure"></a>\_Struttura di caricamento FMS

Contiene informazioni utilizzate da Gestione file per aggiungere un menu personalizzato fornito da una DLL di estensione di file Manager. La struttura fornisce inoltre un valore Delta che può essere utilizzato dalla DLL di estensione per modificare il menu personalizzato dopo che il menu è stato caricato da file Manager.

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

Lunghezza, in byte, della struttura.

</dd> <dt>

**szMenuName**
</dt> <dd>

Tipo: **TCHAR \[ il \_ testo del menu \_ \] Len**

</dd> <dd>

Nome con terminazione null per una voce di menu visualizzata sulla barra dei menu in gestione file.

</dd> <dt>

**hMenu**
</dt> <dd>

Tipo: **HMENU**

</dd> <dd>

Identificatore del menu popup aggiunto alla barra dei menu in gestione file.

</dd> <dt>

**wMenuDelta**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

Valore delta della voce di menu. Per evitare conflitti con le proprie voci di menu, gestione file consente di rinumerare gli identificatori delle voci di menu nel menu popup identificato dal membro **HMENU** aggiungendo questo valore Delta a ogni identificatore. Una DLL di estensione che deve modificare una voce di menu deve identificare l'elemento aggiungendo il valore delta all'identificatore della voce di menu. Il valore di questo membro può variare da sessione a sessione.

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

 

 




