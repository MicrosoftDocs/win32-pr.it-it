---
description: "La libreria Xenroll.dll contiene i metodi e le proprietà seguenti che è possibile utilizzare per gestire gli archivi certificati. FunctionsDescriptionCAStoreFlagsSpecifies o restituisce flag che controllano l'accesso all'archivio dell'autorità di certificazione (CA). CAStoreNameWStrSpecifies o restituisce il nome dell'archivio CA. CAStoreTypeWStrSpecifies o restituisce il tipo dell'archivio identificato dalla proprietà castorename. MyStoreFlagsSpecifies o restituisce un flag che determina il percorso dell'archivio personale. MyStoreNameWStrSpecifies o restituisce il nome dell'archivio personale. MyStoreTypeWStrSpecifies o restituisce il tipo dell'archivio personale. RequestStoreFlagsSpecifies o restituisce un flag che determina il percorso dell'archivio richieste. RequestStoreNameWStrSpecifies o restituisce il nome dell'archivio richieste. RequestStoreTypeWStrSpecifies o restituisce il tipo dell'archivio richieste. RootStoreFlagsSpecifies o restituisce un flag che determina il percorso dell'archivio radice. RootStoreNameWStrSpecifies o restituisce il nome dell'archivio radice. RootStoreTypeWStrSpecifies o restituisce il tipo dell'archivio radice. SetHStoreCASpecifies l'handle dell'archivio CA. SetHStoreMySpecifies l'handle dell'archivio personale. SetHStoreRequestSpecifies l'handle dell'archivio richieste. SetHStoreROOTSpecifies l'handle dell'archivio radice. "
ms.assetid: 15e4368b-4199-415a-9c2c-2c1351b717e6
title: Funzioni dell'archivio certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00ab4b7245f999e1131f41172b3c77af8b9c2aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315421"
---
# <a name="certificate-store-functions"></a>Funzioni dell'archivio certificati

La libreria Xenroll.dll contiene i metodi e le proprietà seguenti che è possibile utilizzare per gestire gli archivi certificati.

| Funzioni                                                          | Descrizione                                                                                                                                                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags)                 | Specifica o restituisce i flag che controllano l'accesso all'archivio dell' [*autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CA).<br/> |
| [**CAStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr)           | Specifica o restituisce il nome dell'archivio CA.<br/>                                                                                                                                            |
| [**CAStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr)           | Specifica o restituisce il tipo dell'archivio identificato dalla proprietà **Castorename** .<br/>                                                                                                    |
| [**MyStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags)                 | Specifica o restituisce un flag che determina il percorso dell'archivio personale.<br/>                                                                                                               |
| [**MyStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr)           | Specifica o restituisce il nome dell'archivio personale.<br/>                                                                                                                                      |
| [**MyStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr)           | Specifica o restituisce il tipo dell'archivio personale.<br/>                                                                                                                                      |
| [**RequestStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags)       | Specifica o restituisce un flag che determina il percorso dell'archivio richieste.<br/>                                                                                                                |
| [**RequestStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr) | Specifica o restituisce il nome dell'archivio richieste.<br/>                                                                                                                                       |
| [**RequestStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr) | Specifica o restituisce il tipo dell'archivio richieste.<br/>                                                                                                                                       |
| [**RootStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags)             | Specifica o restituisce un flag che determina il percorso dell'archivio radice.<br/>                                                                                                                   |
| [**RootStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr)       | Specifica o restituisce il nome dell'archivio radice.<br/>                                                                                                                                          |
| [**RootStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr)       | Specifica o restituisce il tipo dell'archivio radice.<br/>                                                                                                                                          |
| [**SetHStoreCA**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreca)                   | Specifica l'handle dell'archivio CA.<br/>                                                                                                                                                     |
| [**SetHStoreMy**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoremy)                   | Specifica l'handle dell'archivio personale.<br/>                                                                                                                                               |
| [**SetHStoreRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstorerequest)         | Specifica l'handle dell'archivio richieste.<br/>                                                                                                                                                |
| [**SetHStoreROOT**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreroot)               | Specifica l'handle dell'archivio radice.<br/>                                                                                                                                                   |



 

CertEnroll.dll non Esporta funzionalità che consentono di specificare o recuperare i valori delle proprietà dell'archivio o di copiare i certificati in archivi specifici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

