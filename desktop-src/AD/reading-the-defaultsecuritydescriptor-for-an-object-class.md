---
title: Lettura di defaultSecurityDescriptor per una classe di oggetti
description: Utilizzando ADSI, è possibile ottenere l'attributo defaultSecurityDescriptor per una classe di oggetti con l'interfaccia IADs.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, lettura di defaultSecurityDescriptor per una classe di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e217ae42214c2c07867c2a57427d74fb7636736
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046492"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a><span data-ttu-id="9b7c0-104">Lettura di defaultSecurityDescriptor per una classe di oggetti</span><span class="sxs-lookup"><span data-stu-id="9b7c0-104">Reading the defaultSecurityDescriptor for an Object Class</span></span>

<span data-ttu-id="9b7c0-105">Utilizzando ADSI, è possibile ottenere l'attributo **defaultSecurityDescriptor** per una classe di oggetti con l'interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="9b7c0-105">Using ADSI, you can obtain the **defaultSecurityDescriptor** attribute for an object class with the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="9b7c0-106">Per ottenere l'attributo **defaultSecurityDescriptor** per una classe di oggetti, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-106">To obtain the **defaultSecurityDescriptor** attribute for an object class, perform the following steps.</span></span>

1.  <span data-ttu-id="9b7c0-107">Ottenere un puntatore all'interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) per l'oggetto **classSchema** per la classe dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-107">Get an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface pointer to the **classSchema** object for the object class.</span></span>
2.  <span data-ttu-id="9b7c0-108">Usare il metodo [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) per ottenere il descrittore di sicurezza predefinito dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-108">Use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to get the default security descriptor of the object.</span></span> <span data-ttu-id="9b7c0-109">Il nome della proprietà che contiene il descrittore di sicurezza è "defaultSecurityDescriptor".</span><span class="sxs-lookup"><span data-stu-id="9b7c0-109">The name of the property that contains the security descriptor is "defaultSecurityDescriptor".</span></span> <span data-ttu-id="9b7c0-110">La proprietà verrà restituita come [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contenente un BSTR con il descrittore di sicurezza predefinito in formato stringa SDDL.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-110">The property will be returned as a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) containing a BSTR with the default security descriptor in SDDL string format.</span></span>
3.  <span data-ttu-id="9b7c0-111">Utilizzare la funzione [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) per convertire il formato stringa SDDL in un descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-111">Use the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL string form to a security descriptor.</span></span>
4.  <span data-ttu-id="9b7c0-112">Utilizzare le API di sicurezza [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)e [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) per leggere le parti del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-112">Use the [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner), and [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) Security APIs to read the parts of the security descriptor.</span></span>

<span data-ttu-id="9b7c0-113">Per un esempio di codice che illustra come eseguire questa operazione, vedere il [codice di esempio per la lettura di defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="9b7c0-113">For a code example that demonstrates how to do this, see [Example Code for Reading defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).</span></span>

 

 