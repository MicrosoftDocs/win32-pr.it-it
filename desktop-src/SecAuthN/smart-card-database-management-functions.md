---
description: Gestire il smart card database, aggiornando il database usando un contesto di Resource Manager specificato.
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: Funzioni di gestione del database smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b107663df8b80b5883c9ce9b3f045e8d7913ac92b5acb23d9ae758dafa2ac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917807"
---
# <a name="smart-card-database-management-functions"></a>Funzioni di gestione del database smart card

Le funzioni seguenti gestiscono il [*smart card database*](../secgloss/s-gly.md), aggiornando il database usando un contesto di resource [*manager specificato.*](../secgloss/r-gly.md)

> [!Note]  
> La sicurezza del database viene mantenuta inserendo restrizioni di accesso al database, anziché aggiungendo meccanismi di sicurezza al sottosistema smart card [*database*](../secgloss/s-gly.md).

 



| Argomento                                                            | Descrizione                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardAddReaderToGroup**](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | Aggiungere un [*lettore*](../secgloss/r-gly.md) a un [*gruppo di lettori*](../secgloss/r-gly.md). |
| [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | Rimuovere un smart card dal sistema.                                                                                                                                    |
| [**SCardForgetReader**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | Rimuovere un lettore dal sistema.                                                                                                                                        |
| [**SCardForgetReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | Rimuovere un gruppo di lettori dal sistema.                                                                                                                                  |
| [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | Introdurre una nuova scheda nel sistema.                                                                                                                                     |
| [**SCardIntroduceReader**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | Introdurre un nuovo lettore nel sistema.                                                                                                                                   |
| [**SCardIntroduceReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | Introdurre un nuovo gruppo di lettori nel sistema.                                                                                                                             |
| [**SCardRemoveReaderFromGroup**](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | Rimuovere un lettore da un gruppo di lettori.                                                                                                                                    |



 

 

 
