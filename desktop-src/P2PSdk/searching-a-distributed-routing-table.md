---
description: Prima che un'applicazione possa eseguire ricerche nella tabella di routing distribuita (DRT), è necessario creare una query di ricerca.
ms.assetid: b3403a64-128c-461e-9384-8e62c03322e1
title: Ricerca in una tabella di routing distribuita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9977ca395393cef09198182fb8790738d2b00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315441"
---
# <a name="searching-a-distributed-routing-table"></a>Ricerca in una tabella di routing distribuita

Prima che un'applicazione possa eseguire ricerche nella tabella di routing distribuita (DRT), è necessario creare una query di ricerca. Il valore della chiave desiderata viene specificato dall'applicazione quando viene chiamata la funzione [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) . Il comportamento della ricerca è determinato dalle informazioni specificate dall'applicazione nella struttura delle [**informazioni di \_ ricerca \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .

In genere, un evento dell'applicazione viene segnalato quando la ricerca individua i risultati e un altro al termine della ricerca. Tuttavia, se **fIterative** è impostato in [**DRT \_ Search \_ info**](/windows/desktop/api/drt/ns-drt-drt_search_info), un evento dell'applicazione può essere segnalato quando viene eseguito un contatto con ogni nodo lungo il percorso.

Dopo la segnalazione di un evento, l'applicazione chiama la funzione [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) per i risultati. Se il codice restituito è **\_ OK**, i risultati vengono puntati nella struttura dei [**\_ \_ risultati di ricerca DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) restituita dall'API. I risultati restituiti rientrano nell'intervallo di valori specificato [**nelle \_ \_ informazioni di ricerca DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info). Nel caso in cui la ricerca non rilevi corrispondenze, solo **DRT \_ E non verrà restituito \_ alcun \_** valore alla fine dei risultati restituiti.

Le informazioni seguenti illustrano in dettaglio come i membri contenuti nelle [**\_ \_ informazioni di ricerca di DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) consentono a un'applicazione di determinare in modo specifico il comportamento di ricerca dell'infrastruttura DRT:

## <a name="fallowcurrentinstancematch"></a>fAllowCurrentInstanceMatch

Per impostazione predefinita, i risultati della ricerca di DRT includono solo corrispondenze rilevate all'esterno del nodo locale. L'impostazione di **fAllowCurrentInstanceMatch** specifica che nei risultati della ricerca sono incluse anche le corrispondenze rilevate nell'istanza locale di DRT.

## <a name="cmaxendpoints"></a>cMaxEndpoints

La quantità e l'intervallo dei risultati restituiti dalla ricerca sono specificati dall'applicazione con i valori **cMaxEndpoints** (Quantity) e **pMinimumKey** e **pMaximumKey** (intervallo), a cui fanno riferimento le [**\_ \_ informazioni di ricerca DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info).

Quando **cMaxEndpoints = 1**, l'infrastruttura DRT cerca una chiave, restituendo una corrispondenza nell'intervallo specificato dai valori **pMinimumKey** e **pMaximumKey** in [**DRT \_ Search \_ info**](/windows/desktop/api/drt/ns-drt-drt_search_info). Questa corrispondenza può essere una corrispondenza esatta o la corrispondenza più vicina nell'intervallo. Se non viene trovata alcuna corrispondenza, viene restituito **DRT \_ E \_ \_** .

Se **cMaxEndpoints > 1**, l'infrastruttura DRT restituirà corrispondenze comprese nell'intervallo fino al valore di **cMaxEndpoints**. Le corrispondenze restituite possono contenere una corrispondenza esatta o i risultati della corrispondenza più vicina nell'intervallo. Inoltre, se **pMinimumKey** e **pMaximumKey** sono impostati sullo stesso valore, una ricerca viene eseguita solo per tale valore, restituendo **DRT \_ e \_ non \_ più** se non viene trovato.

## <a name="fanymatchinrange"></a>fAnyMatchInRange

Il membro **fAnyMatchInRange** indica se la ricerca viene interrotta dopo che la prima corrispondenza si trova nell'intervallo specificato o se la ricerca continuerà per la corrispondenza più vicina alla chiave specificata nell'API [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) . Quando **fAnyMatchInRange** è impostato, la ricerca viene eseguita con **cMaxEndpoints = 1** indipendentemente dal valore specificato di **cMaxEndpoints** in [**DRT \_ Search \_ info**](/windows/desktop/api/drt/ns-drt-drt_search_info).

## <a name="fiterative"></a>fIterative

Il membro **fIterative** specifica se a ogni nodo contattato dall'infrastruttura DRT durante la ricerca sono associati i dati chiave/endpoint resi disponibili per l'applicazione tramite il [**\_ \_ risultato della ricerca DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result). Impostando **fIterative** su **true**, il valore di **cMaxEndpoints = 1** verrà forzato. Quando **fIterative** è impostato su **true** in una query di ricerca per DRT, l'applicazione viene richiamata dopo il contatto con ogni nodo o "hop". Ogni risultato dell'hop contiene una chiave che indica il nodo che verrà ricercato da DRT. Il risultato di un hop viene restituito tramite [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) come risultato **\_ \_ intermedio corrispondente a DRT** .

## <a name="pminimumkey-and-pmaximumkey"></a>pMinimumKey e pMaximumKey

I membri **pMinimumKey** e **pMaximumKey** possono essere usati per cercare le chiavi che rientrano in un intervallo. Se il membro **fAnyMatchInRange** è impostato su **false**, DRT restituirà la chiave o le chiavi più vicine alla destinazione di ricerca, specificata usando l'argomento PKey passato nella funzione [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) , che rientra nell'intervallo. Si noti che l'argomento *pKey* passato a **DrtStartSearch** deve rientrare nell'intervallo definito da **pMinimumKey** e **pMaximumKey**. Per cercare una chiave precisa, impostare **pMinimumKey**, **pMaximumKey** e *pKey* sullo stesso valore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione e annullamento della registrazione delle chiavi](registering-and-deregistering-keys.md)
</dt> <dt>

[Informazioni sulle tabelle di routing distribuite](about-distributed-routing-tables.md)
</dt> <dt>

[Riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



