---
description: Per creare una proprietà del certificato, è possibile usare le interfacce seguenti.
ms.assetid: c64fca58-fb2f-412f-b7c0-5db1979d051b
title: Interfacce di proprietà del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d0052675436a28438d5f1600a5b0097f8e177a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749578"
---
# <a name="certificate-property-interfaces"></a>Interfacce di proprietà del certificato

Per creare una proprietà del certificato, è possibile usare le interfacce seguenti.



| Interfaccia                                                                          | Descrizione                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertProperties**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperties)                                         | Gestire una raccolta di oggetti [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) .                                                                                                                                                                                    |
| [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                             | Associa una proprietà esterna a un certificato.                                                                                                                                                                                                       |
| [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)                             | Rappresenta una proprietà del certificato che indica se un certificato è stato archiviato.                                                                                                                                                                |
| [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)               | Rappresenta un hash SHA-1 di una chiave privata crittografata inviata a un'autorità di certificazione per l'archiviazione.                                                                                                                                                  |
| [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)                         | Rappresenta una proprietà del certificato che identifica un modello configurato per consentire la registrazione automatica del certificato.                                                                                                                        |
| [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)                             | Rappresenta una proprietà del certificato che indica se è stato eseguito il backup di un certificato e, in caso affermativo, la data e l'ora in cui è stato salvato.                                                                                                               |
| [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)                       | Consente di specificare e recuperare una stringa che contiene informazioni descrittive per un certificato.                                                                                                                                                     |
| [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)                         | Rappresenta una proprietà del certificato che contiene le informazioni sul certificato e sull'autorità di certificazione create quando il client chiama il metodo di [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) sull'interfaccia [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . |
| [**ICertPropertyEnrollmentPolicyServer**](/windows/desktop/api/Certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver) | Rappresenta una proprietà del certificato esterna che contiene informazioni su un server del criterio di registrazione certificati (CEP) e un server di registrazione certificati (CES).                                                                                       |
| [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)                     | Consente di specificare e recuperare una stringa che contiene il nome visualizzato di un certificato.                                                                                                                                                             |
| [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)                       | Rappresenta una proprietà del certificato che contiene informazioni su una chiave privata.                                                                                                                                                                          |
| [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)                               | Rappresenta una proprietà del certificato che contiene un hash SHA-1 del nuovo certificato creato quando un certificato esistente viene rinnovato.                                                                                                                      |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Rappresenta una proprietà del certificato che contiene il nome DNS (Domain Naming System) del computer in cui è stata creata la richiesta.                                                                                                                     |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Rappresenta una proprietà del certificato che contiene il nome DNS (Domain Naming System) del computer in cui è stata creata la richiesta.                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



