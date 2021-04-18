---
description: Il messaggio NEWCALL della riga TSPI \_ viene inviato alla funzione di callback LineEvent ogni volta che una nuova chiamata non originata da TAPI arriva su una riga aperta da TAPI.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: Messaggio LINE_NEWCALL (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3e7380b2f328283e5f5cad9e84f5a1d0c450dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327987"
---
# <a name="line_newcall-message"></a>\_Messaggio linea NEWCALL

Il messaggio **\_ NEWCALL della riga** TSPI viene inviato alla funzione di callback [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) ogni volta che una nuova chiamata non originata da TAPI arriva su una riga aperta da TAPI. Deve essere il primo messaggio inviato in merito a tale chiamata. TAPI scrive l'handle opaco *htCall* nella posizione passata dal provider di servizi come *dwParam2*. Ciò consente al provider di servizi di usare il valore *htCall* nei messaggi successivi.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*htLine* 
</dt> <dd>

Handle di oggetto opaco TAPI al dispositivo della linea.

</dd> <dt>

*htCall* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwMsg* 
</dt> <dd>

RIGA del valore \_ NEWCALL.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Handle opaco del provider di servizi per la chiamata di tipo [**HDRVCALL**](hdrvline.md). TAPI passa questo valore come parametro *hdCall* per identificare la chiamata nelle procedure successive richiamate per operare sulla chiamata.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Puntatore di tipo LPHTAPICALL che punta a un [**HTAPICALL**](htapicall.md). TAPI scrive l'handle opaco TAPI per la chiamata alla posizione indicata. Il provider di servizi deve salvare questo valore e passarlo come parametro *htCall* per identificare la chiamata negli eventi successivi segnalati per la chiamata.

Questo parametro può inoltre acquisire un valore **null** (vedere la sezione Osservazioni riportata di seguito).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il provider di servizi deve inviare il messaggio di [**riga \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) come messaggio successivo per questa chiamata. L'evento **line \_ NEWCALL** è insolito in quanto restituisce anche un valore al provider di servizi.

Questa funzione segnala le nuove chiamate che hanno origine nel provider di servizi (in ingresso, in uscita, avviate al telefono e così via) per cui TAPI e il provider di servizi non hanno ancora scambiato gli handle opachi. Gli handle vengono scambiati in modo che TAPI e il provider di servizi possano successivamente effettuare richieste ed eventi di report che coinvolgono la chiamata. Poiché queste nuove chiamate non sono necessariamente in ingresso, le chiamate possono essere inizialmente in qualsiasi stato, non necessariamente lo stato dell' *offerta* . Se il provider di servizi viene avviato e rileva che una o più chiamate sono già attive sulla riga, informa TAPI con messaggi di **riga \_ NEWCALL** seguiti dai messaggi della [**riga \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) che indicano lo stato corrente. Una nuova chiamata in uscita, avviata dal telefono da parte dell'utente, verrebbe segnalata con un messaggio di **riga \_ NEWCALL** e il messaggio di **riga iniziale \_ CALLSTATE** indicherebbe che la chiamata era in stato **Dialtone** (e quindi continua da qui).

Se il provider di servizi passa un numero elevato di chiamate a TAPI in un intervallo di tempo molto breve (durante lo stesso ciclo di interrupt), è possibile che TAPI venga sottoposta a backlog nell'elaborazione di tali chiamate. Quando si verifica questo problema, TAPI segnala al provider di servizi di attendere un breve periodo di tempo prima di inviare ulteriori chiamate. Segnala questo problema scrivendo un valore **null**, anziché un [**HTAPICALL**](htapicall.md)valido, nella posizione a cui punta il parametro *dwParam2* della **riga \_ NEWCALL**. Ciò indica che il tentativo di elaborare l'handle di chiamata appena offerto non è stato eseguito correttamente, probabilmente a causa di un'impossibilità temporanea di allocare memoria. Il provider di servizi può rispondere eliminando la chiamata o inviando di nuovo il messaggio di **riga \_ NEWCALL** dopo un ritardo di pianificazione (durante il quale il provider di servizi deve cedere il processore per consentire a TAPI di elaborare altre azioni in sospeso). In ogni caso, nessun altro messaggio relativo alla nuova chiamata può essere passato a TAPI fino a quando lo scambio di handle non riesce. Quando la posizione a cui punta *dwParam2* acquisisce un valore non **null** , il provider di servizi sa che questo valore è un handle [**HTAPICALL**](htapicall.md) valido per la chiamata.

Al livello TAPI non è associato alcun messaggio direttamente corrispondente. Questo messaggio viene usato a livello di TSPI per introdurre in modo univoco e senza ambiguità una nuova chiamata in ingresso a TAPI e recuperare l'identificatore opaco TAPI per la chiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEA \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

