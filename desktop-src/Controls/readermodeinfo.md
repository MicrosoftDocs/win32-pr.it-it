---
title: Struttura READERMODEINFO
description: Contiene le informazioni necessarie per inizializzare la funzione DoReaderMode.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- Struttura READERMODEINFO Windows controlli
- Puntatore alla struttura PREADERMODEINFO Windows controlli
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 510dc7a763d50b42f06b2510e609e0bc7c3c6f31fa1f4c08393964cef75487fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169121"
---
# <a name="readermodeinfo-structure"></a>Struttura READERMODEINFO

\[**READERMODEINFO** è supportato tramite Windows XP con Service Pack 2 (SP2). Potrebbe non essere supportato nelle versioni successive.\]

Contiene le informazioni necessarie per inizializzare [**la funzione DoReaderMode.**](doreadermode.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Obbligatorio. Dimensioni della struttura, in byte. Impostare questo parametro su **sizeof(READERMODE)** prima di chiamare [**DoReaderMode.**](doreadermode.md)

</dd> <dt>

**Hwnd**
</dt> <dd>

Tipo: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Obbligatorio. Handle della finestra da utilizzare per la modalità lettore.

</dd> <dt>

**fFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Flag che personalizzano la funzionalità della finestra in modalità lettore. Questo parametro può essere 0. in caso contrario, uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                  | Significato                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <dt>**RMF \_ ZEROCURSOR**</dt> <dt>0x01</dt> </dl>             | Imposta il cursore al centro dell'area specificata in **prc**. Se questo flag non viene specificato, la posizione del cursore rimane invariata.<br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <dt>**RMF \_ VERTICALONLY**</dt> <dt>0x02</dt> </dl>       | Consente solo lo scorrimento verticale.<br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <dt>**RMF \_ HORIZONTALONLY**</dt> <dt>0x04</dt> </dl> | Consente solo lo scorrimento orizzontale.<br/>                                                                                                     |



 

</dd> <dt>

**Rpc**
</dt> <dd>

Tipo: **LPRECT**

</dd> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che specifica l'area di scorrimento nella finestra della modalità lettore. Se questo membro è **NULL,** come area di scorrimento viene usata l'intera finestra.

</dd> <dt>

**pfnScroll**
</dt> <dd>

Tipo: **PFNREADERSCROLL**

</dd> <dd>

Puntatore a una funzione di callback [*ReaderScroll*](readerscroll.md) definita dall'applicazione usata per notificare all'applicazione che è necessario scorrere la finestra in una direzione specifica.

</dd> <dt>

**fFlags**
</dt> <dd>

Tipo: **PFNREADERTRANSLATEDISPATCH**

</dd> <dd>

Puntatore a una funzione di callback [*TranslateDispatch*](translatedispatch.md) definita dall'applicazione usata per ottenere la prima notifica di tutti i messaggi inviati alla finestra della modalità lettore.

</dd> <dt>

**lParam**
</dt> <dd>

Tipo: **[ **LPARAM**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Informazioni aggiuntive necessarie per l'applicazione, lette dal chiamante nella funzione di callback [*ReaderScroll.*](readerscroll.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è dichiarata in alcuna intestazione pubblica. Per usarlo, è necessario includere la dichiarazione illustrata in precedenza nella propria intestazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows solo \[ app desktop Vista\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>          |



 

