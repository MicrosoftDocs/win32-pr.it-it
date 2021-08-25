---
description: Prima che un'applicazione possa eseguire ricerche nella tabella di routing distribuito (DRT), è necessario creare una query di ricerca.
ms.assetid: b3403a64-128c-461e-9384-8e62c03322e1
title: Ricerca di una tabella di routing distribuito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9016c351412d80b7adb97bc4325dae546e24db68e5737badc311e7c068f1a22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034241"
---
# <a name="searching-a-distributed-routing-table"></a>Ricerca di una tabella di routing distribuito

Prima che un'applicazione possa eseguire ricerche nella tabella di routing distribuito (DRT), è necessario creare una query di ricerca. Il valore della chiave desiderato viene specificato dall'applicazione quando viene chiamata [**la funzione DrtStartSearch.**](/windows/desktop/api/drt/nf-drt-drtstartsearch) Il comportamento della ricerca è determinato dalle informazioni specificate dall'applicazione nella [**struttura DRT \_ SEARCH \_ INFO.**](/windows/desktop/api/drt/ns-drt-drt_search_info)

In genere, un evento dell'applicazione viene segnalato quando la ricerca individua i risultati e un altro alla fine della ricerca. Tuttavia, se **fIterative** è impostato in [**DRT \_ SEARCH \_ INFO,**](/windows/desktop/api/drt/ns-drt-drt_search_info)un evento dell'applicazione può essere segnalato quando viene effettuato un contatto con ogni nodo lungo la strada.

Dopo la segnalazione di un evento, l'applicazione chiama quindi la [**funzione DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) per i risultati. Se il codice restituito è **S \_ OK,** i risultati vengono puntati alla struttura [**DRT \_ SEARCH \_ RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) restituita dall'API. I risultati restituiti rientrano nell'intervallo di valori specificato in [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info). Nel caso in cui la ricerca non trovi alcuna corrispondenza, verrà restituito solo il valore **DRT \_ E NO \_ \_ MORE** alla fine dei risultati restituiti.

Le informazioni seguenti illustrano in dettaglio come i membri contenuti in [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) consentono a un'applicazione di dettare in modo specifico il comportamento di ricerca dell'infrastruttura DRT:

## <a name="fallowcurrentinstancematch"></a>fAllowCurrentInstanceMatch

Per impostazione predefinita, i risultati della ricerca DRT includono solo le corrispondenze trovate all'esterno del nodo locale. **L'impostazione fAllowCurrentInstanceMatch** specifica che i risultati della ricerca includono anche le corrispondenze trovate nell'istanza DRT locale.

## <a name="cmaxendpoints"></a>cMaxEndpoints

La quantità e l'intervallo dei risultati restituiti dalla ricerca vengono specificati dall'applicazione con i valori **cMaxEndpoints** (quantity) e **pMinimumKey** e **pMaximumKey** (intervallo) a cui fa riferimento [**DRT \_ SEARCH \_ INFO.**](/windows/desktop/api/drt/ns-drt-drt_search_info)

Quando **cMaxEndpoints = 1,** l'infrastruttura DRT cerca una chiave, restituisce una corrispondenza all'interno dell'intervallo specificato dai valori **pMinimumKey** e **pMaximumKey** in [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info). Questa corrispondenza può essere una corrispondenza esatta o la corrispondenza più vicina all'interno dell'intervallo. Se non viene trovata una corrispondenza, viene restituito **DRT \_ E NO \_ \_ MORE.**

Se **cMaxEndpoints > 1,** l'infrastruttura DRT restituirà corrispondenze all'interno dell'intervallo fino al valore **di cMaxEndpoints**. Le corrispondenze restituite possono contenere una corrispondenza esatta o i risultati della corrispondenza più vicini all'interno dell'intervallo. Inoltre, se **pMinimumKey** e **pMaximumKey** sono impostati sullo stesso valore, viene eseguita una ricerca solo per tale valore, che restituisce **DRT \_ E NO \_ \_ MORE** se non viene trovato.

## <a name="fanymatchinrange"></a>fAnyMatchInRange

Il membro **fAnyMatchInRange** indica se la ricerca verrà interrotta dopo che la prima corrispondenza si trova all'interno dell'intervallo specificato o se la ricerca continuerà per la corrispondenza più vicina alla chiave specificata nell'API [**DrtStartSearch.**](/windows/desktop/api/drt/nf-drt-drtstartsearch) Quando **fAnyMatchInRange** è impostato, la ricerca viene eseguita con **cMaxEndpoints = 1** indipendentemente dal valore specificato di **cMaxEndpoints** in [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info).

## <a name="fiterative"></a>fIterative

Il **membro fIterative** specifica se a ogni nodo contattato dall'infrastruttura DRT durante la ricerca saranno associati i dati chiave/endpoint associati all'applicazione tramite [**DRT SEARCH \_ \_ RESULT.**](/windows/desktop/api/drt/ns-drt-drt_search_result) Impostando **fIterative** su **TRUE,** verrà forzato il valore **di cMaxEndpoints = 1.** Quando **fIterative** è impostato su **TRUE** all'interno di una query di ricerca per DRT, l'applicazione viene richiamata dopo il contatto con ogni nodo o "hop". Ogni risultato dell'hop contiene una chiave che indica quale nodo verrà cercato successivamente da DRT. Un risultato hop viene restituito [**tramite DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) come risultato **intermedio di DRT \_ MATCH. \_**

## <a name="pminimumkey-and-pmaximumkey"></a>pMinimumKey e pMaximumKey

I **membri pMinimumKey** e **pMaximumKey** possono essere usati per cercare chiavi che rientrano in un intervallo. Se il membro **fAnyMatchInRange** è impostato su **FALSE,** la funzione DRT restituirà le chiavi più vicine alla destinazione di ricerca (specificata usando l'argomento pKey passato nella funzione [**DrtStartSearch)**](/windows/desktop/api/drt/nf-drt-drtstartsearch) che rientra nell'intervallo. Si noti che *l'argomento pKey* passato a **DrtStartSearch** deve rientrare nell'intervallo definito da **pMinimumKey** e **pMaximumKey**. Per cercare una chiave precisa, impostare **pMinimumKey**, **pMaximumKey** *e pKey* sullo stesso valore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione e annullamento della registrazione delle chiavi](registering-and-deregistering-keys.md)
</dt> <dt>

[Informazioni sulle tabelle di routing distribuito](about-distributed-routing-tables.md)
</dt> <dt>

[Informazioni di riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



