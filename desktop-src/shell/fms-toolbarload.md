---
description: Contiene informazioni sui pulsanti personalizzati da aggiungere alla barra degli strumenti di gestione file. I pulsanti sono forniti da una DLL di estensione di file Manager.
title: Struttura FMS_TOOLBARLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 8e123c759a827adddf5fd00eaf33193ebca0dbf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979695"
---
# <a name="fms_toolbarload-structure"></a>\_Struttura TOOLBARLOAD FMS

Contiene informazioni sui pulsanti personalizzati da aggiungere alla barra degli strumenti di gestione file. I pulsanti sono forniti da una DLL di estensione di file Manager.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a>Members

<dl> <dt>

**dwSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensione, in byte, della struttura. Gestione file imposta le dimensioni prima di chiamare l'estensione e controlla le dimensioni dopo la restituzione della procedura di estensione.

</dd> <dt>

**lpButtons**
</dt> <dd>

Tipo: **LPEXT \_ Button**

</dd> <dd>

Indirizzo di una matrice di strutture [**di \_ pulsanti EXT**](ext-button.md) .

</dd> <dt>

**cButtons**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Numero di strutture [**di \_ pulsanti EXT**](ext-button.md) nella matrice a cui punta il membro **lpButtons** . Questo numero è uguale al numero di pulsanti e separatori da aggiungere alla barra degli strumenti.

</dd> <dt>

**cBitmaps**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Numero di pulsanti rappresentati dalla bitmap specificata.

</dd> <dt>

**idBitmap**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Identificatore di una risorsa bitmap nel file eseguibile per la DLL di estensione. La risorsa bitmap contiene immagini per il numero di pulsanti specificato da **cBitmaps**. Gestione file carica la risorsa bitmap e la usa per visualizzare i pulsanti.

</dd> <dt>

**hBitmap**
</dt> <dd>

Tipo: **HBITMAP**

</dd> <dd>

Handle per una bitmap che verrà utilizzata da Gestione file per ottenere e visualizzare le immagini del pulsante se **idBitmap** è 0.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TOOLBARLOAD FMEVENT**](fmevent-toolbarload.md)
</dt> </dl>

 

 




