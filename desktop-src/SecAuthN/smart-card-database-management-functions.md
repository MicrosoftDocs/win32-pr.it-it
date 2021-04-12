---
description: Gestire il database delle smart card, aggiornando il database usando un contesto di Resource Manager specificato.
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: Funzioni di gestione di database per Smart Card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c424494a30c71e15647da773027311ed53a2599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347306"
---
# <a name="smart-card-database-management-functions"></a>Funzioni di gestione di database per Smart Card

Le funzioni seguenti gestiscono il [*database delle smart card*](../secgloss/s-gly.md), aggiornando il database usando un [*contesto di Resource Manager*](../secgloss/r-gly.md)specificato.

> [!Note]  
> La sicurezza del database viene gestita inserendo restrizioni di accesso nel database, invece di aggiungere meccanismi di sicurezza al [*sottosistema Smart Card*](../secgloss/s-gly.md).

 



| Argomento                                                            | Descrizione                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardAddReaderToGroup**](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | Aggiungere un [*Reader*](../secgloss/r-gly.md) a un [*gruppo Reader*](../secgloss/r-gly.md). |
| [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | Rimuovere una smart card dal sistema.                                                                                                                                    |
| [**SCardForgetReader**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | Rimuovere un Reader dal sistema.                                                                                                                                        |
| [**SCardForgetReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | Rimuovere un gruppo di Reader dal sistema.                                                                                                                                  |
| [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | Introduce una nuova scheda al sistema.                                                                                                                                     |
| [**SCardIntroduceReader**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | Introduce un nuovo lettore al sistema.                                                                                                                                   |
| [**SCardIntroduceReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | Introduce un nuovo gruppo di lettori al sistema.                                                                                                                             |
| [**SCardRemoveReaderFromGroup**](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | Rimuovere un Reader da un gruppo di Reader.                                                                                                                                    |



 

 

 
