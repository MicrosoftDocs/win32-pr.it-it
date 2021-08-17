---
description: Eseguire una query smart card database. Possono fornire un elenco di smart card fornite da un utente specifico, le interfacce e il provider di servizi primario di una scheda specifica, i gruppi di lettori definiti per il sistema e i lettori all'interno di un set di gruppi di lettori.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Funzioni di query del database smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54050ad6e6b5b4d7e8c91f7cdefab683274d153050100545c9e1ed5452c47cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917797"
---
# <a name="smart-card-database-query-functions"></a>Funzioni di query del database smart card

Nelle funzioni seguenti viene eseguita una query [*smart card database*](../secgloss/s-gly.md). Possono fornire un elenco di smart card fornite da un utente specifico, le interfacce [](../secgloss/r-gly.md) e il [*provider*](../secgloss/p-gly.md) di servizi [](../secgloss/r-gly.md) primario di una scheda specifica, i gruppi di lettori definiti per il sistema e i lettori all'interno di un set di gruppi di lettori.

Quando si usano queste funzioni, è possibile eseguire una query sul database smart card completo oppure limitare la ricerca impostando il contesto [*di resource manager*](../secgloss/r-gly.md). Il contesto di Gestione risorse viene impostato chiamando [**SCardEstablishContext prima**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) di chiamare una funzione di query.

> [!Note]  
> Senza un contesto specificato, alcune informazioni potrebbero essere ancora inaccessibili a causa di restrizioni di sicurezza.

 



| Argomento                                                  | Descrizione                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardGetProviderId**](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | Recupera l'identificatore (GUID) del [*provider di servizi primario*](../secgloss/p-gly.md) per la scheda specificata. |
| [**SCardListCards**](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | Recuperare un elenco di schede introdotte in precedenza nel sistema da un utente specifico.                                                                                                     |
| [**SCardListInterfaces**](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | Recupera gli identificatori (GUID) delle interfacce fornite da una scheda specificata.                                                                                                         |
| [**SCardListReaderGroups**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | Recuperare un elenco di gruppi di lettori introdotti in precedenza nel sistema.                                                                                                 |
| [**SCardListReaders**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | Recuperare l'elenco di lettori all'interno di un set di gruppi di lettori denominati.                                                                                                                    |



 

 

 
