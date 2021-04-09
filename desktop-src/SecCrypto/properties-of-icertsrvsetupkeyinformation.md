---
description: Le proprietà seguenti sono definite dall'interfaccia ICertSrvSetupKeyInformation.
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: Proprietà di ICertSrvSetupKeyInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882098"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a><span data-ttu-id="7ca93-103">Proprietà di ICertSrvSetupKeyInformation</span><span class="sxs-lookup"><span data-stu-id="7ca93-103">Properties of ICertSrvSetupKeyInformation</span></span>

<span data-ttu-id="7ca93-104">Le proprietà seguenti sono definite dall'interfaccia [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) .</span><span class="sxs-lookup"><span data-stu-id="7ca93-104">The following properties are defined by the [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) interface.</span></span>



| <span data-ttu-id="7ca93-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ca93-105">Property</span></span>                                                                           | <span data-ttu-id="7ca93-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ca93-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ca93-107">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="7ca93-107">**ContainerName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | <span data-ttu-id="7ca93-108">Ottiene o imposta il nome utilizzato dal [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) per generare, archiviare o accedere alla chiave.</span><span class="sxs-lookup"><span data-stu-id="7ca93-108">Gets or sets the name used by the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to generate, store, or access the key.</span></span>                                                                       |
| [<span data-ttu-id="7ca93-109">**Existing**</span><span class="sxs-lookup"><span data-stu-id="7ca93-109">**Existing**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | <span data-ttu-id="7ca93-110">Ottiene o imposta un valore che indica se la chiave privata esiste già.</span><span class="sxs-lookup"><span data-stu-id="7ca93-110">Gets or sets a value that indicates whether the private key already exists.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="7ca93-111">**ExistingCACertificate**</span><span class="sxs-lookup"><span data-stu-id="7ca93-111">**ExistingCACertificate**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | <span data-ttu-id="7ca93-112">Ottiene o imposta il valore binario che è stato codificato tramite [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) e che è il valore binario del certificato della CA che corrisponde a una chiave esistente.</span><span class="sxs-lookup"><span data-stu-id="7ca93-112">Gets or sets the binary value that has been encoded by using [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) and that is the binary value of the CA certificate that corresponds to an existing key.</span></span> |
| [<span data-ttu-id="7ca93-113">**HashAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="7ca93-113">**HashAlgorithm**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | <span data-ttu-id="7ca93-114">Ottiene o imposta il nome dell'algoritmo hash utilizzato per firmare o verificare il certificato della CA per la chiave.</span><span class="sxs-lookup"><span data-stu-id="7ca93-114">Gets or sets the name of the hash algorithm used to sign or verify the CA certificate for the key.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="7ca93-115">**Lunghezza**</span><span class="sxs-lookup"><span data-stu-id="7ca93-115">**Length**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | <span data-ttu-id="7ca93-116">Ottiene o imposta il livello di attendibilità della chiave per uno dei valori supportati dal CSP.</span><span class="sxs-lookup"><span data-stu-id="7ca93-116">Gets or sets the strength of the key to one of the values supported by the CSP.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="7ca93-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="7ca93-117">**ProviderName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | <span data-ttu-id="7ca93-118">Ottiene o imposta il nome del CSP utilizzato per generare o archiviare la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="7ca93-118">Gets or sets the name of the CSP that is used to generate or store the private key.</span></span>                                                                                                                                                                                                               |



 

 

 
