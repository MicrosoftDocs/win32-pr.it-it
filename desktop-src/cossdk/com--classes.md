---
description: Di seguito sono riportate le classi COM+.
ms.assetid: 236725f6-16a3-4209-a9e3-a127c1d7243a
title: Classi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2cdabc1f4535df6734cf525f288bf6cbd8a93543a9163848815441c9bc384c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129223"
---
# <a name="com-classes"></a>Classi COM+

Di seguito sono riportate le classi COM+.



| Classe                                                            | Descrizione                                                                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppDomainHelper**](appdomainhelper.md)                       | Associa un oggetto gestito a un dominio applicazione, ovvero un ambiente isolato in cui vengono eseguite le applicazioni.                                                                                                                           |
| [**ClrAssemblyLocator**](clrassemblylocator.md)                 | Recupera informazioni su un assembly quando si usa codice gestito nel .NET Framework Common Language Runtime.                                                                                                                          |
| [**CServiceConfig**](cserviceconfig.md)                         | Specifica e configura i servizi che devono essere attivi nel dominio del servizio immesso quando si chiama [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) o [**CoEnterServiceDomain.**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)                     |
| [**SecurityCallContext**](securitycallcontext.md)               | Fornisce l'accesso al contesto di sicurezza della chiamata corrente, che contiene informazioni sui chiamanti di un oggetto.                                                                                                                           |
| [**SecurityCallers**](securitycallers.md)                       | Fornisce l'accesso alle informazioni sui singoli chiamanti in una raccolta di chiamanti. La raccolta rappresenta la catena di chiamate che termina con la chiamata corrente e ogni chiamante nella raccolta rappresenta l'identità di un chiamante. |
| [**SecurityIdentity**](securityidentity.md)                     | Fornisce l'accesso a una raccolta di informazioni di sicurezza che rappresentano l'identità di un chiamante. Usando questa classe, è possibile trovare informazioni su un determinato chiamante in una catena di chiamanti che fa parte del contesto della chiamata di sicurezza.                 |
| [**Proprietà condivisa**](sharedproperty.md)                         | Imposta o recupera il valore di una proprietà condivisa.                                                                                                                                                                                       |
| [**SharedPropertyGroup**](sharedpropertygroup.md)               | Crea e accede alle proprietà condivise in un gruppo di proprietà condivise.                                                                                                                                                                  |
| [**Sharedpropertygroupmanager**](sharedpropertygroupmanager.md) | Crea gruppi di proprietà condivise e per ottenere l'accesso ai gruppi di proprietà condivise esistenti.                                                                                                                                                 |
| [**Transactioncontext**](transactioncontext.md)                 | Crea un oggetto transazionale generico che inizia una transazione.                                                                                                                                                                       |
| [**TransactionContextEx**](transactioncontextex.md)             | Crea un oggetto transazionale generico che inizia una transazione. Chiamando i metodi di questa classe, è possibile comporre il lavoro di più oggetti COM in una singola transazione ed eseguire in modo esplicito il commit o l'interruzione della transazione.        |



 

 

 



