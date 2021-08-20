---
title: Lettura di defaultSecurityDescriptor per una classe object
description: Usando ADSI, è possibile ottenere l'attributo defaultSecurityDescriptor per una classe di oggetti con l'interfaccia IADs.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory , lettura di defaultSecurityDescriptor per una classe di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26204ebe31155363a1be8bf30bd1c0495d16a939b58789f421a0772d6d90a9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184692"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a>Lettura di defaultSecurityDescriptor per una classe object

Usando ADSI, è possibile ottenere **l'attributo defaultSecurityDescriptor** per una classe di oggetti con [**l'interfaccia IADs.**](/windows/desktop/api/iads/nn-iads-iads) Per ottenere **l'attributo defaultSecurityDescriptor** per una classe di oggetti, seguire questa procedura.

1.  Ottenere un puntatore a interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) all'oggetto **classSchema** per la classe di oggetti.
2.  Usare il [**metodo IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) per ottenere il descrittore di sicurezza predefinito dell'oggetto. Il nome della proprietà che contiene il descrittore di sicurezza è "defaultSecurityDescriptor". La proprietà verrà restituita come [**VARIANT contenente**](/windows/win32/api/oaidl/ns-oaidl-variant) un BSTR con il descrittore di sicurezza predefinito in formato stringa SDDL.
3.  Usare la [**funzione ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) per convertire il formato stringa SDDL in un descrittore di sicurezza.
4.  Usare le API di sicurezza [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)e [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) per leggere le parti del descrittore di sicurezza.

Per un esempio di codice che illustra come eseguire questa operazione, vedere [Codice di esempio per la lettura di defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).

 

 