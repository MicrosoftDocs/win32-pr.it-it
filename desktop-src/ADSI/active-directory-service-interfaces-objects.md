---
title: Oggetti interfacce del servizio Active Directory
description: Il modello a oggetti ADSI è costituito da oggetti COM. I client modificano gli oggetti con le interfacce. I provider ADSI implementano gli oggetti e le relative interfacce.
ms.assetid: 3c9fd08e-47d6-4b71-8259-7c831d7d95c9
ms.tgt_platform: multiple
keywords:
- oggetti ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e356d9b1212b448d16bb6bba081f6141a877b0b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872950"
---
# <a name="active-directory-service-interfaces-objects"></a>Oggetti interfacce del servizio Active Directory

Il modello a oggetti ADSI è costituito da oggetti COM. I client modificano gli oggetti con le interfacce. I provider ADSI implementano gli oggetti e le relative interfacce.

Gli oggetti ADSI sono oggetti COM che rappresentano un elemento in un servizio directory: computer, utenti, file, server, stampanti, code di stampa e così via. ovvero gli elementi che gli amministratori di rete utilizzano quotidianamente. ADSI definisce diversi tipi di oggetti per rappresentare tipi diversi di elementi. Ogni oggetto, come illustrato nella figura seguente, supporta una o più interfacce COM che consentono l'accesso ai dati dell'oggetto, spesso denominati metadati.

![oggetti interfacce del servizio Active Directory](images/ds2objex.png)

Poiché le interfacce COM sono set di proprietà e metodi connessi logicamente, è possibile considerare ogni interfaccia come un handle per l'oggetto che fornisce l'accesso a un solo set di funzioni logiche alla volta. Nella tabella seguente sono elencati gli elementi ADSI di base.



| Interfaccia            | Descrizione                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IADs**             | Utilizzato per l'identificazione dell'oggetto. Come l'interfaccia fondamentale necessaria per tutti gli oggetti ADSI, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) fornisce l'accesso ai metadati degli oggetti, inclusa la relativa definizione nello schema ADSI. IADs fornisce anche l'accesso alle proprietà e ai metodi che gestiscono i dati degli oggetti nella cache delle proprietà.                                                                                   |
| **IADsContainer**    | Utilizzato per la gestione e il rilevamento degli oggetti. Tutti gli oggetti contenitore ADSI richiedono l'interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) per gestire la creazione, l'eliminazione, la copia e lo sviluppo di oggetti, l'associazione e l'enumerazione.                                                                                                                                                                      |
| **IADsPropertyList** | Utilizzato per la gestione delle proprietà degli oggetti. L'interfaccia [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) ottimizza la gestione dei dati oggetto nella cache delle proprietà.                                                                                                                                                                                                                                |
| **IDirectoryObject** | Utilizzato per l'accesso diretto agli oggetti. L'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) fornisce l'accesso agli oggetti di basso livello per i client che non usano l'automazione. Questa interfaccia ignora la cache delle proprietà dell'oggetto e fornisce l'accesso diretto alle proprietà dell'oggetto. Per ulteriori informazioni, vedere [le interfacce IADs e IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md). |
| **IUnknown**         | Utilizzato per la gestione di oggetti COM. L'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) è obbligatoria per tutti gli oggetti com.                                                                                                                                                                                                                                                                              |
| **IDispatch**        | Utilizzato per la chiamata del metodo e dei dati della libreria dei tipi. L'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) è obbligatoria per tutti gli oggetti di automazione.                                                                                                                                                                                                                             |



 

Oggetti ADSI più complessi possono esporre interfacce aggiuntive. [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) supporta ad esempio i metodi che gestiscono le raccolte di elementi della directory dello stesso tipo di dati. I metodi [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) gestiscono le raccolte di casi speciali di oggetti che supportano l'interfaccia [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) . Per i provider che la supportano, l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) supporta i metodi per eseguire query nei servizi directory. Inoltre, ADSI fornisce interfacce che rappresentano elementi fisici e logici noti. Ad esempio, gli oggetti ADSI che rappresentano gli utenti supportano [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), quelli che rappresentano i computer supportano [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)e così via. Per ulteriori informazioni sugli oggetti ADSI, vedere [le interfacce IADs e IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md). Non tutti i provider implementano tutte le interfacce o tutti i metodi e le proprietà di tutte le interfacce. Per ulteriori informazioni, vedere [riferimenti ADSI](adsi-reference.md).

 

 