---
title: Oggetti ADSI di WinNT
description: Il provider ADSI WinNT implementa gli oggetti COM seguenti per supportare le funzionalità e i servizi di varie interfacce ADSI.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- Oggetti ADSI ,ADSI del provider di servizi WinNT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f3d2cb845e7fa6c754198abbb9a274987f69a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467388"
---
# <a name="adsi-objects-of-winnt"></a>Oggetti ADSI di WinNT

Il provider ADSI WinNT implementa gli oggetti COM seguenti per supportare le funzionalità e i servizi di varie interfacce ADSI.




| Oggetto ADSI | Descrizione | Interfacce supportate | 
|-------------|-------------|----------------------|
| <strong>Classe</strong> | Oggetto ADSI che rappresenta una definizione di classe. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>IADsClass</strong></a></dt></dl> | 
| <strong>Computer</strong> | Oggetto ADSI che rappresenta un computer. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>Dominio</strong> | Oggetto ADSI che rappresenta un dominio in rete. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FileService</strong> | Oggetto ADSI che rappresenta un servizio file. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FileShare</strong> | Oggetto ADSI che rappresenta una condivisione file. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWFileService</strong> | Oggetto ADSI che rappresenta un servizio file. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt></dl> | 
| <strong>FPNWFileShare</strong> | Oggetto ADSI che rappresenta una condivisione file. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWResource</strong> | Oggetto ADSI che rappresenta una risorsa. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWResourcesCollection</strong> | Oggetto ADSI che rappresenta una raccolta di risorse. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>FPNWSession</strong> | Oggetto ADSI che rappresenta una sessione. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWSessionsCollection</strong> | Oggetto ADSI che rappresenta una raccolta di sessioni. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>Gruppo</strong> | Oggetto ADSI che rappresenta un gruppo. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADsGroup</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong></strong></a></dt></dl><blockquote>[!Note]<br />Non è possibile usare GetInfo per i gruppi che contengono membri che sono entità di sicurezza noti nell'ambito WinNT.</blockquote><br /> | 
| <strong>Groupcollection</strong> | Oggetto ADSI che rappresenta una raccolta di gruppi. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt></dl> | 
| <strong>Localgroup</strong> | Oggetto ADSI che rappresenta un gruppo locale. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADsGroup</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong></strong></a></dt></dl> | 
| <strong>LocalgroupCollection</strong> | Oggetto ADSI che rappresenta una raccolta di gruppi locali. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt></dl> | 
| <strong>Namespace</strong> | Oggetto ADSI che rappresenta lo spazio dei nomi WinNT. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt></dl> | 
| <strong>Printjob</strong> | Oggetto ADSI che rappresenta un processo di stampa. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>PrintJobsCollection</strong> | Oggetto ADSI che rappresenta una raccolta di processi di stampa. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>PrintQueue</strong> | Oggetto ADSI che rappresenta una coda di stampa. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>Proprietà</strong> | Oggetto ADSI che rappresenta una definizione di attributo. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"><strong>IADsProperty</strong></a></dt></dl> | 
| <strong>Risorsa</strong> | Oggetto ADSI che rappresenta una risorsa. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>ResourcesCollection</strong> | Oggetto ADSI che rappresenta una raccolta di risorse. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>Schema</strong> | Oggetto ADSI che rappresenta il contenitore dello schema. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt></dl> | 
| <strong>Servizio</strong> | Oggetto ADSI che rappresenta un servizio. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADsService</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong></strong></a></dt></dl> | 
| <strong>Sessione</strong> | Oggetto ADSI che rappresenta una sessione. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>SessionsCollection</strong> | Oggetto ADSI che rappresenta una raccolta di sessioni. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>Sintassi</strong> | Oggetto ADSI che rappresenta la sintassi di un attributo. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"><strong>IADsSyntax</strong></a></dt></dl> | 
| <strong>Utente</strong> | Oggetto ADSI che rappresenta un account utente. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>UserGroupCollection</strong> | Oggetto ADSI che rappresenta una raccolta di gruppi di utenti. | <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a> | 




 

 

 





