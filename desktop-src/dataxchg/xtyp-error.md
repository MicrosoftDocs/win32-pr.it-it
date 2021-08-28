---
title: XTYP_ERROR transazione (Ddeml.h)
description: Una Dynamic Data Exchange callback DDE (DDE), DdeCallback, riceve la transazione ERROR XTYP quando \_ si verifica un errore critico.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- XTYP_ERROR di dati della transazione Exchange
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce59800723758201b4857b5a3ae0844675347b2d4fd403c77650b36d9275bfb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755981"
---
# <a name="xtyp_error-transaction"></a>Transazione ERROR \_ XTYP

Una Dynamic Data Exchange callback DDE [*(DDE), DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)riceve la transazione **ERROR XTYP \_** quando si verifica un errore critico.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uType* 
</dt> <dd>

Tipo di transazione.

</dd> <dt>

*uFmt* 
</dt> <dd>

Non usato.

</dd> <dt>

*hconv* 
</dt> <dd>

Handle per la conversazione associata all'errore. Questo parametro è **NULL** se l'errore non è associato a una conversazione.

</dd> <dt>

*hsz1* 
</dt> <dd>

Non usato.

</dd> <dt>

*hsz2* 
</dt> <dd>

Non usato.

</dd> <dt>

*hdata* 
</dt> <dd>

Non usato.

</dd> <dt>

*dwData1* 
</dt> <dd>

Codice di errore nella parola di ordine più basso. Attualmente è supportato solo il codice di errore seguente.



| Valore                                                                                                                                                                      | Significato                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <dt>**MEMORIA INSUFFICIENTE \_ DMLERR \_**</dt> </dl> | Memoria insufficiente. consigliare, eseguire o eseguire i dati potrebbero essere persi o il sistema potrebbe non riuscire.<br/> |



 

</dd> <dt>

*dwData2* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un'applicazione non può bloccare questo tipo di transazione. Il **codice restituito da CBR \_ BLOCK** viene ignorato. La Dynamic Data Exchange DDEML (Dynamic Data Exchange Management Library) tenta di liberare memoria rimuovendo le risorse non critiche. Un'applicazione che ha bloccato le conversazioni deve sbloccarle.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Ddeml.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Dynamic Data Exchange panoramica della libreria di gestione di Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

