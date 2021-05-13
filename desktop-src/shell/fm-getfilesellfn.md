---
description: Inviato da un'estensione di File Manager per recuperare informazioni su un file selezionato dalla finestra di Gestione file attiva (la finestra della directory o la finestra Risultati ricerca). Il file selezionato può avere un nome file lungo.
title: FM_GETFILESELLFN messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: e991d2705f74aa8822dcef89878e9762f22b08dc
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842392"
---
# <a name="fm_getfilesellfn-message"></a>Messaggio \_ FM GETFILESELLFN

Inviato da un'estensione di File Manager per recuperare informazioni su un file selezionato dalla finestra di Gestione file attiva (la finestra della directory o la finestra Risultati ricerca). Il file selezionato può avere un nome file lungo.

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

Solo le estensioni che supportano nomi di file lunghi ( ad esempio, estensioni che supportano la rete) devono usare questo messaggio.

Un'estensione può usare [**il messaggio FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md) per recuperare il conteggio dei file selezionati.

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

[**FM \_ GETFILESEL**](fm-getfilesel.md)
</dt> <dt>

[**FM \_ GETSELCOUNT**](fm-getselcount.md)
</dt> </dl>

 

 




