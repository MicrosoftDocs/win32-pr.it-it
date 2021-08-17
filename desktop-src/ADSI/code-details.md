---
title: Dettagli del codice
description: Questa sezione elenca il codice sorgente per l'implementazione del componente provider di esempio ADSI. Tutti i riferimenti al codice sorgente in questo documento sono soggetti a modifiche e sono disponibili nella directory del codice di esempio inclusa in ADSI SDK.
ms.assetid: 207912e5-ac17-48c7-9536-981a8e92e8cf
ms.tgt_platform: multiple
keywords:
- Dettagli codice ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f03e7c7ed7d61d56f338a8bb44d51b1890d4bd24cd7dc1e6050f1900f6ff61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692287"
---
# <a name="code-details"></a>Dettagli del codice

Questa sezione elenca il codice sorgente per l'implementazione del componente provider di esempio ADSI. Tutti i riferimenti al codice sorgente in questo documento sono soggetti a modifiche e sono disponibili nella directory del codice di esempio inclusa in ADSI SDK.

> [!Note]  
> I [**metodi IAD**](/windows/desktop/api/Iads/nn-iads-iads) **GetEx** e **PutEx** non vengono implementati nel componente provider di esempio ADSI. In altri parole, il codice che implementa oggetti Active Directory che ereditano da **IAD** non dispone **di metodi GetEx** **e PutEx.** Sono inclusi l'oggetto classe dello schema che supporta [**IADsClass,**](/windows/desktop/api/Iads/nn-iads-iadsclass)l'oggetto proprietà che supporta [**IADsProperty,**](/windows/desktop/api/Iads/nn-iads-iadsproperty)l'oggetto Active Directory generico che supporta **gli IAD** e qualsiasi oggetto contenitore che [**supporti IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) Inoltre, gli oggetti sintassi non sono presenti nel componente provider di esempio. Tuttavia, l'architettura ADSI richiede che gli oggetti sintassi siano inclusi nell'oggetto contenitore dello schema, così come gli oggetti classe dello schema e proprietà.

 

Nella tabella seguente sono elencati i file di codice sorgente inclusi nella directory di esempio del provider in Active Directory Service Interfaces SDK.



| File di codice sorgente                 | Descrizione                                                                                                                                                       |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cclsobj.cpp](cclsobj-cpp.md)   | Routine dell'oggetto della classe dello schema.                                                                                                                                     |
| [cdispmgr.cpp](cdispmgr-cpp.md) | Implementazione di Dispatch Manager.                                                                                                                                  |
| [cenumns.cpp](cenumns-cpp.md)   | Routine di enumerazione dello spazio dei nomi.                                                                                                                                   |
| [cenumsch.cpp](cenumsch-cpp.md) | Routine di enumerazione dello schema.                                                                                                                                      |
| [cenumobj.cpp](cenumobj-cpp.md) | Routine di enumerazione di oggetti generici.                                                                                                                              |
| [cenumvar.cpp](cenumvar-cpp.md) | Implementazione di base per le classi derivate xxxEnumVariant.                                                                                                           |
| [cgenobj.cpp](cgenobj-cpp.md)   | Routine di oggetti generici.                                                                                                                                          |
| [cnamcf.cpp](cnamcf-cpp.md)     | Routine class factory dello spazio dei nomi.                                                                                                                                 |
| [cnamesp.cpp](cnamesp-cpp.md)   | Routine dell'oggetto dello spazio dei nomi.                                                                                                                                        |
| [common.cpp](common-cpp.md)     | Codice comune a tutti gli oggetti provider.                                                                                                                              |
| [core.cpp](core-cpp.md)         | Implementazioni per le proprietà "core" condivise da tutti gli oggetti di Active Directory.                                                                                     |
| [cprops.cpp](cprops-cpp.md)     | Funzionalità della cache delle proprietà.                                                                                                                                          |
| [cprov.cpp](cprov-cpp.md)       | Routine dell'oggetto provider di primo livello.                                                                                                                               |
| [cprovcf.cpp](cprovcf-cpp.md)   | Routine dell'oggetto provider di class factory di primo livello.                                                                                                                 |
| [Cprpobj.cpp](cprpobj-cpp.md)   | Routine dell'oggetto proprietà.                                                                                                                                         |
| [cschobj.cpp](cschobj-cpp.md)   | Routine dell'oggetto schema.                                                                                                                                           |
| [getobj.cpp](getobj-cpp.md)     | Funzionalità GetObject.                                                                                                                                                |
| [globals.cpp](globals-cpp.md)   | Globals del componente provider di esempio ADSI.                                                                                                                          |
| [guid.cpp](guid-cpp.md)         | CLSID e LIBID del componente provider di esempio.                                                                                                                     |
| [libmain.cpp](libmain-cpp.md)   | Libmain per adssmp.dll.                                                                                                                                           |
| [memory.cpp](memory-cpp.md)     | Routine di gestione della memoria dei componenti del provider di esempio.                                                                                                            |
| [pack.cpp](pack-cpp.md)         | Esempio di pacchetto/decompressione dei dati dei componenti del provider in VARIANT.                                                                                                          |
| [parse.cpp](parse-cpp.md)       | Analisi del percorso, ad esempio spazio dei nomi del componente del provider.                                                                                                            |
| [property.cpp](property-cpp.md) | Ottenere e inserire le proprietà in base al nome.                                                                                                                                   |
| [object.cpp](object-cpp.md)     | Esempio di codice di elenco del tipo di oggetto del componente provider per il filtro.                                                                                                   |
| [regdsapi.cpp](regdsapi-cpp.md) | API del servizio directory del Registro di sistema del componente del provider di esempio.                                                                                                       |
| smpoper.cpp                      | Routine di conversione dei dati.                                                                                                                                         |
| [stdfact.cpp](stdfact-cpp.md)   | Implementazione [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) standard.                                                                                                  |
| adssmp.inf                       | Dati del Registro di sistema dell'archivio dati di directory di esempio. Per altre informazioni, vedere [Installazione del componente provider di esempio](installing-the-example-provider-component.md). |



 

 

 