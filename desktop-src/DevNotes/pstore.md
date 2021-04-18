---
description: L'archiviazione protetta fornisce alle applicazioni un'interfaccia per archiviare i dati utente che devono essere mantenuti protetti o privi di modifiche.
ms.assetid: 85c1a009-c4f7-4b5a-ad96-6845a4e80de9
title: PStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d291b911c351cce10827b7937c6a474b7c570
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304406"
---
# <a name="pstore"></a>PStore

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

L'archiviazione protetta fornisce alle applicazioni un'interfaccia per archiviare i dati utente che devono essere mantenuti protetti o privi di modifiche.

Le unità di dati archiviate sono denominate elementi. La struttura e il contenuto dei dati archiviati sono opachi per il sistema di archiviazione protetto. L'accesso agli elementi è soggetto a conferma in base a uno stile di sicurezza definito dall'utente, che specifica la conferma necessaria per accedere ai dati, ad esempio se è necessaria una password. Inoltre, l'accesso agli elementi è soggetto a un set di regole di accesso. Esiste una regola di accesso per ogni modalità di accesso, ad esempio lettura/scrittura. I set di regole di accesso sono costituiti da clausole di accesso. Sono attualmente supportati due tipi di clausole di accesso: Authenticode e controllo binario del chiamante. In genere, in fase di installazione dell'applicazione, viene fornito un meccanismo per consentire a una nuova applicazione di richiedere all'utente l'accesso agli elementi che potrebbero essere stati creati in precedenza da un'altra applicazione.

Gli elementi vengono identificati in modo univoco dalla combinazione di una chiave, un tipo, un sottotipo e un nome. La chiave è una costante che specifica se l'elemento è globale per questo computer o associato solo a questo utente. Il nome è una stringa, generalmente scelta dall'utente. Il tipo e il sottotipo sono **GUID** s, generalmente specificati dall'applicazione. Informazioni aggiuntive sui tipi e sui sottotipi vengono mantenute nel registro di sistema e includono attributi come il nome visualizzato e i suggerimenti dell'interfaccia utente. Per i sottotipi, il tipo padre è fisso e incluso nel registro di sistema come attributo. Gli elementi del gruppo di tipi vengono utilizzati per uno scopo comune, ad esempio il pagamento o l'identificazione. Gli elementi del gruppo di sottotipi condividono un formato di dati comune.

## <a name="in-this-section"></a>Contenuto della sezione

-   [**IEnumPStoreItems**](ienumpstoreitems.md)
-   [**IEnumPStoreProviders**](ienumpstoreproviders.md)
-   [**IEnumPStoreTypes**](ienumpstoretypes.md)
-   [**IPStore**](ipstore.md)
-   [**PStoreCreateInstance**](pstorecreateinstance.md)
-   [**PStoreEnumProviders**](pstoreenumproviders.md)
-   [**Costanti PStore**](pstore-constants.md)
-   [**Tipi PStore**](pstore-types.md)

 

 
