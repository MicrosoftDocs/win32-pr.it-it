---
description: Le interfacce seguenti possono essere usate per registrare un utente o un computer in una gerarchia di certificati.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Interfacce di registrazione certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb71c1240791e26781797b547b0a62aaad1612a2bce06738cecfa02c8173b215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902742"
---
# <a name="certificate-enrollment-interfaces"></a>Interfacce di registrazione certificati

Le interfacce seguenti possono essere usate per registrare un utente o un computer in una gerarchia di certificati.



| Interfaccia                                              | Descrizione                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | Registra un computer o un utente in una gerarchia di certificati.                                                                                                                              |
| [**IX509Enrollment2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | Estende [**l'interfaccia IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per abilitare l'inizializzazione da un modello.                                                                          |
| [**IX509EnrollmentHelper**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | Definisce i metodi che consentono a un'applicazione Web di registrare un certificato, archiviare le credenziali del server dei criteri nella cache delle credenziali e registrare i server dei criteri e i server di registrazione. |
| [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | Recupera informazioni dettagliate sull'errore relative a una transazione di registrazione certificati.                                                                                                    |
| [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | X.509 Simple Computer Enrollment Protocol Interface<br/>                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 




