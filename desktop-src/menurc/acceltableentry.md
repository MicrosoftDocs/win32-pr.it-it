---
title: Struttura ACCELTABLEENTRY
description: Descrive i dati in una singola risorsa della tabella dei tasti di scelta rapida. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Menu struttura ACCELTABLEENTRY e altre risorse
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479084"
---
# <a name="acceltableentry-structure"></a>Struttura ACCELTABLEENTRY

Descrive i dati in una singola risorsa della tabella dei tasti di scelta rapida. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

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

Tipo: **Word**

</dd> <dd>

Descrive le caratteristiche del tasto di scelta rapida. Questo membro può avere uno o più dei seguenti valori da winuser. h.



| Valore                                                                                                                                                                                                      | Significato                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <dt>**FVIRTKEY**</dt> <dt>true</dt> </dl>    | Il tasto di scelta rapida è un [codice a chiave virtuale](/windows/desktop/inputdev/virtual-key-codes). Se questo flag non viene specificato, si presuppone che il tasto di scelta rapida specifichi un codice carattere ASCII. <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <dt></dt> <dt>0x02</dt> FNOINVERT </dl> | Una voce di menu sulla barra dei menu non viene evidenziata quando si utilizza un acceleratore. Questo attributo è obsoleto e viene mantenuto solo per compatibilità con le versioni precedenti dei file di risorse progettati per Windows a 16 bit.<br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <dt></dt> <dt>0x04</dt> FSHIFT </dl>          | L'acceleratore viene attivato solo se l'utente preme il tasto MAIUSC. Questo flag è valido solo per le chiavi virtuali. <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <dt></dt> <dt>0x08</dt> FCONTROL </dl>    | L'acceleratore viene attivato solo se l'utente preme il tasto CTRL. Questo flag è valido solo per le chiavi virtuali. <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <dt></dt> <dt>0x10</dt> Falt </dl>                | L'acceleratore viene attivato solo se l'utente preme il tasto ALT. Questo flag è valido solo per le chiavi virtuali. <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <dt>**0x80**</dt> </dl>                                                                          | La voce è l'ultima in una tabella di tasti di scelta rapida. <br/>                                                                                                                                                          |



 

</dd> <dt>

**wAnsi**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Valore del carattere ANSI o codice di chiave virtuale che identifica il tasto di scelta rapida.

</dd> <dt>

**wId**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Identificatore per il tasto di scelta rapida. Si tratta del valore passato alla routine della finestra quando l'utente preme il tasto specificato.

</dd> <dt>

**padding**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Numero di byte inseriti per garantire che la struttura sia allineata a un limite **DWORD** .

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura **ACCELTABLEENTRY** viene ripetuta per tutte le voci della tabella di tasti di scelta rapida nella risorsa. L'ultima voce nella tabella è contrassegnata con il valore 0x0080.

È possibile calcolare il numero di elementi nella tabella se si divide la lunghezza della risorsa di otto. L'applicazione può quindi accedere in modo casuale alle singole voci a lunghezza fissa.

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

 

