---
title: Costanti ADSI
description: Nella tabella seguente sono elencate le costanti definite e utilizzate in ADSI (Active Directory Service Interfaces).
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
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707486"
---
# <a name="adsi-constants"></a>Costanti ADSI

Nella tabella seguente sono elencate le costanti definite e utilizzate in ADSI (Active Directory Service Interfaces).



| ADSI (costante)                      | Valore                                   | Descrizione                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ANNUNCI \_ ext \_ INITCREDENTIALS**      | 1                                       | Codice di controllo che indica che i dati personalizzati forniti al metodo [**IADsExtension:: Oper**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) contengono le credenziali utente.                                                     |
| **\_inizializzazione EXT di ADS \_ \_ completata** | 2                                       | Codice di controllo utilizzato con [**IADsExtension:: opera**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) per indicare che le estensioni possono eseguire tutte le inizializzazioni necessarie, a seconda delle funzionalità supportate dall'oggetto padre. |
| **ANNUNCI \_ ext \_ MAXEXTDISPID**         | 16777215                                | Il DISPID più alto che può essere utilizzato da un oggetto di estensione per i relativi metodi e proprietà.                                                                                                                                   |
| **ANNUNCI \_ ext \_ MINEXTDISPID**         | 1                                       | DISPID più basso che può essere utilizzato da un oggetto di estensione per i relativi metodi e proprietà.                                                                                                                                    |
| **\_risposta VLV \_ ADS**             | L "fc8cb04d-311d-406c-8CB9-1ae8b843b419" | Usato con il metodo [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) per recuperare i metadati di ricerca VLV. Per altre informazioni, vedere [come eseguire la ricerca con VLV](how-to-search-using-vlv.md).        |
| **\_ADSISEARCH DBPROPFLAGS**        | 0x0000C000                              | Utilizzato per utilizzare il provider di OLE DB.                                                                                                                                                                           |



 

 

 




