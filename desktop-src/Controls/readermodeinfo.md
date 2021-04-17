---
title: Struttura READERMODEINFO
description: Contiene informazioni necessarie per inizializzare la funzione DoReaderMode.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- Controlli di Windows della struttura READERMODEINFO
- Controlli Windows del puntatore alla struttura PREADERMODEINFO
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dacf0fc59ef62447ca12b7a470689e13967d687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477854"
---
# <a name="readermodeinfo-structure"></a>Struttura READERMODEINFO

\[**READERMODEINFO** è supportato tramite Windows XP con Service Pack 2 (SP2). Potrebbe non essere supportata nelle versioni successive.\]

Contiene informazioni necessarie per inizializzare la funzione [**DoReaderMode**](doreadermode.md) .

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Obbligatorio. Dimensioni, in byte, della struttura. Impostare questo parametro su **sizeof (READERMODE)** prima di chiamare [**DoReaderMode**](doreadermode.md).

</dd> <dt>

**HWND**
</dt> <dd>

Tipo: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Obbligatorio. Handle della finestra da utilizzare per la modalità Reader.

</dd> <dt>

**fFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Flag che personalizzano la funzionalità della finestra modalità lettore. Questo parametro può essere 0. in caso contrario, uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                  | Significato                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <dt>**RMF \_**</dt> <dt>0x01</dt> ZEROCURSOR </dl>             | Imposta il cursore al centro dell'area specificata nella **Repubblica popolare cinese**. Se questo flag non è specificato, la posizione del cursore rimane invariata.<br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <dt>**RMF \_**</dt> <dt>0x02</dt> VERTICALONLY </dl>       | Consente solo lo scorrimento verticale.<br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <dt>**RMF \_**</dt> <dt>0x04</dt> HORIZONTALONLY </dl> | Consente solo lo scorrimento orizzontale.<br/>                                                                                                     |



 

</dd> <dt>

**PRC**
</dt> <dd>

Tipo: **lpRect**

</dd> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica l'area di scorrimento nella finestra modalità lettore. Se questo membro è **null**, viene utilizzata l'intera finestra come area di scorrimento.

</dd> <dt>

**pfnScroll**
</dt> <dd>

Tipo: **PFNREADERSCROLL**

</dd> <dd>

Puntatore a una funzione di callback [*ReaderScroll*](readerscroll.md) definita dall'applicazione utilizzata per notificare all'applicazione che è necessario scorrere la finestra in una direzione specifica.

</dd> <dt>

**fFlags**
</dt> <dd>

Tipo: **PFNREADERTRANSLATEDISPATCH**

</dd> <dd>

Puntatore a una funzione di callback [*TranslateDispatch*](translatedispatch.md) definita dall'applicazione utilizzata per ottenere la prima notifica di tutti i messaggi inviati alla finestra modalità lettore.

</dd> <dt>

**lParam**
</dt> <dd>

Tipo: **[ **lParam**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Informazioni aggiuntive necessarie per l'applicazione, lette dal chiamante nella funzione di callback [*ReaderScroll*](readerscroll.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è dichiarata in alcuna intestazione pubblica. Per usarlo, è necessario includere la dichiarazione illustrata in precedenza nella propria intestazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, \[ solo app desktop di Windows Vista\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>          |



 

