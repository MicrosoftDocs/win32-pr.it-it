---
description: Un'applicazione che utilizza un'autorità di backup per archiviare le chiavi di sessione in genere segue questa procedura.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Archiviazione di chiavi di sessione mediante un'autorità di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345726"
---
# <a name="storing-session-keys-using-a-backup-authority"></a><span data-ttu-id="44c78-103">Archiviazione di chiavi di sessione mediante un'autorità di backup</span><span class="sxs-lookup"><span data-stu-id="44c78-103">Storing Session Keys Using a Backup Authority</span></span>

<span data-ttu-id="44c78-104">Un'applicazione che utilizza un' [*autorità di backup*](../secgloss/b-gly.md) per archiviare le chiavi di sessione in genere segue questa procedura.</span><span class="sxs-lookup"><span data-stu-id="44c78-104">An application using a [*backup authority*](../secgloss/b-gly.md) to store session keys typically follows these steps.</span></span>

<span data-ttu-id="44c78-105">**Per utilizzare un'autorità di backup**</span><span class="sxs-lookup"><span data-stu-id="44c78-105">**To use a backup authority**</span></span>

1.  <span data-ttu-id="44c78-106">Crittografare il file come di consueto.</span><span class="sxs-lookup"><span data-stu-id="44c78-106">Encrypt the file as usual.</span></span>
2.  <span data-ttu-id="44c78-107">Esportare la [*chiave di sessione*](../secgloss/s-gly.md) usata per crittografare il file in un [*BLOB di chiavi semplice*](../secgloss/s-gly.md), specificando che la chiave [*pubblica di scambio*](../secgloss/k-gly.md) della chiave deve essere usata per crittografare il BLOB della chiave.</span><span class="sxs-lookup"><span data-stu-id="44c78-107">Export the [*session key*](../secgloss/s-gly.md) used to encrypt the file into a [*simple key BLOB*](../secgloss/s-gly.md), specifying that your own [*key exchange public key*](../secgloss/k-gly.md) be used to encrypt the key BLOB.</span></span> <span data-ttu-id="44c78-108">Archiviare questo BLOB di chiavi con il file crittografato.</span><span class="sxs-lookup"><span data-stu-id="44c78-108">Store this key BLOB with the encrypted file.</span></span>
3.  <span data-ttu-id="44c78-109">Esportare di nuovo la chiave di sessione, questa volta specificando che la chiave pubblica dell'autorità di backup verrà usata per crittografare il BLOB della chiave.</span><span class="sxs-lookup"><span data-stu-id="44c78-109">Export the session key again, this time specifying that the backup authority's public key be used to encrypt the key BLOB.</span></span> <span data-ttu-id="44c78-110">Inviare questo BLOB di chiavi all'autorità di backup, insieme alla descrizione della chiave, al numero di serie e così via.</span><span class="sxs-lookup"><span data-stu-id="44c78-110">Send this key BLOB to the backup authority, along with the key's description, serial number, and so on.</span></span>

<span data-ttu-id="44c78-111">Se una [*coppia di chiavi*](../secgloss/k-gly.md) viene persa, le chiavi possono essere recuperate dall' [*autorità di backup*](../secgloss/b-gly.md) se è possibile stabilire l'identità del proprietario delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="44c78-111">If a [*key pair*](../secgloss/k-gly.md) is lost, the keys can be retrieved from the [*backup authority*](../secgloss/b-gly.md) if the identity of the keys' owner can be established.</span></span> <span data-ttu-id="44c78-112">La procedura per stabilire l'identità è determinata dai criteri dell'autorità di backup specifica e non comporta CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="44c78-112">The procedure for establishing identity is determined by the policy of the particular backup authority and does not involve CryptoAPI.</span></span>

<span data-ttu-id="44c78-113">Per il codice necessario per creare una chiave della sessione ed esportare la chiave in un [*BLOB di chiavi semplice*](../secgloss/s-gly.md) che può essere scritto in un file su disco, vedere [esempio C Program: exporting a Session Key](example-c-program-exporting-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="44c78-113">For the code needed to create a session key and export that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

 

 
