---
description: I programmi di esempio nelle sezioni seguenti eseguono operazioni che richiedono la disponibilità di coppie di chiavi pubbliche/private per la crittografia e la decrittografia di file, messaggi e firme.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Contenitori chiave, chiavi e certificati necessari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759464"
---
# <a name="necessary-key-containers-keys-and-certificates"></a><span data-ttu-id="1e214-103">Contenitori chiave, chiavi e certificati necessari</span><span class="sxs-lookup"><span data-stu-id="1e214-103">Necessary Key Containers, Keys, and Certificates</span></span>

<span data-ttu-id="1e214-104">I programmi di esempio nelle sezioni seguenti eseguono operazioni che richiedono la disponibilità di [*coppie di chiavi pubbliche/private*](../secgloss/p-gly.md) per la crittografia e la decrittografia di file, messaggi e firme.</span><span class="sxs-lookup"><span data-stu-id="1e214-104">Example programs in the following sections perform operations that require [*public/private key pairs*](../secgloss/p-gly.md) to be available for encrypting and decrypting files, messages, and signatures.</span></span> <span data-ttu-id="1e214-105">Molti di questi programmi verranno compilati, collegati ed eseguiti, ma non riusciranno in fase di esecuzione senza la presenza di [*contenitori*](../secgloss/k-gly.md)di chiavi, chiavi, [*archivi certificati*](../secgloss/c-gly.md)e certificati appropriati in tali archivi.</span><span class="sxs-lookup"><span data-stu-id="1e214-105">Many of these programs will compile, link, and run but fail at run time without the existence of proper [*key containers*](../secgloss/k-gly.md), keys, [*certificate stores*](../secgloss/c-gly.md), and certificates in those stores.</span></span>

<span data-ttu-id="1e214-106">Inoltre, alcuni dei certificati nell'archivio MY devono disporre di alcune delle proprietà estese impostate.</span><span class="sxs-lookup"><span data-stu-id="1e214-106">In addition, some of the certificates in the MY store must have some of their extended properties set.</span></span>

<span data-ttu-id="1e214-107">La creazione del contenitore di chiavi predefinito necessario può essere eseguita eseguendo il programma nel [programma C di esempio: creazione di un contenitore di chiavi e generazione di chiavi](example-c-program-creating-a-key-container-and-generating-keys.md).</span><span class="sxs-lookup"><span data-stu-id="1e214-107">Creating the needed default key container can be done by running the program in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span> <span data-ttu-id="1e214-108">Si noti che la creazione di un contenitore di chiavi non genera automaticamente coppie di chiavi pubbliche/private.</span><span class="sxs-lookup"><span data-stu-id="1e214-108">Note that the creation of a key container does not automatically generate public/private key pairs.</span></span> <span data-ttu-id="1e214-109">Il programma di esempio, tuttavia, crea il contenitore di chiavi e genera le coppie di chiavi pubblica/privata.</span><span class="sxs-lookup"><span data-stu-id="1e214-109">The example program, however, both creates the key container and generates the public/private key pairs.</span></span>

<span data-ttu-id="1e214-110">Dopo la generazione delle coppie di chiavi pubblica/privata, è possibile ottenere i certificati di test con tali chiavi da un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="1e214-110">After public/private key pairs have been generated, test certificates using those keys can be obtained from a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="1e214-111">Molti programmi presuppongono che i certificati con nomi di soggetto specifici esistano nell'archivio di sistema MY.</span><span class="sxs-lookup"><span data-stu-id="1e214-111">Several of the programs assume that certificates with specific subject names exist in the MY system store.</span></span> <span data-ttu-id="1e214-112">In particolare, diversi programmi cercano certificati con i nomi di soggetto "certificato di test completo" e "Hortense".</span><span class="sxs-lookup"><span data-stu-id="1e214-112">In particular, several programs look for certificates with the subject names "Full Test Cert" and "Hortense."</span></span> <span data-ttu-id="1e214-113">I nomi oggetto per i certificati possono essere modificati nel codice in modo che corrispondano ai nomi soggetto dei certificati presenti nell'archivio certificati personali.</span><span class="sxs-lookup"><span data-stu-id="1e214-113">The subject names for the certificates may be changed in the code to match the subject names of certificates that exist in the MY certificate store.</span></span>

<span data-ttu-id="1e214-114">Esecuzione del programma di esempio nel [programma C di esempio: elencare i certificati in un archivio](example-c-program-listing-the-certificates-in-a-store.md) visualizzerà tutti i certificati in un archivio e tutte le proprietà estese impostate per tali certificati.</span><span class="sxs-lookup"><span data-stu-id="1e214-114">Running the example program in [Example C Program: Listing the Certificates in a Store](example-c-program-listing-the-certificates-in-a-store.md) will display all of the certificates in a store and all of the extended properties that are set on those certificates.</span></span>

 

 
