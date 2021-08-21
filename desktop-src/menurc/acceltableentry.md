---
title: Struttura ACCELTABLEENTRY
description: Descrive i dati in una singola risorsa tabella dei tasti di scelta rapida. La definizione della struttura fornita qui è solo a solo supporto della spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Struttura ACCELTABLEENTRY Menu e altre risorse
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ef163c8473c049d3bbe6fbfa8b36876765bf07df0b26cd1d68d3f92c5d315f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972130"
---
# <a name="acceltableentry-structure"></a>Struttura ACCELTABLEENTRY

Descrive i dati in una singola risorsa tabella dei tasti di scelta rapida. La definizione della struttura fornita qui è solo a solo supporto della spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a>Members

<dl> <dt>

**fFlags**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Descrive le caratteristiche dei tasti di scelta rapida. Questo membro può avere uno o più dei valori seguenti da Winuser.h.



| Valore                                                                                                                                                                                                      | Significato                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <dt>**FVIRTKEY**</dt> <dt>TRUE</dt> </dl>    | Il tasto di scelta rapida è [un codice di tasto virtuale](/windows/desktop/inputdev/virtual-key-codes). Se questo flag non viene specificato, si presuppone che il tasto di scelta rapida specifica un codice carattere ASCII. <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <dt>**FNOINVERT**</dt> <dt>0x02</dt> </dl> | Una voce di menu sulla barra dei menu non viene evidenziata quando si usa un tasto di scelta rapida. Questo attributo è obsoleto e viene mantenuto solo per garantire la compatibilità con le versioni precedenti dei file di risorse progettati per le versioni Windows.<br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <dt>**FSHIFT**</dt> <dt>0x04</dt> </dl>          | L'acceleratore viene attivato solo se l'utente preme MAIUSC. Questo flag si applica solo alle chiavi virtuali. <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <dt>**FCONTROL**</dt> <dt>0x08</dt> </dl>    | L'acceleratore viene attivato solo se l'utente preme CTRL. Questo flag si applica solo alle chiavi virtuali. <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <dt>**FaLT**</dt> <dt>0x10</dt> </dl>                | L'acceleratore viene attivato solo se l'utente preme ALT. Questo flag si applica solo alle chiavi virtuali. <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <dt>**0x80**</dt> </dl>                                                                          | La voce è l'ultima in una tabella dei tasti di scelta rapida. <br/>                                                                                                                                                          |



 

</dd> <dt>

**wAnsi**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Valore di carattere ANSI o codice di tasto virtuale che identifica il tasto di scelta rapida.

</dd> <dt>

**Wid**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Identificatore del tasto di scelta rapida. Si tratta del valore passato alla routine della finestra quando l'utente preme il tasto specificato.

</dd> <dt>

**padding**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Numero di byte inseriti per garantire che la struttura sia allineata su un **limite DWORD.**

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura ACCELTABLEENTRY** viene ripetuta per tutte le voci della tabella dei tasti di scelta rapida nella risorsa. L'ultima voce nella tabella è contrassegnata con il valore 0x0080.

È possibile calcolare il numero di elementi nella tabella se si divide la lunghezza della risorsa per otto. L'applicazione può quindi accedere in modo casuale alle singole voci a lunghezza fissa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> </dl>

 

