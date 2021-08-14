---
title: Struttura dei codici di errore COM
description: Struttura dei codici di errore COM
ms.assetid: 97e68708-eb62-4481-af03-cf8b80304103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65953582952ce076028ffcf6652e46356c4cf2afacdd088d546c2fdaafd18a33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104024"
---
# <a name="structure-of-com-error-codes"></a>Struttura dei codici di errore COM

La figura seguente mostra il formato di [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a) (o SCODE). i numeri indicano le posizioni in bit:

![Mostra il formato di 'H RESULT' o 'S CODE' con numeri che indicano posizioni di bit.](images/a5a947d1-7b5a-4474-afed-2a1c58fe2421.png)

Il bit di ordine elevato in **HRESULT** o SCODE indica se il valore restituito rappresenta l'esito positivo o negativo. Se impostato su 0, SEVERITY \_ SUCCESS, il valore indica l'esito positivo. Se impostato su 1, SEVERITY \_ ERROR, indica un errore.

I bit R, C, N e r sono riservati.

Il campo della struttura indica il servizio di sistema responsabile dell'errore. Microsoft alloca nuovi codici di struttura non appena diventano necessari. La maggior parte dei valori **SCODE e HRESULT** imposta il campo della struttura su FACILITY \_ ITF, che indica un errore del metodo di interfaccia.

I campi di funzionalità comuni sono descritti nella tabella seguente.



| Campo Della struttura                | Valore        | Descrizione                                                                                                                                                                                                                                                                                                              |
|-------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FACILITY \_ DISPATCH<br/> | 2<br/> | Per gli errori **dell'interfaccia IDispatch ad** associazione tardiva. <br/>                                                                                                                                                                                                                                                             |
| FACILITY \_ ITF<br/>      | 4<br/> | Per la maggior parte dei codici di stato restituiti dai metodi di interfaccia. Il significato effettivo dell'errore è definito dall'interfaccia . Ovvero, due **HRESULT** con esattamente lo stesso valore a 32 bit restituito da due interfacce diverse potrebbero avere significati diversi. <br/>                                                       |
| FACILITY \_ NULL<br/>     | 0<br/> | Per codici di stato comuni ampiamente applicabili, ad esempio S \_ OK. <br/>                                                                                                                                                                                                                                                    |
| RPC DI \_ FACILITY<br/>      | 1<br/> | Per i codici di stato restituiti dalle chiamate di procedura remota. <br/>                                                                                                                                                                                                                                                       |
| ARCHIVIAZIONE \_ DELLE STRUTTURE<br/>  | 3<br/> | Per i codici di stato [**restituiti dalle chiamate al**](/windows/desktop/api/objidl/nn-objidl-istorage) metodo IStorage o [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) relative all'archiviazione strutturata. I codici di stato il cui valore di codice (inferiore a 16 bit) è compreso nell'intervallo di codici di errore MS-DOS (ovvero minori di 256) hanno lo stesso significato dell'errore MS-DOS corrispondente. <br/> |
| FUNZIONALITÀ \_ WIN32<br/>    | 7<br/> | Usato per fornire un mezzo per gestire i codici di errore dalle funzioni nell'API Windows come **HRESULT.** Anche i codici di errore in OLE a 16 bit che hanno duplicato i codici di errore di sistema sono stati modificati in FACILITY \_ WIN32. <br/>                                                                                                 |
| FINESTRE DELLE \_ STRUTTURE<br/>  | 8<br/> | Usato per codici di errore aggiuntivi da interfacce definite da Microsoft.<br/>                                                                                                                                                                                                                                            |



 

Il campo del codice è un numero univoco assegnato a rappresentare l'errore o l'avviso.

Per convenzione, **i valori HRESULT** hanno in genere nomi nel formato seguente: *Facility* \_ *Severity* \_ *Reason*.

*Facility* è il nome della struttura o un altro identificatore di distinzione. *La gravità* è una singola lettera, S o E, che indica se la chiamata di funzione ha avuto esito positivo (S) o ha generato un errore (E); e *Reason* è un identificatore che descrive il significato del codice. Ad esempio, il codice di stato STG E FILENOTFOUND indica che si è verificato un errore correlato all'archiviazione. In particolare, un \_ file richiesto non \_ esiste. I codici di stato di FACILITY \_ NULL omettono *il prefisso facility.* \_

I codici di errore sono definiti nel contesto di un'implementazione dell'interfaccia. Una volta definiti, i codici di esito positivo non possono essere modificati o aggiunti nuovi codici di esito positivo. È tuttavia possibile scrivere nuovi codici di errore. Microsoft si riserva il diritto di definire nuovi codici di errore (ma non codici di esito positivo) per le interfacce descritte in FACILITY \_ ITF o in nuove strutture.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](error-handling-in-com.md)
</dt> <dt>

[Windows Protocolli: HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)
</dt> </dl>

 

