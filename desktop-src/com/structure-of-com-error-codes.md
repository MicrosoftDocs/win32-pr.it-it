---
title: Struttura dei codici di errore COM
description: Struttura dei codici di errore COM
ms.assetid: 97e68708-eb62-4481-af03-cf8b80304103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb27143f50028592f6fe0aeb5cab9795dcd10d4a
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104558632"
---
# <a name="structure-of-com-error-codes"></a>Struttura dei codici di errore COM

Nella figura seguente viene illustrato il formato di un valore [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a) (o SCODE); i numeri indicano le posizioni dei bit:

![Mostra il formato di "risultato H" o "codice" con i numeri che indicano le posizioni dei bit.](images/a5a947d1-7b5a-4474-afed-2a1c58fe2421.png)

Il bit più significativo in **HRESULT** o SCODE indica se il valore restituito rappresenta l'esito positivo o negativo. Se impostato su 0, la gravità ha \_ esito positivo, il valore indica l'esito positivo. Se impostato su 1, errore di gravità indica un errore \_ .

I bit R, C, N e r sono riservati.

Il campo della struttura indica il servizio di sistema responsabile dell'errore. Microsoft alloca nuovi codici di struttura quando diventano necessari. La maggior parte dei valori SCODE e **HRESULT** imposta il campo della struttura su struttura \_ ITF, che indica un errore del metodo di interfaccia.

I campi della funzionalità comuni sono descritti nella tabella seguente.



| Campo della struttura                | Valore        | Descrizione                                                                                                                                                                                                                                                                                                              |
|-------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| distribuzione della struttura \_<br/> | 2<br/> | Per gli errori dell'interfaccia **IDispatch** con associazione tardiva. <br/>                                                                                                                                                                                                                                                             |
| FUNZIONALITÀ \_ ITF<br/>      | 4<br/> | Per la maggior parte dei codici di stato restituiti dai metodi di interfaccia. Il significato effettivo dell'errore è definito dall'interfaccia. Ovvero, due **HRESULT** s con esattamente lo stesso valore a 32 bit restituito da due interfacce diverse possono avere significati diversi. <br/>                                                       |
| FUNZIONE \_ null<br/>     | 0<br/> | Per i codici di stato comuni applicabili a livello generale, ad esempio S \_ OK. <br/>                                                                                                                                                                                                                                                    |
| RPC di struttura \_<br/>      | 1<br/> | Per i codici di stato restituiti dalle chiamate a procedure remote. <br/>                                                                                                                                                                                                                                                       |
| archiviazione di strutture \_<br/>  | 3<br/> | Per i codici di stato restituiti dalle chiamate al metodo [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) correlate all'archiviazione strutturata. I codici di stato il cui valore (inferiore a 16 bit) è compreso nell'intervallo dei codici di errore MS-DOS, ovvero minori di 256, hanno lo stesso significato dell'errore MS-DOS corrispondente. <br/> |
| Win32 della struttura \_<br/>    | 7<br/> | Utilizzato per fornire un metodo per gestire i codici di errore dalle funzioni nell'API Windows come valore **HRESULT**. I codici di errore in OLE a 16 bit che hanno duplicato i codici di errore di sistema sono stati modificati anche in Win32 della struttura \_ . <br/>                                                                                                 |
| finestre di struttura \_<br/>  | 8<br/> | Utilizzato per ulteriori codici di errore dalle interfacce definite da Microsoft.<br/>                                                                                                                                                                                                                                            |



 

Il campo del codice è un numero univoco assegnato per rappresentare l'errore o l'avviso.

Per convenzione, i valori **HRESULT** hanno in genere nomi nel formato seguente: motivo della gravità della *struttura* \_  \_ .

La *struttura* è il nome della struttura o un altro identificatore di distinzione; Il livello di *gravità* è una singola lettera, S o E, che indica se la chiamata di funzione ha avuto esito positivo o ha generato un errore (E); e *reason* è un identificatore che descrive il significato del codice. Il codice di stato STG \_ E FileNotFound indica ad esempio che \_ si è verificato un errore relativo all'archiviazione. in particolare, non esiste un file richiesto. I codici di stato della funzionalità \_ null omettono il prefisso della *funzionalità* \_ .

I codici di errore sono definiti all'interno del contesto di un'implementazione dell'interfaccia. Una volta definito, i codici di esito positivo non possono essere modificati o nuovi codici di riuscita aggiunti. Tuttavia, è possibile scrivere nuovi codici di errore. Microsoft si riserva il diritto di definire nuovi codici di errore (ma non codici di esito positivo) per le interfacce descritte in funzionalità \_ ITF o in nuove strutture.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](error-handling-in-com.md)
</dt> <dt>

[Protocolli di Windows: HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)
</dt> </dl>

 

