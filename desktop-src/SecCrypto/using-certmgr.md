---
description: Utilizzare CertMgr per visualizzare certificati, CRL e scopi consentiti da un file o da un archivio certificati, per copiare i certificati in un archivio certificati, per eliminare certificati da un archivio certificati e per salvare i certificati nei file.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Utilizzo di CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308639"
---
# <a name="using-certmgr"></a><span data-ttu-id="9fd3e-103">Utilizzo di CertMgr</span><span class="sxs-lookup"><span data-stu-id="9fd3e-103">Using CertMgr</span></span>

<span data-ttu-id="9fd3e-104">[Certmgr](certmgr.md) può essere utilizzato per visualizzare [*certificati*](../secgloss/c-gly.md), [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL) ed [*elenchi di certificati attendibili*](../secgloss/c-gly.md) (scopi consentiti) da un file o un archivio certificati, per copiare i certificati in un [*archivio certificati*](../secgloss/c-gly.md), per eliminare certificati da un archivio certificati e per salvare i certificati nei file.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-104">[CertMgr](certmgr.md) can be used to view [*certificates*](../secgloss/c-gly.md), [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) from a file or a certificate store, to copy certificates into a [*certificate store*](../secgloss/c-gly.md), to delete certificates from a certificate store, and to save certificates to files.</span></span>

<span data-ttu-id="9fd3e-105">Quando [certmgr](certmgr.md) viene utilizzato senza opzioni, viene visualizzata una procedura guidata di certmgr per guidare l'utente durante l'operazione.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-105">When [CertMgr](certmgr.md) is used without options, a CertMgr wizard appears to guide the user through the operation.</span></span>

<span data-ttu-id="9fd3e-106">Il file deve essere uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9fd3e-106">The file must be one of the following types:</span></span>

-   <span data-ttu-id="9fd3e-107">Un file CTL, CRL o certificate codificato (potrebbe essere codificato in base 64)</span><span class="sxs-lookup"><span data-stu-id="9fd3e-107">An encoded CTL, CRL, or certificate file (could be base-64 encoded)</span></span>
-   <span data-ttu-id="9fd3e-108">Un \# file PKCS 7</span><span class="sxs-lookup"><span data-stu-id="9fd3e-108">A PKCS \#7 file</span></span>
-   <span data-ttu-id="9fd3e-109">Un file SPC</span><span class="sxs-lookup"><span data-stu-id="9fd3e-109">An SPC file</span></span>
-   <span data-ttu-id="9fd3e-110">Documento firmato</span><span class="sxs-lookup"><span data-stu-id="9fd3e-110">A signed document</span></span>
-   <span data-ttu-id="9fd3e-111">StoreFile serializzato</span><span class="sxs-lookup"><span data-stu-id="9fd3e-111">A serialized storeFile</span></span>

<span data-ttu-id="9fd3e-112">Negli esempi seguenti vengono utilizzati i comandi [certmgr](certmgr.md) per eseguire attività comuni relative ai certificati.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-112">The following examples use [CertMgr](certmgr.md) commands to perform common certificate tasks.</span></span>

-   <span data-ttu-id="9fd3e-113">Visualizzare i certificati, i CRL e scopi consentiti da *MyFile. ext*.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-113">View the certificates, CRLs, and CTLs from *MyFile.ext*.</span></span>

    <span data-ttu-id="9fd3e-114">**certmgr** *MyFile. ext*</span><span class="sxs-lookup"><span data-stu-id="9fd3e-114">**certmgr** *MyFile.ext*</span></span>

-   <span data-ttu-id="9fd3e-115">Visualizzare i certificati, i CRL e scopi consentiti dall'archivio di sistema.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-115">View the certificates, CRLs, and CTLs from the MY system store.</span></span>

    <span data-ttu-id="9fd3e-116">**certmgr-s My**</span><span class="sxs-lookup"><span data-stu-id="9fd3e-116">**certmgr -s my**</span></span>

-   <span data-ttu-id="9fd3e-117">Copiare tutti i certificati, i CRL e scopi consentiti in un file denominato MyFile *. ext* in un nuovo file, denominato *NewFile. ext*.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-117">Copy all the certificates, CRLs, and CTLs in a file named *MyFile.ext* to a new file, called *NewFile.ext*.</span></span>

    <span data-ttu-id="9fd3e-118">**certmgr-Add-All-c** *MyFile. ext* *NewFile. ext*</span><span class="sxs-lookup"><span data-stu-id="9fd3e-118">**certmgr -add -all -c** *MyFile.ext* *NewFile.ext*</span></span>

-   <span data-ttu-id="9fd3e-119">Copiare tutti i certificati, i CRL e scopi consentiti dall'archivio di sistema in un file denominato *NewMyFile. ext*.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-119">Copy all the certificates, CRLs, and CTLs from the MY system store to a file called *NewMyFile.ext*.</span></span>

    <span data-ttu-id="9fd3e-120">**certmgr-Add-All-c-s My** *NewMyFile. ext*</span><span class="sxs-lookup"><span data-stu-id="9fd3e-120">**certmgr -add -all -c -s my** *NewMyFile.ext*</span></span>

-   <span data-ttu-id="9fd3e-121">Copiare un certificato con il nome comune *CERT* nell'archivio di sistema in un file denominato *NewCert. cer*.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-121">Copy a certificate with the common name *MyCert* in the MY system store to a file called *NewCert.cer*.</span></span>

    <span data-ttu-id="9fd3e-122">**certmgr-Add-c-n** *CERT* **-s My** *NewCert. cer*</span><span class="sxs-lookup"><span data-stu-id="9fd3e-122">**certmgr -add -c -n** *MyCert* **-s my** *NewCert.cer*</span></span>

-   <span data-ttu-id="9fd3e-123">Eliminare tutti i certificati dall'archivio di sistema.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-123">Delete all the certificates from the MY system store.</span></span>

    <span data-ttu-id="9fd3e-124">**certmgr-del-all-c-s My**</span><span class="sxs-lookup"><span data-stu-id="9fd3e-124">**certmgr -del -all -c -s my**</span></span>

-   <span data-ttu-id="9fd3e-125">Eliminare tutti i scopi consentiti dall'archivio di sistema personale e salvare l'archivio risultante in un file denominato *NewStore. Str*.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-125">Delete all the CTLs from the MY system store and save the resulting store to a file called *NewStore.str*.</span></span>

    <span data-ttu-id="9fd3e-126">**certmgr-del-all-CTL-s My** *NewStore. Str*</span><span class="sxs-lookup"><span data-stu-id="9fd3e-126">**certmgr -del -all -ctl -s my** *NewStore.str*</span></span>

-   <span data-ttu-id="9fd3e-127">Salvare, in un file denominato *NewCert. cer*, un certificato con codifica [*X. 509*](../secgloss/x-gly.md) , che ha il nome comune *CERT* e che si trova nell'archivio certificati radice.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-127">Save, to a file called *NewCert.cer*, a certificate that is an [*X.509*](../secgloss/x-gly.md) encoded certificate, that has the common name *MyCert*, and that is located in the Root certificate store.</span></span>

    <span data-ttu-id="9fd3e-128">**certmgr-put-c-n** *CERT* **-s root** *NewCert. cer*</span><span class="sxs-lookup"><span data-stu-id="9fd3e-128">**certmgr -put -c -n** *MyCert* **-s root** *NewCert.cer*</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fd3e-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9fd3e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fd3e-130">CertMgr</span><span class="sxs-lookup"><span data-stu-id="9fd3e-130">CertMgr</span></span>](certmgr.md)
</dt> </dl>

 

 
