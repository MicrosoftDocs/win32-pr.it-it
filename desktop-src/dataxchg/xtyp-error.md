---
title: Transazione XTYP_ERROR (DDEML. h)
description: Una funzione di callback Dynamic Data Exchange (DDE), DdeCallback, riceve la \_ transazione di errore XTYP quando si verifica un errore critico.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- Scambio di dati delle transazioni XTYP_ERROR
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
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301597"
---
# <a name="xtyp_error-transaction"></a>\_Transazione di errore XTYP

Una funzione di callback Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la transazione di **\_ errore XTYP** quando si verifica un errore critico.


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

Handle per la conversazione associata all'errore. Questo parametro è **null** se l'errore non è associato a una conversazione.

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

Codice di errore nella parola di ordine inferiore. Attualmente, è supportato solo il codice di errore seguente.



| Valore                                                                                                                                                                      | Significato                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <dt>**\_memoria insufficiente DMLERR \_**</dt> </dl> | Memoria insufficiente. è possibile che i dati Advise, poke o Execute vadano persi o che il sistema abbia esito negativo.<br/> |



 

</dd> <dt>

*dwData2* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un'applicazione non può bloccare questo tipo di transazione. il codice restituito del **\_ blocco CBR** viene ignorato. La libreria di gestione Dynamic Data Exchange (DDEML) tenta di liberare memoria rimuovendo le risorse non critiche. Un'applicazione che dispone di conversazioni bloccate dovrebbe sbloccarle.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>DDEML. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica della libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

