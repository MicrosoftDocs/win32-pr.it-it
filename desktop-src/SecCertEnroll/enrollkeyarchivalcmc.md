---
description: Crea una richiesta di certificato CMC per archiviare una chiave privata in un'autorità di certificazione (CA).
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144f5f063834c156da5058fbc34f66ebdb76eb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308113"
---
# <a name="enrollkeyarchivalcmc"></a><span data-ttu-id="3c5da-103">enrollKeyArchivalCMC</span><span class="sxs-lookup"><span data-stu-id="3c5da-103">enrollKeyArchivalCMC</span></span>

<span data-ttu-id="3c5da-104">L'esempio enrollKeyArchivalCMC crea una richiesta di certificato CMC per archiviare una chiave privata in un'autorità di certificazione (CA).</span><span class="sxs-lookup"><span data-stu-id="3c5da-104">The enrollKeyArchivalCMC sample creates a CMC certificate request to archive a private key on a certification authority (CA).</span></span> <span data-ttu-id="3c5da-105">Per altre informazioni, vedere [richiesta di archiviazione delle chiavi CMC](cmc-key-archival-request.md).</span><span class="sxs-lookup"><span data-stu-id="3c5da-105">For more information, see [CMC Key Archival Request](cmc-key-archival-request.md).</span></span>

## <a name="location"></a><span data-ttu-id="3c5da-106">Location</span><span class="sxs-lookup"><span data-stu-id="3c5da-106">Location</span></span>

<span data-ttu-id="3c5da-107">Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollKeyArchivalCMC</span><span class="sxs-lookup"><span data-stu-id="3c5da-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollKeyArchivalCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="3c5da-108">Discussione</span><span class="sxs-lookup"><span data-stu-id="3c5da-108">Discussion</span></span>

<span data-ttu-id="3c5da-109">Esempio enrollKeyArchivalCMC:</span><span class="sxs-lookup"><span data-stu-id="3c5da-109">The enrollKeyArchivalCMC sample:</span></span>

1.  <span data-ttu-id="3c5da-110">Elabora gli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="3c5da-110">Processes the command line arguments.</span></span> <span data-ttu-id="3c5da-111">La riga di comando deve contenere il nome del modello di certificato da usare per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="3c5da-111">The command line should contain the name of the certificate template to use for enrollment.</span></span>
2.  <span data-ttu-id="3c5da-112">Crea un oggetto richiesta di certificato [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e lo inizializza per un contesto dell'utente finale usando il nome del modello.</span><span class="sxs-lookup"><span data-stu-id="3c5da-112">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) certificate request object and initializes it for an end-user context by using the template name.</span></span>
3.  <span data-ttu-id="3c5da-113">Imposta la proprietà [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) nella richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="3c5da-113">Sets the [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) property on the CMC request.</span></span>
4.  <span data-ttu-id="3c5da-114">Crea un oggetto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e lo usa per recuperare una stringa che contiene la configurazione della CA.</span><span class="sxs-lookup"><span data-stu-id="3c5da-114">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
5.  <span data-ttu-id="3c5da-115">Crea un oggetto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) e lo usa per recuperare il certificato di Exchange per l'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="3c5da-115">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it to retrieve the exchange certificate for the CA.</span></span>
6.  <span data-ttu-id="3c5da-116">Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inizializza usando la richiesta CMC, crea una stringa con codifica Base64 che contiene la richiesta di archiviazione delle chiavi e la invia alla CA.</span><span class="sxs-lookup"><span data-stu-id="3c5da-116">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, creates a base64 encoded string that contains the key archival request, and submits it to the CA.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c5da-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c5da-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c5da-118">Richiesta di archiviazione delle chiavi CMC</span><span class="sxs-lookup"><span data-stu-id="3c5da-118">CMC Key Archival Request</span></span>](cmc-key-archival-request.md)
</dt> <dt>

[<span data-ttu-id="3c5da-119">Richiesta CMC</span><span class="sxs-lookup"><span data-stu-id="3c5da-119">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="3c5da-120">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="3c5da-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
