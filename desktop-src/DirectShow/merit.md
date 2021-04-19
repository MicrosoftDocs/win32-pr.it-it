---
description: I valori di Merit definiscono l'ordine in cui il gestore del grafico del filtro tenta di aggiungere filtri durante la compilazione del grafo.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Merit (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323989"
---
# <a name="merit"></a>Merito

I valori di Merit definiscono l'ordine in cui il gestore del grafico del filtro tenta di aggiungere filtri durante la compilazione del grafo.

<dl> <span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>Il **merito \_ Preferenza** (0x800000) <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **Merit \_ Normal** (0x600000) Merit <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **\_ improbabile** (0x400000) <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **Merit non \_ \_ \_ use** (0x200000) <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **Merit \_ SW \_** Compressor (0x100000) <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **Merit \_ HW \_ Compressor** (0x100050)
</dl>

## <a name="remarks"></a>Commenti

Ogni filtro viene registrato con un valore Merit. Quando il gestore del grafico dei filtri compila un grafo, enumera tutti i filtri registrati con il tipo di supporto corretto. Quindi, le tentano in ordine di merito, dal più alto al più basso. Usa criteri aggiuntivi per scegliere tra i filtri con uguale Merit. Non tenta mai i filtri con un valore Merit minore o uguale a **Merit \_ non \_ \_ usare**.

Un filtro che non deve mai essere considerato per la riproduzione ordinaria deve avere un merito di **merito non \_ \_ \_ usare** o meno. I filtri possono essere registrati con valori intermedi non definiti da questa enumerazione, ad esempio **Merit \_ Normal** + 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti e GUID](constants-and-guids.md)
</dt> <dt>

[Linee guida per la registrazione dei filtri](guidelines-for-registering-filters.md)
</dt> <dt>

[Connessione intelligente](intelligent-connect.md)
</dt> </dl>

 

 




