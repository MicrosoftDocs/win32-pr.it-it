---
description: Crea una richiesta PKCS \# 10 personalizzata e tenta di registrarla in un'autorità di certificazione (CA) dell'organizzazione (Enterprise).
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d20615826bb72b6282144b72a394cde41e35910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308121"
---
# <a name="enrollcustompkcs10_2"></a><span data-ttu-id="b6e70-103">enrollCustomPKCS10 \_ 2</span><span class="sxs-lookup"><span data-stu-id="b6e70-103">enrollCustomPKCS10\_2</span></span>

<span data-ttu-id="b6e70-104">L' \_ esempio enrollCustomPKCS10 2 crea una richiesta PKCS \# 10 personalizzata e tenta di registrarla in un' [*autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CA) dell'organizzazione (Enterprise).</span><span class="sxs-lookup"><span data-stu-id="b6e70-104">The enrollCustomPKCS10\_2 sample creates a custom PKCS \#10 request and attempts to enroll it in an enterprise [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span>

## <a name="location"></a><span data-ttu-id="b6e70-105">Location</span><span class="sxs-lookup"><span data-stu-id="b6e70-105">Location</span></span>

<span data-ttu-id="b6e70-106">Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollCustomPKCS10 \_ 2.</span><span class="sxs-lookup"><span data-stu-id="b6e70-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomPKCS10\_2 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="b6e70-107">Discussione</span><span class="sxs-lookup"><span data-stu-id="b6e70-107">Discussion</span></span>

<span data-ttu-id="b6e70-108">Esempio enrollCustomPKCS10 \_ 2:</span><span class="sxs-lookup"><span data-stu-id="b6e70-108">The enrollCustomPKCS10\_2 sample:</span></span>

1.  <span data-ttu-id="b6e70-109">Elabora gli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b6e70-109">Processes the command line arguments.</span></span> <span data-ttu-id="b6e70-110">La riga di comando deve contenere il nome di un modello e il nome di un provider di crittografia.</span><span class="sxs-lookup"><span data-stu-id="b6e70-110">The command line should contain the name of a template and the name of a cryptographic provider.</span></span>
2.  <span data-ttu-id="b6e70-111">Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e lo inizializza usando il nome del modello specificato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b6e70-111">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the name of the template specified on the command line.</span></span>
3.  <span data-ttu-id="b6e70-112">Recupera la [*richiesta di certificato*](/windows/desktop/SecGloss/c-gly) dall'oggetto di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b6e70-112">Retrieves the [*certificate request*](/windows/desktop/SecGloss/c-gly) from the enrollment object.</span></span>
4.  <span data-ttu-id="b6e70-113">Recupera la richiesta PKCS \# 10 più interna dall'oggetto richiesta di certificato ottenuto nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="b6e70-113">Retrieves the innermost PKCS\#10 request from the certificate request object obtained in step 3.</span></span>
5.  <span data-ttu-id="b6e70-114">Recupera una [*chiave privata*](/windows/desktop/SecGloss/p-gly) dalla richiesta PKCS \# 10.</span><span class="sxs-lookup"><span data-stu-id="b6e70-114">Retrieves a [*private key*](/windows/desktop/SecGloss/p-gly) from the PKCS\#10 request.</span></span>
6.  <span data-ttu-id="b6e70-115">Crea una raccolta [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) e aggiunge i provider di crittografia disponibili alla raccolta e quindi recupera un oggetto [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) per il provider specificato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b6e70-115">Creates an [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) collection and adds the available cryptographic providers to the collection and then retrieves an [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) object for the provider specified on the command line.</span></span>
7.  <span data-ttu-id="b6e70-116">Imposta l'oggetto stato sulla chiave privata.</span><span class="sxs-lookup"><span data-stu-id="b6e70-116">Sets the status object on the private key.</span></span>
8.  <span data-ttu-id="b6e70-117">Tenta di registrare la [*richiesta di certificato*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="b6e70-117">Attempts to enroll the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6e70-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6e70-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6e70-119">\#Richiesta PKCS 10</span><span class="sxs-lookup"><span data-stu-id="b6e70-119">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="b6e70-120">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="b6e70-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
