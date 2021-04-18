---
description: Il formato del certificato X. 509 versione 3 identifica più estensioni che possono essere aggiunte a un certificato.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Estensioni (API di registrazione certificati)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5478b8edeff3524ada760cc5680f5c9dca359e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315408"
---
# <a name="extensions-certificate-enrollment-api"></a><span data-ttu-id="34a9a-103">Estensioni (API di registrazione certificati)</span><span class="sxs-lookup"><span data-stu-id="34a9a-103">Extensions (Certificate Enrollment API)</span></span>

<span data-ttu-id="34a9a-104">Il formato del certificato X. 509 versione 3 identifica più estensioni che possono essere aggiunte a un certificato.</span><span class="sxs-lookup"><span data-stu-id="34a9a-104">The X.509 version 3 certificate format identifies multiple extensions that can be added to a certificate.</span></span> <span data-ttu-id="34a9a-105">Le estensioni forniscono informazioni avanzate sull'utilizzo delle chiavi, criteri e vincoli dei certificati, moduli nome alternativi e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="34a9a-105">The extensions provide enhanced information about key usage, certificate policies and constraints, alternative name forms, and more.</span></span> <span data-ttu-id="34a9a-106">È possibile usare l'interfaccia [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) per definire un valore di estensione.</span><span class="sxs-lookup"><span data-stu-id="34a9a-106">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an extension value.</span></span> <span data-ttu-id="34a9a-107">Molte delle estensioni comuni possono essere create usando interfacce predefinite derivate da **IX509Extension**.</span><span class="sxs-lookup"><span data-stu-id="34a9a-107">Many of the common extensions can be created by using predefined interfaces derived from **IX509Extension**.</span></span> <span data-ttu-id="34a9a-108">Una raccolta di estensioni viene aggiunta a una richiesta di certificato includendo la raccolta negli attributi della richiesta.</span><span class="sxs-lookup"><span data-stu-id="34a9a-108">A collection of extensions is added to a certificate request by including the collection in the request attributes.</span></span> <span data-ttu-id="34a9a-109">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="34a9a-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="34a9a-110">Estensioni supportate</span><span class="sxs-lookup"><span data-stu-id="34a9a-110">Supported Extensions</span></span>](supported-extensions.md)
-   [<span data-ttu-id="34a9a-111">\#Estensioni PKCS 10</span><span class="sxs-lookup"><span data-stu-id="34a9a-111">PKCS \#10 Extensions</span></span>](pkcs--10-extensions.md)
-   [<span data-ttu-id="34a9a-112">Estensioni CMC</span><span class="sxs-lookup"><span data-stu-id="34a9a-112">CMC Extensions</span></span>](cmc-extensions.md)

 

 



