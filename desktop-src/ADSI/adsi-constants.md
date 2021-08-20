---
title: Costanti ADSI
description: Nella tabella seguente sono elencate le costanti definite e usate in Active Directory Service Interfaces (ADSI).
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ca2a6b7eae4550f4bbd4c8c8373d63c9bdd121e6561f08e591cb6a943d309f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023919"
---
# <a name="adsi-constants"></a>Costanti ADSI

Nella tabella seguente sono elencate le costanti definite e usate in Active Directory Service Interfaces (ADSI).



| Costante ADSI                      | Valore                                   | Descrizione                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ EXT \_ INITCREDENTIALS**      | 1                                       | Codice di controllo che indica che i dati personalizzati forniti al metodo [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) contengono credenziali utente.                                                     |
| **INIZIALIZZAZIONE DI ADS \_ EXT \_ \_ COMPLETATA** | 2                                       | Codice di controllo usato con [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) per indicare che le estensioni possono eseguire qualsiasi inizializzazione necessaria, a seconda delle funzionalità supportate dall'oggetto padre. |
| **ADS \_ EXT \_ MAXEXTDISPID**         | 16777215                                | IL DISPID più elevato che un oggetto di estensione può usare per i relativi metodi e proprietà.                                                                                                                                   |
| **ADS \_ EXT \_ MINEXTDISPID**         | 1                                       | DISPID più basso che un oggetto di estensione può usare per i relativi metodi e proprietà.                                                                                                                                    |
| **RISPOSTA \_ VLV DI ADS \_**             | L"fc8cb04d-311d-406c-8cb9-1ae8b843b419" | Usato con il [**metodo IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) per recuperare i metadati di ricerca VLV. Per altre informazioni, vedere [How to Search Using VLV](how-to-search-using-vlv.md).        |
| **DBPROPFLAGS \_ ADSISEARCH**        | 0x0000C000                              | Usato per lavorare con il provider OLE DB.                                                                                                                                                                           |



 

 

 




