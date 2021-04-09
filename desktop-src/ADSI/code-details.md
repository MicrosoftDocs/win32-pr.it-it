---
title: Dettagli codice
description: Questa sezione elenca il codice sorgente per l'implementazione del componente provider di esempio ADSI. Tutti i riferimenti al codice sorgente in questo documento sono soggetti a modifiche e sono disponibili nella directory del codice di esempio inclusa in ADSI SDK.
ms.assetid: 207912e5-ac17-48c7-9536-981a8e92e8cf
ms.tgt_platform: multiple
keywords:
- Dettagli codice ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d959357f2cdd094b26cde4f649c3286389b8415
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047352"
---
# <a name="code-details"></a>Dettagli codice

Questa sezione elenca il codice sorgente per l'implementazione del componente provider di esempio ADSI. Tutti i riferimenti al codice sorgente in questo documento sono soggetti a modifiche e sono disponibili nella directory del codice di esempio inclusa in ADSI SDK.

> [!Note]  
> I [](/windows/desktop/api/Iads/nn-iads-iads) metodi IADs **GetEx** e **PutEx** non sono implementati nel componente provider di esempio ADSI. Ovvero, il codice che implementa Active Directory oggetti che ereditano da **IADs** non dispone di metodi **GetEx** e **PutEx** . Questo include l'oggetto classe di schema che supporta [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), l'oggetto proprietà che supporta [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), l'oggetto Active Directory generico che supporta **IADs** e qualsiasi oggetto contenitore che supporta [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). Inoltre, gli oggetti sintassi non sono presenti nel componente provider di esempio. Tuttavia, l'architettura ADSI richiede l'inclusione degli oggetti sintassi nell'oggetto contenitore dello schema, così come sono gli oggetti classe e proprietà dello schema.

 

Nella tabella seguente sono elencati i file di codice sorgente inclusi nella directory di esempio del provider in Active Directory Service Interfaces SDK.



| File di codice sorgente                 | Descrizione                                                                                                                                                       |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cclsobj. cpp](cclsobj-cpp.md)   | Routine oggetto classe di schema.                                                                                                                                     |
| [cdispmgr. cpp](cdispmgr-cpp.md) | Implementazione della gestione dispatch.                                                                                                                                  |
| [cenumns. cpp](cenumns-cpp.md)   | Routine di enumerazione dello spazio dei nomi.                                                                                                                                   |
| [cenumsch. cpp](cenumsch-cpp.md) | Routine di enumerazione dello schema.                                                                                                                                      |
| [cenumobj. cpp](cenumobj-cpp.md) | Routine di enumerazione di oggetti generici.                                                                                                                              |
| [cenumvar. cpp](cenumvar-cpp.md) | Implementazione di base per le classi derivate xxxEnumVariant.                                                                                                           |
| [cgenobj. cpp](cgenobj-cpp.md)   | Routine di oggetti generici.                                                                                                                                          |
| [cnamcf. cpp](cnamcf-cpp.md)     | Routine di class factory dello spazio dei nomi.                                                                                                                                 |
| [cnamesp. cpp](cnamesp-cpp.md)   | Routine degli oggetti dello spazio dei nomi.                                                                                                                                        |
| [Common. cpp](common-cpp.md)     | Codice comune a tutti gli oggetti provider.                                                                                                                              |
| [Core. cpp](core-cpp.md)         | Implementazioni per le proprietà' core ' condivise da tutti gli oggetti Active Directory.                                                                                     |
| [cProps. cpp](cprops-cpp.md)     | Funzionalità della cache delle proprietà.                                                                                                                                          |
| [cprov. cpp](cprov-cpp.md)       | Routine degli oggetti provider di primo livello.                                                                                                                               |
| [cprovcf. cpp](cprovcf-cpp.md)   | Oggetto provider di primo livello class factory routine.                                                                                                                 |
| [cprpobj. cpp](cprpobj-cpp.md)   | Routine oggetto proprietà.                                                                                                                                         |
| [cschobj. cpp](cschobj-cpp.md)   | Routine degli oggetti dello schema.                                                                                                                                           |
| [getobj. cpp](getobj-cpp.md)     | Funzionalità GetObject.                                                                                                                                                |
| [Globals. cpp](globals-cpp.md)   | Componenti globali del provider di esempio ADSI.                                                                                                                          |
| [GUID. cpp](guid-cpp.md)         | Esempi di componente provider CLSIDs e LIBIDs.                                                                                                                     |
| [LibMain. cpp](libmain-cpp.md)   | LibMain per adssmp.dll.                                                                                                                                           |
| [Memory. cpp](memory-cpp.md)     | Routine di gestione della memoria del componente del provider di esempio.                                                                                                            |
| [Pack. cpp](pack-cpp.md)         | Esempio di pacchetto di componenti del provider/decomprimere i dati nelle varianti.                                                                                                          |
| [Parse. cpp](parse-cpp.md)       | Analisi del percorso per lo spazio dei nomi del componente provider di esempio.                                                                                                            |
| [Property. cpp](property-cpp.md) | Ottiene e inserisce le proprietà in base al nome.                                                                                                                                   |
| [Object. cpp](object-cpp.md)     | Esempio di codice dell'elenco dei tipi di oggetto del provider per l'applicazione di filtri.                                                                                                   |
| [regdsapi. cpp](regdsapi-cpp.md) | API del servizio directory del registro di sistema del componente di esempio.                                                                                                       |
| smpoper. cpp                      | Routine di conversione dei dati.                                                                                                                                         |
| [STDFact. cpp](stdfact-cpp.md)   | Implementazione [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) standard.                                                                                                  |
| adssmp. inf                       | Dati del registro di sistema dell'archivio dati della directory di esempio Per ulteriori informazioni, vedere [installazione del componente provider di esempio](installing-the-example-provider-component.md). |



 

 

 