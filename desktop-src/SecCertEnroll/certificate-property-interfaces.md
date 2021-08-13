---
description: Le interfacce seguenti possono essere usate per creare una proprietà del certificato.
ms.assetid: c64fca58-fb2f-412f-b7c0-5db1979d051b
title: Interfacce delle proprietà del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e3d0ab8d9f8e9bb73d47b7e112dfa0ff6fb11f70031c64405b660ee5096dd78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902607"
---
# <a name="certificate-property-interfaces"></a>Interfacce delle proprietà del certificato

Le interfacce seguenti possono essere usate per creare una proprietà del certificato.



| Interfaccia                                                                          | Descrizione                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertProperties**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperties)                                         | Gestire una raccolta di [**oggetti ICertProperty.**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                                                                                                                                                                    |
| [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                             | Associa una proprietà esterna a un certificato.                                                                                                                                                                                                       |
| [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)                             | Rappresenta una proprietà del certificato che identifica se un certificato è stato archiviato.                                                                                                                                                                |
| [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)               | Rappresenta un hash SHA-1 di una chiave privata crittografata inviata a un'autorità di certificazione per l'archiviazione.                                                                                                                                                  |
| [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)                         | Rappresenta una proprietà del certificato che identifica un modello configurato per abilitare la registrazione automatica del certificato.                                                                                                                        |
| [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)                             | Rappresenta una proprietà del certificato che identifica se è stato eseguito il backup di un certificato e, in tal caso, la data e l'ora in cui è stato salvato.                                                                                                               |
| [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)                       | Consente di specificare e recuperare una stringa contenente informazioni descrittive per un certificato.                                                                                                                                                     |
| [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)                         | Rappresenta una proprietà del certificato che contiene le informazioni sul certificato e sull'autorità di certificazione create quando il client chiama il [**metodo Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) nell'interfaccia [**IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) |
| [**ICertPropertyEnrollmentPolicyServer**](/windows/desktop/api/Certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver) | Rappresenta una proprietà del certificato esterno che contiene informazioni su un server dei criteri di registrazione certificati (CEP) e un server di registrazione certificati (CES).                                                                                       |
| [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)                     | Consente di specificare e recuperare una stringa contenente il nome visualizzato di un certificato.                                                                                                                                                             |
| [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)                       | Rappresenta una proprietà del certificato che contiene informazioni su una chiave privata.                                                                                                                                                                          |
| [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)                               | Rappresenta una proprietà del certificato che contiene un hash SHA-1 del nuovo certificato creato al rinnovo di un certificato esistente.                                                                                                                      |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Rappresenta una proprietà del certificato che contiene il nome DNS (Domain Naming System) del computer in cui è stata creata la richiesta.                                                                                                                     |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Rappresenta una proprietà del certificato che contiene il nome DNS (Domain Naming System) del computer in cui è stata creata la richiesta.                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



