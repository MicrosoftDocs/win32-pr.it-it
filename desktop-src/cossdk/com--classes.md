---
description: Di seguito sono riportate le classi COM+.
ms.assetid: 236725f6-16a3-4209-a9e3-a127c1d7243a
title: Classi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626c3dfdae542b602cf27a8d8be5cb69dde5910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127802"
---
# <a name="com-classes"></a>Classi COM+

Di seguito sono riportate le classi COM+.



| Classe                                                            | Descrizione                                                                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppDomainHelper**](appdomainhelper.md)                       | Associa un oggetto gestito a un dominio dell'applicazione, che è un ambiente isolato in cui vengono eseguite le applicazioni.                                                                                                                           |
| [**ClrAssemblyLocator**](clrassemblylocator.md)                 | Recupera le informazioni su un assembly quando si utilizza codice gestito nel Common Language Runtime .NET Framework.                                                                                                                          |
| [**CServiceConfig**](cserviceconfig.md)                         | Specifica e configura i servizi che devono essere attivi nel dominio del servizio immesso quando si chiama [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) o [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).                     |
| [**SecurityCallContext**](securitycallcontext.md)               | Consente di accedere al contesto di sicurezza della chiamata corrente, che contiene informazioni sui chiamanti di un oggetto.                                                                                                                           |
| [**SecurityCallers**](securitycallers.md)                       | Consente di accedere alle informazioni sui singoli chiamanti in una raccolta di chiamanti. La raccolta rappresenta la catena di chiamate che terminano con la chiamata corrente e ogni chiamante della raccolta rappresenta l'identità di un chiamante. |
| [**SecurityIdentity**](securityidentity.md)                     | Consente di accedere a una raccolta di informazioni di sicurezza che rappresenta l'identità di un chiamante. Utilizzando questa classe, è possibile trovare informazioni su un particolare chiamante in una catena di chiamanti che fa parte del contesto di chiamata di sicurezza.                 |
| [**SharedProperty**](sharedproperty.md)                         | Imposta o Recupera il valore di una proprietà condivisa.                                                                                                                                                                                       |
| [**SharedPropertyGroup**](sharedpropertygroup.md)               | Consente di creare e accedere alle proprietà condivise in un gruppo di proprietà condivise.                                                                                                                                                                  |
| [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) | Crea gruppi di proprietà condivisi e per ottenere l'accesso ai gruppi di proprietà condivisi esistenti.                                                                                                                                                 |
| [**TransactionContext**](transactioncontext.md)                 | Crea un oggetto transazionale generico che avvia una transazione.                                                                                                                                                                       |
| [**TransactionContextEx**](transactioncontextex.md)             | Crea un oggetto transazionale generico che avvia una transazione. Chiamando i metodi di questa classe, è possibile comporre il lavoro di più oggetti COM in una singola transazione e confermare o interrompere in modo esplicito la transazione.        |



 

 

 



