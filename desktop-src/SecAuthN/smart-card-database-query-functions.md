---
description: Eseguire una query sul database delle smart card. Possono fornire un elenco di Smart Card fornite da un utente specifico, le interfacce e il provider di servizi primari di una scheda specifica, i gruppi di Reader definiti per il sistema e i lettori in un set di gruppi di lettori.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Funzioni di query di database per Smart Card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232962"
---
# <a name="smart-card-database-query-functions"></a>Funzioni di query di database per Smart Card

Le funzioni seguenti eseguono una query sul [*database delle smart card*](../secgloss/s-gly.md). Possono fornire un elenco di Smart Card fornite da un utente specifico, le interfacce e il [*provider di servizi primari*](../secgloss/p-gly.md) di una scheda specifica, i [*gruppi di Reader*](../secgloss/r-gly.md) definiti per il sistema e i [*lettori*](../secgloss/r-gly.md) in un set di gruppi di lettori.

Quando si usano queste funzioni, è possibile eseguire una query sul database completo delle smart card oppure è possibile limitare la ricerca impostando il [*contesto di Resource Manager*](../secgloss/r-gly.md). Il contesto di Resource Manager viene impostato chiamando [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) prima di chiamare una funzione di query.

> [!Note]  
> Senza un contesto specificato, alcune informazioni potrebbero essere ancora inaccessibili a causa di restrizioni di sicurezza.

 



| Argomento                                                  | Descrizione                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardGetProviderId**](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | Recuperare l'identificatore (GUID) del [*provider di servizi primario*](../secgloss/p-gly.md) per la scheda specificata. |
| [**SCardListCards**](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | Recuperare un elenco di schede introdotte in precedenza dal sistema da un utente specifico.                                                                                                     |
| [**SCardListInterfaces**](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | Recuperare gli identificatori (GUID) delle interfacce fornite da una scheda specificata.                                                                                                         |
| [**SCardListReaderGroups**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | Recuperare un elenco di gruppi di Reader introdotti in precedenza nel sistema.                                                                                                 |
| [**SCardListReaders**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | Recuperare l'elenco di Reader in un set di gruppi di Reader denominati.                                                                                                                    |



 

 

 
