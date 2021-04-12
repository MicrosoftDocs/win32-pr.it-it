---
description: Viene usato un Message Authentication Code (MAC) per rilevare manomissioni e falsificazioni di messaggi.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Codici di autenticazione messaggi in Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232828"
---
# <a name="message-authentication-codes-in-schannel"></a>Codici di autenticazione messaggi in Schannel

Viene usato un [*Message Authentication Code*](../secgloss/m-gly.md) (Mac) per rilevare manomissioni e falsificazioni di messaggi. Il mittente di un messaggio crea un MAC crittografando un [*hash*](../secgloss/h-gly.md) unidirezionale del corpo del messaggio usando una chiave di [*sessione*](../secgloss/s-gly.md) condivisa da mittente e destinatario. Il MAC viene aggiunto al messaggio inviato al destinatario. Il destinatario del messaggio genera di nuovo il MAC, usando la chiave della sessione condivisa e il corpo del messaggio e confronta il MAC generato con il Mac ricevuto dal mittente. Se i due sono identici, il mittente deve avere la chiave della sessione condivisa e il messaggio non è stato modificato durante il transito.

Nei protocolli Schannel, l'algoritmo utilizzato per generare il MAC è determinato dal [pacchetto di crittografia](cipher-suites-in-schannel.md) utilizzato dal mittente e dal destinatario.

 

 
