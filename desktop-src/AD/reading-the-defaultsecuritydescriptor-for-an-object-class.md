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
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a>Lettura di defaultSecurityDescriptor per una classe di oggetti

Utilizzando ADSI, è possibile ottenere l'attributo **defaultSecurityDescriptor** per una classe di oggetti con l'interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) . Per ottenere l'attributo **defaultSecurityDescriptor** per una classe di oggetti, seguire questa procedura.

1.  Ottenere un puntatore all'interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) per l'oggetto **classSchema** per la classe dell'oggetto.
2.  Usare il metodo [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) per ottenere il descrittore di sicurezza predefinito dell'oggetto. Il nome della proprietà che contiene il descrittore di sicurezza è "defaultSecurityDescriptor". La proprietà verrà restituita come [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contenente un BSTR con il descrittore di sicurezza predefinito in formato stringa SDDL.
3.  Utilizzare la funzione [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) per convertire il formato stringa SDDL in un descrittore di sicurezza.
4.  Utilizzare le API di sicurezza [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)e [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) per leggere le parti del descrittore di sicurezza.

Per un esempio di codice che illustra come eseguire questa operazione, vedere il [codice di esempio per la lettura di defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).

 

 