---
title: Ambito della query
description: L'ambito di una query è determinato dall'oggetto a cui si esegue l'associazione.
ms.assetid: 7ece8599-8a4b-45a1-95f4-a4180052f245
ms.tgt_platform: multiple
keywords:
- ambito di query ADSI
- query ADSI, ambito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac51fc261cb418db0018acd996c248766896a25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707387"
---
# <a name="scope-of-query"></a>Ambito della query

L'ambito di una query è determinato dall'oggetto a cui si esegue l'associazione. Se non si è certi della posizione in cui si trova l'oggetto all'interno dell'azienda, sarà necessario eseguire una ricerca più ampia possibile. Tuttavia, se si è certi che l'oggetto sarà contenuto all'interno di un dominio specifico, ad esempio il dominio a cui l'utente è connesso o all'interno di un gruppo specifico, ad esempio il gruppo Managers, sarà necessario impostare l'ambito della ricerca in modo da riflettere la circostanza. Per ottenere prestazioni ottimali, è consigliabile tentare di specificare come destinazione l'ambito per cercare il minor numero possibile di oggetti.

Quando non si è certi della posizione di un oggetto nell'organizzazione, è possibile eseguire l'associazione al servizio catalogo globale. Il servizio catalogo globale contiene un elenco di tutti gli oggetti nella directory e un piccolo subset di tutti gli attributi dell'oggetto. Dopo aver individuato l'oggetto nel catalogo globale, è possibile recuperare il nome distinto dal catalogo globale e utilizzarlo per l'associazione all'oggetto per eseguire altre operazioni.

Dopo aver scelto l'oggetto da associare, è possibile limitare ulteriormente la query a uno degli ambiti seguenti: una query di base, una query a un livello o una ricerca di sottoalbero, come illustrato nella figura seguente.

![oggetti alla radice di una ricerca di una ricerca di base, di un livello o di un sottoalbero](images/netds6.png)

## <a name="base"></a>Base

Una query di base limita la ricerca solo all'oggetto di base. Il numero massimo di oggetti restituiti è sempre uno. Questa ricerca può essere usata per verificare l'esistenza di un oggetto. Se, ad esempio, si dispone di un nome distinto di un oggetto ed è necessario verificare l'esistenza dell'oggetto in base al percorso, è possibile utilizzare una ricerca a un solo livello. Se la ricerca ha esito negativo, è possibile presupporre che l'oggetto sia stato rinominato o spostato in un percorso diverso o che siano stati forniti dati non corretti sull'oggetto. Si noti che è necessario archiviare il GUID anziché il nome distinto se si vuole rivedere un oggetto. In questo modo è possibile rinominare o spostare l'oggetto nella gerarchia di directory senza suddividere il collegamento permanente.

## <a name="one-level"></a>Un livello

Una ricerca a un solo livello è limitata agli elementi figlio immediati di un oggetto di base, ma esclude l'oggetto di base stesso. Questa impostazione può eseguire una ricerca di destinazione per gli oggetti figlio immediati di un oggetto padre. Ad esempio, se si dispone di un oggetto padre denominato P1 e i relativi elementi figlio immediati sono: C1, C2, C3, in una ricerca a un livello, C1, C2 e C3 devono essere inclusi durante la valutazione dei criteri, ma P1 non fa parte della ricerca. Una ricerca a un livello può essere utilizzata per enumerare tutti gli elementi figlio di un oggetto. In alcuni provider ADSI, infatti, l'enumerazione [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) viene convertita in una ricerca a un solo livello.

## <a name="subtree"></a>Sottoalbero

Una ricerca del sottoalbero, nota anche come ricerca completa, include tutti gli oggetti sotto l'oggetto di base, escluso l'oggetto di base stesso. Questa ricerca può generare riferimenti ad altri server. Questa ricerca ha l'ambito più grande e può restituire un set di risultati di grandi dimensioni. Se possibile, eseguire una ricerca su almeno un attributo indicizzato e impostare le impostazioni dei riferimenti (per altre informazioni, vedere [prestazioni e gestione di set di risultati di grandi dimensioni](performance-and-handling-large-result-sets.md)) per soddisfare i requisiti di ricerca. È inoltre consigliabile che i risultati di una ricerca di sottoalbero vengano eseguiti in modo asincrono e di paging per ridurre l'overhead del server e l'efficacia della rete. Una ricerca di sottoalbero viene in genere usata per cercare oggetti per un ambito specifico. Ad esempio, cercare tutti gli utenti con account che scadranno tra 30 giorni o meno.

 

 




