---
description: Inviato da un'estensione di File Manager per recuperare informazioni su un file selezionato dalla finestra di Gestione file attiva (finestra della directory o finestra Risultati ricerca).
title: FM_GETFILESEL messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: a801b22fd23b4a67eaf01efbbef574e24a74a2e1304f3a65678c4197517a4a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094186"
---
# <a name="fm_getfilesel-message"></a>Messaggio \_ FM GETFILESEL

Inviato da un'estensione di File Manager per recuperare informazioni su un file selezionato dalla finestra di Gestione file attiva (finestra della directory o finestra Risultati ricerca).

## <a name="parameters"></a>Parametri

<dl> <dt>

*index* 
</dt> <dd>

Indice in base zero del file selezionato da recuperare.

</dd> <dt>

*lpfmsgfs* 
</dt> <dd>

Indirizzo di una [**struttura \_ FMS GETFILESEL**](fms-getfilesel.md) che riceve informazioni sulla selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice in base zero del file selezionato recuperato.

## <a name="remarks"></a>Commenti

Un'estensione può usare il [**messaggio FM \_ GETSELCOUNT**](fm-getselcount.md) per recuperare il numero di file selezionati.

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

[**FM \_ GETFILESELLFN**](fm-getfilesellfn.md)
</dt> <dt>

[**FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md)
</dt> </dl>

 

 




