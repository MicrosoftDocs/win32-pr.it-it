---
description: I valori dei vantaggi definiscono l'ordine in cui Filter Graph Manager tenta di aggiungere filtri durante la compilazione del grafo.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Merito (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a55c112f1a08d63e45d5385f525371ae9642c1b01a1b4af5d7747b042efffe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073015"
---
# <a name="merit"></a>Merito

I valori dei vantaggi definiscono l'ordine in cui Filter Graph Manager tenta di aggiungere filtri durante la compilazione del grafo.

<dl> <span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**LE DUE SIE \_** PREFERRED (0x800000) <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **0X600000) \_ PREFER** (0X800000) <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> 0X600000) 0x400000 **0X200000) \_** 0X200000) <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **\_ \_ \_** <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> 0X100000) **\_ \_** <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **0X100050 \_ \_**
</dl>

## <a name="remarks"></a>Commenti

Ogni filtro viene registrato con un valore di valore . Quando il gestore del grafo dei filtri compila un grafo, enumera tutti i filtri registrati con il tipo di supporto corretto. Quindi li prova in ordine di priorità, dal più alto al più basso. Usa criteri aggiuntivi per scegliere tra filtri con uguale merito. Non prova mai i filtri con un valore di valore inferiore o uguale a **NON \_ \_ USARE \_ .**

Un filtro che non deve mai essere considerato per la riproduzione ordinaria deve avere un'inie'ia **di NON \_ USARE \_ o \_** meno. I filtri possono essere registrati con valori intermedi non definiti da questa enumerazione, ad esempio **NORMAL + \_** 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti e GUID](constants-and-guids.md)
</dt> <dt>

[Linee guida per la registrazione di filtri](guidelines-for-registering-filters.md)
</dt> <dt>

[Gestione Connessione](intelligent-connect.md)
</dt> </dl>

 

 




