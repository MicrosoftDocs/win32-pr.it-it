---
description: Il messaggio TSPI LINE NEWCALL viene inviato alla funzione di callback LINEEVENT ogni volta che una nuova chiamata non originata da TAPI arriva in una riga aperta \_ da TAPI.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: LINE_NEWCALL messaggio (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f541f7535e9b41dc66a83b8d033d3ff7adf4d51f6e78f275d2695cb5ae7a35b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761907"
---
# <a name="line_newcall-message"></a>LINE \_ NEWCALL message

Il messaggio TSPI **LINE \_ NEWCALL** viene inviato alla funzione di callback [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) ogni volta che una nuova chiamata non originata da TAPI arriva in una riga aperta da TAPI. Deve trattarsi del primo messaggio inviato relativo a tale chiamata. TAPI scrive *l'handle* opaco htCall nella posizione passata dal provider di servizi *come dwParam2.* In questo modo al provider di servizi viene restituito il valore *htCall* da usare nei messaggi successivi.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*htLine* 
</dt> <dd>

Handle dell'oggetto opaco TAPI per il dispositivo linea.

</dd> <dt>

*htCall* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwMsg* 
</dt> <dd>

Valore LINE \_ NEWCALL.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Handle opaco del provider di servizi per la chiamata, di [**tipo HDRVCALL**](hdrvline.md). TAPI passa questo valore come *parametro hdCall* per identificare la chiamata nelle procedure successive richiamate per operare sulla chiamata.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Puntatore di tipo LPHTAPICALL che punta a [**HTAPICALL.**](htapicall.md) TAPI scrive l'handle opaco TAPI per la chiamata nella posizione indicata. Il provider di servizi deve salvare questo valore e passarlo come parametro *htCall* per identificare la chiamata negli eventi successivi che segnala per la chiamata.

Questo parametro può anche acquisire un **valore NULL** (vedere la sezione Osservazioni seguente).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il provider di servizi deve inviare [**il \_ messaggio LINE CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) come messaggio successivo per questa chiamata. **L'evento LINE \_ NEWCALL** è insolito perché passa anche un valore al provider di servizi.

Questa funzione segnala le nuove chiamate che hanno origine nel provider di servizi (in ingresso, in uscita, avviate al telefono e così via) per le quali TAPI e il provider di servizi non hanno ancora scambiato handle opachi. Gli handle vengono s scambiati in modo che TAPI e il provider di servizi possano successivamente effettuare richieste e segnalare eventi che coinvolgono la chiamata. Poiché queste nuove chiamate non sono necessariamente in ingresso, le chiamate possono inizialmente essere in qualsiasi stato, non necessariamente lo *stato dell'offerta.* Se il provider di servizi viene avviato e rileva che una o più chiamate sono già attive nella riga, ne informa TAPI con messaggi **LINE \_ NEWCALL** seguiti da messaggi [**LINE \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) che indicano lo stato corrente. Una nuova chiamata in uscita, avviata al telefono dall'utente, verrebbe segnalata con un messaggio **LINE \_ NEWCALL** e il messaggio **LINE \_ CALLSTATE** iniziale indicherebbe che la chiamata era nello stato **DIALTONE** (e quindi continua da qui).

Se il provider di servizi passa un numero elevato di chiamate a TAPI in un periodo di tempo molto breve (durante lo stesso ciclo di interrupt), TAPI può diventare backlogged nell'elaborazione di tali chiamate. In questo caso, TAPI segnala al provider di servizi di attendere un breve periodo di tempo prima di inviare altre chiamate. Segnala questo problema scrivendo un valore **NULL,** anziché un [**HTAPICALL valido,**](htapicall.md)nella posizione a cui punta *il parametro dwParam2* di **LINE \_ NEWCALL.** Ciò indica che il tentativo di elaborare l'handle di chiamata appena offerto non è riuscito, probabilmente a causa dell'impossibilità temporanea di allocare memoria. Il provider di servizi può rispondere eliminando la chiamata o inviando nuovamente il messaggio **LINE \_ NEWCALL** dopo un ritardo di pianificazione (durante il quale il provider di servizi deve cedere il processore per consentire a TAPI di elaborare altre azioni in sospeso). In ogni caso, non è possibile passare altri messaggi relativi alla nuova chiamata a TAPI fino a quando lo scambio di handle ha esito positivo. Quando la posizione a cui *punta dwParam2* acquisisce un valore non **NULL,** il provider di servizi sa che questo valore è un handle [**HTAPICALL**](htapicall.md) valido per la chiamata.

Non è presente alcun messaggio direttamente corrispondente a livello TAPI. Questo messaggio viene usato a livello di TSPI per introdurre in modo univoco e non ambiguo una nuova chiamata in ingresso a TAPI e recuperare l'identificatore opaco TAPI per la chiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

