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
# <a name="message-authentication-codes-in-schannel"></a><span data-ttu-id="3bb4f-103">Codici di autenticazione messaggi in Schannel</span><span class="sxs-lookup"><span data-stu-id="3bb4f-103">Message Authentication Codes in Schannel</span></span>

<span data-ttu-id="3bb4f-104">Viene usato un [*Message Authentication Code*](../secgloss/m-gly.md) (Mac) per rilevare manomissioni e falsificazioni di messaggi.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-104">A [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) is used to detect message tampering and forgery.</span></span> <span data-ttu-id="3bb4f-105">Il mittente di un messaggio crea un MAC crittografando un [*hash*](../secgloss/h-gly.md) unidirezionale del corpo del messaggio usando una chiave di [*sessione*](../secgloss/s-gly.md) condivisa da mittente e destinatario.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-105">The sender of a message creates a MAC by encrypting a one-way [*hash*](../secgloss/h-gly.md) of the message body using a [*session key*](../secgloss/s-gly.md) shared by sender and recipient.</span></span> <span data-ttu-id="3bb4f-106">Il MAC viene aggiunto al messaggio inviato al destinatario.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-106">The MAC is appended to the message that is sent to the recipient.</span></span> <span data-ttu-id="3bb4f-107">Il destinatario del messaggio genera di nuovo il MAC, usando la chiave della sessione condivisa e il corpo del messaggio e confronta il MAC generato con il Mac ricevuto dal mittente.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-107">The message recipient generates the MAC again, using the shared session key and message body, and compares the generated MAC to the MAC received from the sender.</span></span> <span data-ttu-id="3bb4f-108">Se i due sono identici, il mittente deve avere la chiave della sessione condivisa e il messaggio non è stato modificato durante il transito.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-108">If the two are identical, then the sender must have the shared session key, and the message has not been altered in transit.</span></span>

<span data-ttu-id="3bb4f-109">Nei protocolli Schannel, l'algoritmo utilizzato per generare il MAC è determinato dal [pacchetto di crittografia](cipher-suites-in-schannel.md) utilizzato dal mittente e dal destinatario.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-109">In Schannel protocols, the algorithm used to generate the MAC is determined by the [cipher suite](cipher-suites-in-schannel.md) in use by the sender and recipient.</span></span>

 

 
