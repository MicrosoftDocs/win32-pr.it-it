---
title: Ambito della query
description: L'ambito di una query è determinato dall'oggetto a cui si esegue l'associazione.
ms.assetid: 7ece8599-8a4b-45a1-95f4-a4180052f245
ms.tgt_platform: multiple
keywords:
- ambito della query ADSI
- query ADSI , ambito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a31ebe378502dd9b4ddda6dce83e3547dab580360a8d1ec07516d1e3347cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023254"
---
# <a name="scope-of-query"></a>Ambito della query

L'ambito di una query è determinato dall'oggetto a cui si esegue l'associazione. Se non si è certi di dove si trova l'oggetto all'interno dell'organizzazione, sarà necessario eseguire una ricerca più ampia possibile. Tuttavia, se si sa che l'oggetto sarà contenuto all'interno di un dominio specifico, ad esempio il dominio a cui l'utente è connesso o all'interno di un gruppo specifico, ad esempio il gruppo Managers, è necessario impostare l'ambito della ricerca in modo da riflettere la circostanza. Per ottenere prestazioni ottimali, è consigliabile provare a impostare come destinazione l'ambito per cercare il minor numero possibile di oggetti.

Quando non si è certi della posizione di un oggetto nell'organizzazione, è possibile eseguire l'associazione al servizio di catalogo globale. Il servizio di catalogo globale contiene un elenco di ogni oggetto nella directory e un piccolo subset di attributi di ogni oggetto. Dopo aver trovato l'oggetto nel catalogo globale, è possibile recuperarne il nome distinto dal catalogo globale e usarlo per eseguire l'associazione all'oggetto per eseguire altre operazioni.

Dopo aver deciso a quale oggetto associare, è possibile limitare ulteriormente la query a uno degli ambiti seguenti: una query di base, una query a un livello o una ricerca nel sottoalbero, come illustrato nella figura seguente.

![oggetti nella radice di una ricerca di una ricerca di base, di un livello o di un sottoalbero](images/netds6.png)

## <a name="base"></a>Base

Una query di base limita la ricerca solo all'oggetto di base. Il numero massimo di oggetti restituiti è sempre uno. Questa ricerca può essere usata per verificare l'esistenza di un oggetto. Ad esempio, se si ha il nome distinto di un oggetto ed è necessario verificare l'esistenza dell'oggetto in base al percorso, è possibile usare una ricerca a un livello. Se la ricerca ha esito negativo, è possibile presupporre che l'oggetto sia stato rinominato o spostato in un percorso diverso oppure che siano stati dati non corretti sull'oggetto. Tenere presente che è necessario archiviare il GUID anziché il nome distinto se si vuole rivedere un oggetto. In questo modo l'oggetto può essere rinominato o spostato nella gerarchia di directory senza interrompere il collegamento persistente.

## <a name="one-level"></a>Un livello

Una ricerca a un livello è limitata agli elementi figlio immediati di un oggetto di base, ma esclude l'oggetto di base stesso. Questa impostazione può eseguire una ricerca mirata di oggetti figlio immediati di un oggetto padre. Ad esempio, se si ha un oggetto padre denominato P1 e i relativi figli immediati sono: C1, C2, C3, in una ricerca a un livello, È necessario includere C1, C2 e C3 quando si valutano i criteri, ma P1 non fa parte della ricerca. Una ricerca a un livello può essere usata per enumerare tutti gli elementi figlio di un oggetto. In alcuni provider ADSI, infatti, l'enumerazione [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) si traduce in una ricerca a un livello.

## <a name="subtree"></a>Sottoalbero

Una ricerca sottoalbero, nota anche come ricerca approfondita, include tutti gli oggetti sotto l'oggetto di base, escludendo l'oggetto di base stesso. Questa ricerca può generare riferimenti ad altri server. Questa ricerca ha l'ambito più ampio e può restituire un set di risultati di grandi dimensioni. Se possibile, cercare almeno un attributo indicizzato e impostare le impostazioni delle segnalazioni (per altre informazioni, vedere Prestazioni e [gestione](performance-and-handling-large-result-sets.md)di set di risultati di grandi dimensioni ) in modo che corrispondano ai requisiti di ricerca. È anche consigliabile che i risultati di una ricerca nel sottoalbero siano eseguiti in modo asincrono e di cui sia stato eseguito il pager per ridurre il sovraccarico del server e l'efficacia della rete. Una ricerca nel sottoalbero viene in genere usata per cercare oggetti per un determinato ambito. Ad esempio, cercare tutti gli utenti con account che scadranno tra 30 giorni o meno.

 

 




