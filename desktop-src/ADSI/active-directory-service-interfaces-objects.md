---
title: Oggetti delle interfacce del servizio Active Directory
description: Il modello a oggetti ADSI è costituito da oggetti COM. I client modificano gli oggetti con le interfacce. I provider ADSI implementano gli oggetti e le relative interfacce.
ms.assetid: 3c9fd08e-47d6-4b71-8259-7c831d7d95c9
ms.tgt_platform: multiple
keywords:
- oggetti ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20d75454b840597e1fd2ac0599d72d04acb1ee674f84aff40da64f9886879cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181187"
---
# <a name="active-directory-service-interfaces-objects"></a>Oggetti delle interfacce del servizio Active Directory

Il modello a oggetti ADSI è costituito da oggetti COM. I client modificano gli oggetti con le interfacce. I provider ADSI implementano gli oggetti e le relative interfacce.

Gli oggetti ADSI sono oggetti COM che rappresentano un elemento all'interno di un servizio directory: computer, utenti, file, server, stampanti, code di stampa e così via. ciò significa che gli elementi con cui gli amministratori di rete lavorano quotidianamente. ADSI definisce diversi tipi di oggetti per rappresentare tipi diversi di elementi. Ogni oggetto, come illustrato nella figura seguente, supporta una o più interfacce COM che consentono l'accesso ai dati degli oggetti, spesso denominati metadati.

![oggetti delle interfacce del servizio Active Directory](images/ds2objex.png)

Poiché le interfacce COM sono set di proprietà e metodi connessi logicamente, è possibile pensare a ogni interfaccia come a un handle all'oggetto che fornisce l'accesso a un solo set di funzioni logiche alla volta. Nella tabella seguente sono elencati gli elementi ADSI fondamentali.



| Interfaccia            | Descrizione                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IAD**             | Utilizzato per l'identificazione dell'oggetto. Come interfaccia fondamentale necessaria per tutti gli oggetti ADSI, gli [**IAD**](/windows/desktop/api/Iads/nn-iads-iads) fornisce l'accesso ai metadati degli oggetti, inclusa la relativa definizione nello schema ADSI. Gli IAD forniscono inoltre l'accesso alle proprietà e ai metodi che gestiscono i dati degli oggetti nella cache delle proprietà.                                                                                   |
| **IADsContainer**    | Utilizzato per la gestione e il rilevamento di oggetti. Tutti gli oggetti contenitore ADSI richiedono [**l'interfaccia IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) per gestire la creazione, l'eliminazione, la copia e lo spostamento di oggetti, l'associazione e l'enumerazione.                                                                                                                                                                      |
| **IADsPropertyList** | Utilizzato per la gestione delle proprietà degli oggetti. [**L'interfaccia IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) ottimizza la gestione dei dati degli oggetti nella cache delle proprietà.                                                                                                                                                                                                                                |
| **IDirectoryObject** | Usato per l'accesso diretto agli oggetti. [**L'interfaccia IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) fornisce l'accesso agli oggetti di basso livello per i client che non usano Automazione. Questa interfaccia ignora la cache delle proprietà dell'oggetto e fornisce l'accesso diretto alle proprietà dell'oggetto. Per altre informazioni, vedere [Interfacce IADs e IDirectoryObject.](the-iads-and-idirectoryobject-interfaces.md) |
| **IUnknown**         | Utilizzato per la gestione di oggetti COM. [**L'interfaccia IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) è necessaria per tutti gli oggetti COM.                                                                                                                                                                                                                                                                              |
| **Idispatch**        | Usato per i dati della libreria dei tipi e la chiamata al metodo. [**L'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) è necessaria per tutti gli oggetti di automazione.                                                                                                                                                                                                                             |



 

Gli oggetti ADSI più complessi possono esporre interfacce aggiuntive. Ad esempio, [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) supporta metodi che gestiscono raccolte di elementi di directory dello stesso tipo di dati. [**I metodi IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) gestiscono le raccolte di casi speciali di oggetti che supportano [**l'interfaccia IADsMembers.**](/windows/desktop/api/Iads/nn-iads-iadsmembers) Per i provider che la supportano, [**l'interfaccia IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) supporta i metodi per eseguire query nei servizi directory. INOLTRE, ADSI fornisce interfacce che rappresentano elementi logici e fisici noti. Ad esempio, gli oggetti ADSI che rappresentano gli utenti supportano [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), quelli che rappresentano i computer [**supportano IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)e così via. Per altre informazioni sugli oggetti ADSI, vedere [Interfacce IADs e IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md). Non tutti i provider implementano tutte le interfacce o tutti i metodi e le proprietà in tutte le interfacce. Per altre informazioni, vedere Informazioni [di riferimento su ADSI.](adsi-reference.md)

 

 