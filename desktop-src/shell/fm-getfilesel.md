---
description: Inviato da un'estensione di File Manager per recuperare le informazioni su un file selezionato dalla finestra di Gestione file attiva (nella finestra della directory o nella finestra Risultati ricerca).
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
ms.openlocfilehash: 2da95a39f8e84215640e926ae21a043865223665
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841422"
---
# <a name="fm_getfilesel-message"></a>Messaggio \_ FM GETFILESEL

Inviato da un'estensione di File Manager per recuperare le informazioni su un file selezionato dalla finestra di Gestione file attiva (nella finestra della directory o nella finestra Risultati ricerca).

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

Un'estensione può usare il [**messaggio FM \_ GETSELCOUNT**](fm-getselcount.md) per recuperare il conteggio dei file selezionati.

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

 

 




