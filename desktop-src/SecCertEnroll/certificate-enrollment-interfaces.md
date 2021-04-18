---
description: Le interfacce seguenti possono essere utilizzate per registrare un utente o un computer in una gerarchia di certificati.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Interfacce di registrazione certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318961"
---
# <a name="certificate-enrollment-interfaces"></a>Interfacce di registrazione certificati

Le interfacce seguenti possono essere utilizzate per registrare un utente o un computer in una gerarchia di certificati.



| Interfaccia                                              | Descrizione                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | Registra un computer o un utente in una gerarchia di certificati.                                                                                                                              |
| [**IX509Enrollment2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | Estende l'interfaccia [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per abilitare l'inizializzazione da un modello.                                                                          |
| [**IX509EnrollmentHelper**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | Definisce i metodi che consentono a un'applicazione Web di registrare un certificato, archiviare le credenziali del server dei criteri nella cache delle credenziali e registrare i server dei criteri e i server di registrazione. |
| [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | Recupera informazioni dettagliate sugli errori relativi a una transazione di registrazione del certificato.                                                                                                    |
| [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | Interfaccia del protocollo di registrazione del computer semplice X. 509<br/>                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 




