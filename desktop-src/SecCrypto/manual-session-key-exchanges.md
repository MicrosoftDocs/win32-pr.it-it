---
description: Viene illustrato come inviare un messaggio crittografato.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Scambi manuali di chiavi di sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0114f8173084126a72519d291158f15f3e1c171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563224"
---
# <a name="manual-session-key-exchanges"></a><span data-ttu-id="acdc2-103">Scambi manuali di chiavi di sessione</span><span class="sxs-lookup"><span data-stu-id="acdc2-103">Manual Session Key Exchanges</span></span>

> [!Note]  
> <span data-ttu-id="acdc2-104">La procedura descritta in questa sezione presuppone che gli utenti (o i client CryptoAPI) dispongano già di un proprio set di [*coppie di chiavi pubbliche/private*](../secgloss/p-gly.md) e abbiano ottenuto anche le rispettive [*chiavi pubbliche*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="acdc2-104">The procedure described in this section assumes that the users (or CryptoAPI clients) already possess their own set of [*public/private key pairs*](../secgloss/p-gly.md) and have also obtained each other's [*public keys*](../secgloss/p-gly.md).</span></span>

 

<span data-ttu-id="acdc2-105">Nella figura seguente viene illustrato come utilizzare questa procedura per inviare un messaggio crittografato.</span><span class="sxs-lookup"><span data-stu-id="acdc2-105">The following illustration shows how to use this procedure to send an encrypted message.</span></span>

![invio di un messaggio crittografato](images/capi04.png)

<span data-ttu-id="acdc2-107">Questo approccio è vulnerabile ad almeno una forma comune di attacco.</span><span class="sxs-lookup"><span data-stu-id="acdc2-107">This approach is vulnerable to at least one common form of attack.</span></span> <span data-ttu-id="acdc2-108">Un intercettatore può acquisire copie di uno o più messaggi crittografati e le chiavi crittografate.</span><span class="sxs-lookup"><span data-stu-id="acdc2-108">An eavesdropper can acquire copies of one or more encrypted messages and the encrypted keys.</span></span> <span data-ttu-id="acdc2-109">Quindi, in un secondo momento, l'intercettatore può inviare uno di questi messaggi al ricevitore e il ricevitore non avrà alcun modo per conoscere il messaggio non provenire direttamente dal mittente originale.</span><span class="sxs-lookup"><span data-stu-id="acdc2-109">Then, at some later time, the eavesdropper can send one of these messages to the receiver and the receiver will have no way of knowing the message did not come directly from the original sender.</span></span> <span data-ttu-id="acdc2-110">Questo rischio può essere ridotto impostando il timestamp di tutti i messaggi o usando i numeri di serie.</span><span class="sxs-lookup"><span data-stu-id="acdc2-110">This risk can be reduced by time-stamping all messages or by using serial numbers.</span></span>

<span data-ttu-id="acdc2-111">Il modo più semplice per inviare messaggi crittografati a un altro utente consiste nell'inviare il messaggio crittografato con una chiave di sessione casuale insieme alla chiave di sessione crittografata con la chiave [*pubblica di scambio delle chiavi*](../secgloss/k-gly.md)del destinatario.</span><span class="sxs-lookup"><span data-stu-id="acdc2-111">The easiest way to send encrypted messages to another user is to send the message encrypted with a random session key along with the session key encrypted with the receiver's [*key exchange public key*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="acdc2-112">Di seguito sono riportati i passaggi per l'invio di una chiave di sessione crittografata.</span><span class="sxs-lookup"><span data-stu-id="acdc2-112">Following are the steps for sending an encrypted session key.</span></span>

<span data-ttu-id="acdc2-113">**Per inviare una chiave di sessione crittografata**</span><span class="sxs-lookup"><span data-stu-id="acdc2-113">**To send an encrypted session key**</span></span>

1.  <span data-ttu-id="acdc2-114">Creare una [*chiave di sessione*](../secgloss/s-gly.md) casuale usando la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="acdc2-114">Create a random [*session key*](../secgloss/s-gly.md) by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>
2.  <span data-ttu-id="acdc2-115">Crittografare il messaggio utilizzando la chiave della sessione.</span><span class="sxs-lookup"><span data-stu-id="acdc2-115">Encrypt the message by using the session key.</span></span> <span data-ttu-id="acdc2-116">Questa procedura è illustrata in [crittografia e decrittografia dei dati](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="acdc2-116">This procedure is discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>
3.  <span data-ttu-id="acdc2-117">Esportare la chiave della sessione in un [*BLOB di chiavi*](../secgloss/k-gly.md) con la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , specificando che la chiave deve essere crittografata con la chiave pubblica di scambio delle chiavi dell'utente di destinazione.</span><span class="sxs-lookup"><span data-stu-id="acdc2-117">Export the session key into a [*key BLOB*](../secgloss/k-gly.md) with the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, specifying that the key be encrypted with the destination user's key exchange public key.</span></span>
4.  <span data-ttu-id="acdc2-118">Inviare il messaggio crittografato e il BLOB della chiave crittografata all'utente di destinazione.</span><span class="sxs-lookup"><span data-stu-id="acdc2-118">Send both the encrypted message and the encrypted key BLOB to the destination user.</span></span>
5.  <span data-ttu-id="acdc2-119">L'utente di destinazione importa il BLOB della chiave nel suo CSP usando la funzione [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .</span><span class="sxs-lookup"><span data-stu-id="acdc2-119">The destination user imports the key BLOB into his or her CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span> <span data-ttu-id="acdc2-120">La chiave della sessione verrà decrittografata automaticamente, purché sia stata specificata la chiave pubblica per lo scambio delle chiavi dell'utente di destinazione nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="acdc2-120">This will automatically decrypt the session key, provided the destination user's key exchange public key was specified in step 3.</span></span>
6.  <span data-ttu-id="acdc2-121">L'utente di destinazione può quindi decrittografare il messaggio utilizzando la chiave della sessione, seguendo la procedura descritta in [crittografia dei dati e decrittografia](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="acdc2-121">The destination user can then decrypt the message by using the session key, following the procedure discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

 

 
