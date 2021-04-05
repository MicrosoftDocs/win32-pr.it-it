---
description: Quando un documento o un testo deve avere una privacy protetta da un singolo utente o quando il documento deve essere condiviso da un piccolo gruppo di persone che hanno accesso alla stessa password segreta, è possibile eseguire semplici operazioni di crittografia/decrittografia.
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: Crittografia e decrittografia di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7123544fb9c8fa59291be2eae2c5bf9a120f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968130"
---
# <a name="encrypting-and-decrypting-data"></a><span data-ttu-id="56623-103">Crittografia e decrittografia di dati</span><span class="sxs-lookup"><span data-stu-id="56623-103">Encrypting and Decrypting Data</span></span>

<span data-ttu-id="56623-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="56623-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="56623-105">Usare invece il .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="56623-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="56623-106">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="56623-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="56623-107">Quando un documento o un testo deve avere una privacy protetta da un singolo utente o quando il documento deve essere condiviso da un piccolo gruppo di persone che hanno accesso alla stessa password segreta, è possibile eseguire semplici operazioni di crittografia/decrittografia.</span><span class="sxs-lookup"><span data-stu-id="56623-107">When a document or text needs to have privacy protected by a single user or when the document is to be shared among a small group of people who all have access to the same secret password, simple encryption/decryption can be done.</span></span> <span data-ttu-id="56623-108">CAPICOM non supporta il \# tipo di contenuto EncryptedData di PKCS 7, ma usa una struttura ASN non standard per EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="56623-108">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a non-standard ASN structure for EncryptedData.</span></span> <span data-ttu-id="56623-109">Pertanto, solo CAPICOM è in grado di decrittografare un oggetto capicot EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="56623-109">Therefore, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

<span data-ttu-id="56623-110">Le sezioni seguenti illustrano esempi per le attività di crittografia e decrittografia:</span><span class="sxs-lookup"><span data-stu-id="56623-110">The following sections show examples for encryption and decryption tasks:</span></span>

-   [<span data-ttu-id="56623-111">Crittografia di un messaggio in CAPICOM</span><span class="sxs-lookup"><span data-stu-id="56623-111">Encrypting a Message in CAPICOM</span></span>](encrypting-a-message-in-capicom.md)
-   [<span data-ttu-id="56623-112">Decrittografia di un messaggio in CAPICOM</span><span class="sxs-lookup"><span data-stu-id="56623-112">Decrypting a Message in CAPICOM</span></span>](decrypting-a-message-in-capicom.md)

 

 



