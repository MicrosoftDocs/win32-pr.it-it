---
description: A volte un messaggio firmato richiede un controfirma.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Controfirme messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8dff2920217dd9a79f917f7b625da3919747d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752127"
---
# <a name="message-countersignatures"></a><span data-ttu-id="d9ce5-103">Controfirme messaggi</span><span class="sxs-lookup"><span data-stu-id="d9ce5-103">Message Countersignatures</span></span>

<span data-ttu-id="d9ce5-104">A volte un messaggio firmato richiede un [*controfirma*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d9ce5-104">Sometimes a signed message requires a [*countersignature*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="d9ce5-105">Ad esempio, l'utente A può inviare un messaggio di dati firmato all'utente B, in attesa di B per confermare l'accordo con i termini contenuti nel documento.</span><span class="sxs-lookup"><span data-stu-id="d9ce5-105">For example, user A may send a signed-data message to user B, expecting B to confirm agreement with the terms contained in the document.</span></span> <span data-ttu-id="d9ce5-106">L'utente B decodifica il messaggio, legge i termini e, se il contratto, controfirma il messaggio.</span><span class="sxs-lookup"><span data-stu-id="d9ce5-106">User B decodes the message, reads the terms and, if in agreement, countersigns the message.</span></span> <span data-ttu-id="d9ce5-107">Il messaggio controfirmato viene quindi inviato di nuovo all'utente A. l'utente A ora sa e può dimostrare che l'utente B ha accettato le condizioni.</span><span class="sxs-lookup"><span data-stu-id="d9ce5-107">The countersigned message is then sent back to user A. User A now knows, and can prove, that user B agreed to the terms.</span></span>

<span data-ttu-id="d9ce5-108">Nella tabella seguente sono elencate le sezioni che contengono le descrizioni delle procedure o esempi di programmi C del messaggio controfirma.</span><span class="sxs-lookup"><span data-stu-id="d9ce5-108">The following table lists sections that contain procedure descriptions or C program examples of message countersigning.</span></span>



| <span data-ttu-id="d9ce5-109">Sezione</span><span class="sxs-lookup"><span data-stu-id="d9ce5-109">Section</span></span>                                                                                                                                 | <span data-ttu-id="d9ce5-110">Contenuto</span><span class="sxs-lookup"><span data-stu-id="d9ce5-110">Contents</span></span>                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="d9ce5-111">Funzioni di messaggio</span><span class="sxs-lookup"><span data-stu-id="d9ce5-111">Message Functions</span></span>](cryptography-functions.md)                                                                       | <span data-ttu-id="d9ce5-112">Elenca le funzioni di firma del contatore.</span><span class="sxs-lookup"><span data-stu-id="d9ce5-112">Lists the counter signature functions.</span></span>                             |
| [<span data-ttu-id="d9ce5-113">Controfirma un messaggio</span><span class="sxs-lookup"><span data-stu-id="d9ce5-113">Countersigning a Message</span></span>](countersigning-a-message.md)                                                                                | <span data-ttu-id="d9ce5-114">Descrive il processo di contatore della firma di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="d9ce5-114">Details the process of counter signing a message.</span></span>                  |
| [<span data-ttu-id="d9ce5-115">Verifica di un controfirma</span><span class="sxs-lookup"><span data-stu-id="d9ce5-115">Verifying a Countersignature</span></span>](verifying-a-countersignature.md)                                                                        | <span data-ttu-id="d9ce5-116">Descrive la procedura per la verifica di una firma del contatore.</span><span class="sxs-lookup"><span data-stu-id="d9ce5-116">Details the procedure for verifying a counter signature.</span></span>           |
| [<span data-ttu-id="d9ce5-117">Verifica di un messaggio firmato</span><span class="sxs-lookup"><span data-stu-id="d9ce5-117">Verifying a Signed Message</span></span>](verifying-a-signed-message.md)                                                                            | <span data-ttu-id="d9ce5-118">Descrive in dettaglio un processo per la verifica della firma in un messaggio firmato.</span><span class="sxs-lookup"><span data-stu-id="d9ce5-118">Details a process for verifying the signature on a signed message.</span></span> |
| [<span data-ttu-id="d9ce5-119">Esempio di programma C: codifica e decodifica di un messaggio controfirmato</span><span class="sxs-lookup"><span data-stu-id="d9ce5-119">Example C Program: Encoding and Decoding a CounterSigned Message</span></span>](example-c-program-encoding-and-decoding-a-countersigned-message.md) | <span data-ttu-id="d9ce5-120">Programma C di esempio che codifica e decodifica un messaggio controfirmato.</span><span class="sxs-lookup"><span data-stu-id="d9ce5-120">Sample C program that encodes and decodes a countersigned message.</span></span> |



 

 

 
