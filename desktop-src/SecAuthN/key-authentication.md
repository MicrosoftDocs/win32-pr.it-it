---
description: Molte forme di autenticazione si basano sull'idea che un'entità possa dimostrare la propria identità se è in grado di dimostrare che conosce una chiave, ad esempio una password, che può essere nota solo.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Autenticazione della chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231844"
---
# <a name="key-authentication"></a><span data-ttu-id="e87d7-103">Autenticazione della chiave</span><span class="sxs-lookup"><span data-stu-id="e87d7-103">Key Authentication</span></span>

<span data-ttu-id="e87d7-104">Molte forme di autenticazione si basano sull'idea che un'entità possa dimostrare la propria identità se è in grado di dimostrare che conosce una chiave, ad esempio una password, che può essere nota solo.</span><span class="sxs-lookup"><span data-stu-id="e87d7-104">Many forms of authentication are based on the idea that an entity can prove its identity if it can prove it knows a key, such as a password, that only it can know.</span></span>

<span data-ttu-id="e87d7-105">Le tecniche di autenticazione basate su un segreto, ad esempio una password, devono avere un modo per evitare che il segreto diventi una conoscenza pubblica.</span><span class="sxs-lookup"><span data-stu-id="e87d7-105">Authentication techniques that rely on a secret, such as a password, need to have a way to keep the secret from becoming public knowledge.</span></span> <span data-ttu-id="e87d7-106">Un proprietario della password non può passare a una porta e fornire la password.</span><span class="sxs-lookup"><span data-stu-id="e87d7-106">A password owner cannot walk up to a door and give the password.</span></span> <span data-ttu-id="e87d7-107">Un utente oltre a portiere potrebbe essere in attesa; o potrebbe essere lo sportello errato.</span><span class="sxs-lookup"><span data-stu-id="e87d7-107">Someone besides the doorkeeper might be listening; or it might be the wrong door.</span></span> <span data-ttu-id="e87d7-108">Per tenere un segreto, è necessario che un utente conosca la password senza rivelare la password.</span><span class="sxs-lookup"><span data-stu-id="e87d7-108">In order to keep a secret, there must be a way to prove a user knows the password without revealing the password.</span></span> <span data-ttu-id="e87d7-109">Si tratta dell'idea alla base dell'autenticazione con chiave privata, un metodo di verifica usato in tutto il [*protocollo Kerberos*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e87d7-109">That is the idea behind secret key authentication, a method of verification used throughout the [*Kerberos protocol*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="e87d7-110">Si noti che il "segreto" nell'autenticazione con chiave privata è che il processo di autenticazione viene eseguita in segreto, ovvero senza mai rivelare effettivamente il contenuto della chiave.</span><span class="sxs-lookup"><span data-stu-id="e87d7-110">Notice that the "secret" in secret key authentication is that the authentication process takes place "in secret;" that is, without ever actually revealing the content of the key.</span></span>

<span data-ttu-id="e87d7-111">Per il corretto funzionamento dell'autenticazione con chiave privata, le due parti di una transazione devono condividere una [*chiave di sessione*](../secgloss/s-gly.md) crittografica, che è anche segreta, nota solo a loro e a nessun'altra.</span><span class="sxs-lookup"><span data-stu-id="e87d7-111">For secret key authentication to work, the two parties to a transaction must share a cryptographic [*session key*](../secgloss/s-gly.md) which is also secret, known only to them and to no others.</span></span> <span data-ttu-id="e87d7-112">La chiave è [*simmetrica*](../secgloss/s-gly.md). ovvero una singola chiave utilizzata sia per la crittografia che per la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="e87d7-112">The key is [*symmetric*](../secgloss/s-gly.md); that is, it is a single key used for both encryption and decryption.</span></span> <span data-ttu-id="e87d7-113">Una parte del processo di autenticazione dimostra la propria conoscenza della chiave mediante la crittografia di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="e87d7-113">One party in the authentication process proves its knowledge of the key by encrypting a message.</span></span> <span data-ttu-id="e87d7-114">L'altra parte dimostra la propria conoscenza della chiave mediante la decrittografia del messaggio.</span><span class="sxs-lookup"><span data-stu-id="e87d7-114">The other party proves its knowledge of the key by decrypting the message.</span></span>

 

 
