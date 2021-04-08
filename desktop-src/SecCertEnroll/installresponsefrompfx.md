---
description: Installa un certificato registrato da un file PFX (Personal Information Exchange) nell'archivio certificati.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968215"
---
# <a name="installresponsefrompfx"></a><span data-ttu-id="555e5-103">installResponseFromPFX</span><span class="sxs-lookup"><span data-stu-id="555e5-103">installResponseFromPFX</span></span>

<span data-ttu-id="555e5-104">L'esempio installResponseFromPFX installa un certificato registrato da un file PFX (Personal Information Exchange) nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="555e5-104">The installResponseFromPFX sample installs an enrolled certificate from a Personal Information Exchange (PFX) file to the certificate store.</span></span>

## <a name="location"></a><span data-ttu-id="555e5-105">Location</span><span class="sxs-lookup"><span data-stu-id="555e5-105">Location</span></span>

<span data-ttu-id="555e5-106">Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ installResponseFromPFX</span><span class="sxs-lookup"><span data-stu-id="555e5-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\installResponseFromPFX folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="555e5-107">Discussione</span><span class="sxs-lookup"><span data-stu-id="555e5-107">Discussion</span></span>

<span data-ttu-id="555e5-108">Esempio installResponseFromPFX:</span><span class="sxs-lookup"><span data-stu-id="555e5-108">The installResponseFromPFX sample:</span></span>

1.  <span data-ttu-id="555e5-109">Elabora gli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="555e5-109">Processes the command line arguments.</span></span> <span data-ttu-id="555e5-110">La riga di comando deve contenere:</span><span class="sxs-lookup"><span data-stu-id="555e5-110">The command line should contain:</span></span>
    -   <span data-ttu-id="555e5-111">Nome dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="555e5-111">The name of the sample.</span></span>
    -   <span data-ttu-id="555e5-112">Nome del file PFX contenente il certificato registrato.</span><span class="sxs-lookup"><span data-stu-id="555e5-112">The name of the PFX file that contains the enrolled certificate.</span></span>
    -   <span data-ttu-id="555e5-113">Password associata al file PFX.</span><span class="sxs-lookup"><span data-stu-id="555e5-113">A password associated with the PFX file.</span></span>
2.  <span data-ttu-id="555e5-114">Legge il file PFX, provando prima il formato Base64 e il formato binario se Base64 ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="555e5-114">Reads the PFX file, trying the base64 format first and the binary format if base64 fails.</span></span> <span data-ttu-id="555e5-115">La funzione DecodeFileW () è definita in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="555e5-115">The DecodeFileW() function is defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="555e5-116">Converte il certificato registrato in un **BSTR** e lo usa per inizializzare un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .</span><span class="sxs-lookup"><span data-stu-id="555e5-116">Converts the enrolled certificate to a **BSTR** and uses it to initialize an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object.</span></span> <span data-ttu-id="555e5-117">La funzione convertWszToBstr è definita in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="555e5-117">The convertWszToBstr function is defined in enrollCommon.cpp.</span></span>
4.  <span data-ttu-id="555e5-118">Installa il certificato nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="555e5-118">Installs the certificate in the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="555e5-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="555e5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="555e5-120">enrollEOBOCMC</span><span class="sxs-lookup"><span data-stu-id="555e5-120">enrollEOBOCMC</span></span>](enrolleobocmc.md)
</dt> <dt>

[<span data-ttu-id="555e5-121">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="555e5-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



