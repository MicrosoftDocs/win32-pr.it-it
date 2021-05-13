---
description: Contiene informazioni sui pulsanti personalizzati da aggiungere alla barra degli strumenti di File Manager. I pulsanti sono forniti da una DLL di estensione di File Manager.
title: FMS_TOOLBARLOAD (Wfext.h)
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
ms.openlocfilehash: 3a993312b9e365561018459c43dab87afbd3c2b2
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842162"
---
# <a name="fms_toolbarload-structure"></a>Struttura TOOLBARLOAD DI FMS \_

Contiene informazioni sui pulsanti personalizzati da aggiungere alla barra degli strumenti di File Manager. I pulsanti sono forniti da una DLL di estensione di File Manager.

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

Dimensione, in byte, della struttura . File Manager imposta le dimensioni prima di chiamare l'estensione e controlla le dimensioni al termine della procedura di estensione.

</dd> <dt>

**lpButtons**
</dt> <dd>

Tipo: **PULSANTE \_ LPEXT**

</dd> <dd>

Indirizzo di una matrice di [**strutture BUTTON \_ EXT.**](ext-button.md)

</dd> <dt>

**cButtons**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Numero di [**strutture EXT \_ BUTTON**](ext-button.md) nella matrice a cui punta il **membro lpButtons.** Questo numero è uguale al numero di pulsanti e separatori da aggiungere alla barra degli strumenti.

</dd> <dt>

**cBitmaps**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Numero di pulsanti rappresentati dalla bitmap specificata.

</dd> <dt>

**idBitmap**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Identificatore di una risorsa bitmap nel file eseguibile per la DLL di estensione. La risorsa bitmap contiene immagini per il numero di pulsanti specificato da **cBitmaps**. File Manager carica la risorsa bitmap e la usa per visualizzare i pulsanti.

</dd> <dt>

**Hbitmap**
</dt> <dd>

Tipo: **HBITMAP**

</dd> <dd>

Handle di una bitmap che File Manager userà per ottenere e visualizzare le immagini dei pulsanti se **idBitmap** è 0.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BARRA DEGLI STRUMENTI \_ FMEVENTLOAD**](fmevent-toolbarload.md)
</dt> </dl>

 

 




