---
description: "La Xenroll.dll contiene i metodi e le proprietà seguenti che è possibile usare per gestire gli archivi certificati. FunctionsDescriptionCAStoreFlagsSpecifica o restituisce flag che controllano l'accesso all'archivio dell'autorità di certificazione (CA). CAStoreNameWStrSpecifica o restituisce il nome dell'archivio CA. CAStoreTypeWStrSpecifica o restituisce il tipo di archivio identificato dalla proprietà CAStoreName. MyStoreFlagsSpecifica o restituisce un flag che determina il percorso dell'archivio personale. MyStoreNameWStrSpecifica o restituisce il nome dell'archivio personale. MyStoreTypeWStrSpecifica o restituisce il tipo di archivio personale. RequestStoreFlagsSpecifica o restituisce un flag che determina il percorso dell'archivio richieste. RequestStoreNameWStrSpecifica o restituisce il nome dell'archivio richieste. RequestStoreTypeWStrSpecifica o restituisce il tipo dell'archivio richieste. RootStoreFlagsSpecifica o restituisce un flag che determina il percorso dell'archivio radice. RootStoreNameWStrSpecifica o restituisce il nome dell'archivio radice. RootStoreTypeWStrSpecifica o restituisce il tipo dell'archivio radice. SetHStoreCASpecifica l'handle dell'archivio CA. SetHStoreMySpecifica l'handle dell'archivio personale. SetHStoreRequestSpecifica l'handle dell'archivio richieste. SetHStoreROOTSpecifica l'handle dell'archivio radice. "
ms.assetid: 15e4368b-4199-415a-9c2c-2c1351b717e6
title: Funzioni dell'archivio certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53a90a6fd2146517d4d70f653da42961274301a3058f8dbad9e72b8b90228bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902175"
---
# <a name="certificate-store-functions"></a>Funzioni dell'archivio certificati

La Xenroll.dll contiene i metodi e le proprietà seguenti che è possibile usare per gestire gli archivi certificati.

| Funzioni                                                          | Descrizione                                                                                                                                                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags)                 | Specifica o restituisce flag che controllano l'accesso all'archivio [*dell'autorità*](/windows/desktop/SecGloss/c-gly) di certificazione (CA).<br/> |
| [**CAStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr)           | Specifica o restituisce il nome dell'archivio CA.<br/>                                                                                                                                            |
| [**CAStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr)           | Specifica o restituisce il tipo dell'archivio identificato dalla **proprietà CAStoreName.**<br/>                                                                                                    |
| [**MyStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags)                 | Specifica o restituisce un flag che determina il percorso dell'archivio personale.<br/>                                                                                                               |
| [**MyStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr)           | Specifica o restituisce il nome dell'archivio personale.<br/>                                                                                                                                      |
| [**MyStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr)           | Specifica o restituisce il tipo di archivio personale.<br/>                                                                                                                                      |
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



 

CertEnroll.dll non esporta la funzionalità che consente di specificare o recuperare i valori delle proprietà dell'archivio o di copiare certificati in archivi specifici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

