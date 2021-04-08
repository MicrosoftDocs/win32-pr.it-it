---
description: Registra un utente finale con un'autorità di certificazione (CA) usando un modello, il nome del soggetto e la lunghezza in bit della chiave.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050242"
---
# <a name="enrollsimpleusercert"></a><span data-ttu-id="7fe8f-103">enrollSimpleUserCert</span><span class="sxs-lookup"><span data-stu-id="7fe8f-103">enrollSimpleUserCert</span></span>

<span data-ttu-id="7fe8f-104">L'esempio enrollSimpleUserCert registra un utente finale con un'autorità di certificazione (CA) usando un modello, il nome del soggetto e la lunghezza in bit della chiave.</span><span class="sxs-lookup"><span data-stu-id="7fe8f-104">The enrollSimpleUserCert sample enrolls an end user with a certification authority (CA) by using a template, the subject name, and the length, in bits, of the key.</span></span>

## <a name="location"></a><span data-ttu-id="7fe8f-105">Location</span><span class="sxs-lookup"><span data-stu-id="7fe8f-105">Location</span></span>

<span data-ttu-id="7fe8f-106">Quando si installa il Software Development Kit (SDK) di Microsoft Windows, per impostazione predefinita viene installata una versione C++ dell'esempio, nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate di registrazione del certificato \\ VC \\ enrollSimpleUserCert.</span><span class="sxs-lookup"><span data-stu-id="7fe8f-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollSimpleUserCert folder.</span></span> <span data-ttu-id="7fe8f-107">Una versione C# è installata nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ X509 CSharp EnrollSimpleUserCert per la registrazione del certificato \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="7fe8f-107">A C# version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\CSharp\\EnrollSimpleUserCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="7fe8f-108">Discussione</span><span class="sxs-lookup"><span data-stu-id="7fe8f-108">Discussion</span></span>

<span data-ttu-id="7fe8f-109">Esempio enrollSimpleUserCert:</span><span class="sxs-lookup"><span data-stu-id="7fe8f-109">The enrollSimpleUserCert sample:</span></span>

1.  <span data-ttu-id="7fe8f-110">Elabora gli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="7fe8f-110">Processes the command line arguments.</span></span> <span data-ttu-id="7fe8f-111">La riga di comando deve contenere il nome del modello, il nome del soggetto e la lunghezza della chiave.</span><span class="sxs-lookup"><span data-stu-id="7fe8f-111">The command line should contain the name of the template, the subject name, and the key length.</span></span>
2.  <span data-ttu-id="7fe8f-112">Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e lo inizializza usando il modello.</span><span class="sxs-lookup"><span data-stu-id="7fe8f-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template.</span></span>
3.  <span data-ttu-id="7fe8f-113">Recupera l'oggetto richiesta di certificato interno dall'oggetto di registrazione ed esegue una query per l'oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="7fe8f-113">Retrieves the inner certificate request object from the enrollment object and queries it for the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span> <span data-ttu-id="7fe8f-114">La richiesta più interna è sempre una \# richiesta PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="7fe8f-114">The innermost request is always a PKCS \#10 request.</span></span>
4.  <span data-ttu-id="7fe8f-115">Recupera l'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) dalla richiesta PKCS \# 10 e imposta la lunghezza della chiave specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="7fe8f-115">Retrieves the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object from the PKCS \#10 request and sets the key length specified on the command line.</span></span>
5.  <span data-ttu-id="7fe8f-116">Crea un oggetto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , lo utilizza per codificare il nome soggetto X. 500 e aggiunge il nome alla richiesta PKCS \# 10.</span><span class="sxs-lookup"><span data-stu-id="7fe8f-116">Creates an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, uses it to encode the X.500 subject name, and adds the name to the PKCS \#10 request.</span></span>
6.  <span data-ttu-id="7fe8f-117">Tenta di registrare l'utente finale con l'autorità di certificazione e monitora lo stato di avanzamento del processo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="7fe8f-117">Attempts to enroll the end user with the CA and monitors the progress of the enrollment process.</span></span> <span data-ttu-id="7fe8f-118">La funzione checkEnrollStatus è definita in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="7fe8f-118">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fe8f-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fe8f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fe8f-120">\#Richiesta PKCS 10</span><span class="sxs-lookup"><span data-stu-id="7fe8f-120">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="7fe8f-121">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="7fe8f-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



