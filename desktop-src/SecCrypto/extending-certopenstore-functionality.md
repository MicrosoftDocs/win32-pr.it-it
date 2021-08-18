---
description: L'archivio certificati è fondamentale per tutte le operazioni di gestione dei certificati.
ms.assetid: e5c7c882-cbfc-4343-952c-b13c67326756
title: Estensione della funzionalità CertOpenStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c770ae56ff597f51248486db2c9eb2d74bea8d63d2e8daad83d5938594b2f1a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007090"
---
# <a name="extending-certopenstore-functionality"></a>Estensione della funzionalità CertOpenStore

[*L'archivio certificati è*](../secgloss/c-gly.md) fondamentale per tutte le operazioni di gestione dei certificati. La funzionalità della [**funzione CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) può essere estesa tramite l'uso di una funzione installabile (o registrata) certificate-store-provider. Per una panoramica su come installare o registrare funzioni da usare con CryptoAPI, vedere [Panoramica dell'OID.](oid-overview.md)

> [!Note]  
> Gli archivi certificati personalizzati non vengono migrati automaticamente quando si eseguono distribuzioni automatiche. Per eseguire la migrazione di archivi certificati personalizzati, è necessario creare un manifesto per la migrazione degli archivi personalizzati e usare Windows Utilità di migrazione stato utente (USMT). USMT è disponibile per il download dall'Area download Microsoft all'indirizzo <https://www.microsoft.com/download/details.aspx?id=10837> .

 

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) apre un archivio vuoto in memoria e chiama la funzione del [](../secgloss/o-gly.md) provider dell'archivio (se registrata o installata) usando l'identificatore di oggetto (OID) passato nel parametro *lpszStoreProvider.* Per un elenco dei tipi di provider predefiniti forniti con CryptoAPI, vedere **CertOpenStore.**

La funzione del provider dell'archivio copia i certificati e gli elenchi di [*revoche*](../secgloss/c-gly.md) di certificati (CRL) nell'archivio in memoria specificato dall'handle *hCertStore* passato. La nuova funzione del provider di archivi può usare qualsiasi funzione dell'archivio certificati CryptoAPI, ad esempio [**CertAddCertificateContextToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore) o [**CertAddSerializedElementToStore,**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)per aggiungere i certificati e i CRL all'archivio in memoria. Inoltre, la funzione store-provider restituisce facoltativamente i valori per tutti i membri dati della [**struttura CERT \_ STORE \_ PROV \_ INFO.**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) La funzione deve aggiornare questa struttura solo se supporta funzioni di callback aggiuntive. Ad esempio, se l'archivio fosse di sola lettura, probabilmente non sarebbe necessario il supporto di altre funzioni di callback. Per informazioni dettagliate e prototipi delle possibili funzioni di callback, vedere Funzioni di callback [del provider dell'archivio certificati.](cryptography-functions.md)

L'archivio TrustedPeople per utente è limitato agli archivi fisici predefiniti. Non è possibile estendere l'archivio TrustedPeople per utente. Tuttavia, è possibile estendere l'archivio TrustedPeople del computer locale.

**Windows XP e Windows Server 2003:** L'archivio TrustedPeople per utente non è limitato agli archivi fisici predefiniti.

Uno dei membri dati della struttura [**CERT \_ STORE \_ PROV \_ INFO**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) è la *matrice rgpvStoreProvFunc.* Se la funzione del provider dell'archivio deve supportare una o più funzioni di callback, deve fornire puntatori per questa matrice. Questi puntatori devono puntare alle funzioni di callback che devono essere usate per altre attività dell'archivio certificati, ad esempio la chiusura dell'archivio. La figura seguente illustra il flusso di questo processo.

![Funzionalità certopenstore](images/openstor.png)

Come illustrato nella figura seguente, dopo l'apertura dell'archivio, altre funzioni CryptoAPI (ad esempio [**CertCloseStore)**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)usano la matrice di puntatori per accedere alle funzioni di callback che eseguono l'attività prevista. La definizione della struttura [**CERT \_ STORE \_ PROV \_ INFO**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) e i prototipi delle funzioni di callback predefinite fornite con CryptoAPI sono illustrati in [Certificate Store Provider Callback Functions](cryptography-functions.md).

![Funzionalità certclosestore](images/closstor.png)

Le API dell'archivio consentono a un provider di archivi [](../secgloss/c-gly.md) di gestire certificati, CRL ed elenchi di certificati attendibili (CCL) all'esterno della cache dell'archivio, ad esempio un database esterno di certificati, ad esempio fornito dal database del server dei certificati Microsoft.

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) invia tramite il parametro *pszStoreProvider* alla funzione del provider [**installabile CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) appropriata. Il provider restituisce informazioni nel *parametro pStoreProvInfo* che puntano a una [**struttura CERT STORE \_ \_ PROV \_ INFO.**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) La **struttura CERT \_ STORE \_ PROV \_ INFO** contiene un **membro dwStoreProvFlags.** È stato aggiunto il flag CERT STORE PROV EXTERNAL FLAG per consentire al provider di indicare che i certificati, gli CRL e gli CCL sono esterni alla \_ \_ cache \_ \_ dell'archivio.

[**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) restituisce una matrice di funzioni di callback. Un provider può implementare le funzioni di callback seguenti:

-   CERT \_ STORE \_ PROV \_ CLOSE \_ FUNC
-   CERT \_ STORE \_ PROV \_ READ \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ WRITE \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ DELETE \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ SET \_ CERT \_ PROPERTY \_ FUNC
-   CERT \_ STORE \_ PROV \_ READ \_ CRL \_ FUNC
-   CERT \_ STORE \_ PROV \_ WRITE \_ CRL \_ FUNC
-   CERT \_ STORE \_ PROV \_ DELETE \_ CRL \_ FUNC
-   CERT \_ STORE \_ PROV \_ SET \_ CRL \_ PROPERTY \_ FUNC
-   CERT \_ STORE \_ PROV \_ READ \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ WRITE \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ DELETE \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ SET \_ CTL \_ PROPERTY \_ FUNC

Nelle chiamate alle funzioni di callback WRITE CERT, WRITE CRL e WRITE CTL quando è impostato \_ il FLAG CERT STORE PROV WRITE ADD, i 16 bit superiori del \_ parametro \_ \_ \_ \_ \_ \_ *dwFlags* contengono il *valore dwAddDisposition.* Per supportare archivi esterni, un provider può implementare le funzioni di callback seguenti:

-   CERT \_ STORE \_ PROV \_ FIND \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ FREE \_ FIND \_ CERT \_ FUNC
-   CERT \_ STORE \_ PROV \_ GET \_ CERT \_ PROPERTY \_ FUNC
-   CERT \_ STORE \_ PROV \_ FIND \_ CRL \_ FUNC
-   CERT \_ STORE \_ PROV \_ FREE \_ FIND \_ CRL \_ FUNC
-   CERT \_ STORE \_ PROV \_ GET \_ CRL \_ PROPERTY \_ FUNC
-   CERT \_ STORE \_ PROV \_ FIND \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ FREE \_ FIND \_ CTL \_ FUNC
-   CERT \_ STORE \_ PROV \_ GET \_ CTL \_ PROPERTY \_ FUNC

Le funzioni di callback del certificato hanno le firme seguenti:

``` syntax
typedef struct _CERT_STORE_PROV_FIND_INFO {
    DWORD               cbSize;
    DWORD               dwMsgAndCertEncodingType;
    DWORD               dwFindFlags;
    DWORD               dwFindType;
    const void          *pvFindPara;
} CERT_STORE_PROV_FIND_INFO, *PCERT_STORE_PROV_FIND_INFO;
typedef const CERT_STORE_PROV_FIND_INFO CCERT_STORE_PROV_FIND_INFO,
    *PCCERT_STORE_PROV_FIND_INFO;

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_FIND_CERT)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_STORE_PROV_FIND_INFO pFindInfo,
        IN PCCERT_CONTEXT pPrevCertContext,
        IN DWORD dwFlags,
        IN OUT void **ppvStoreProvFindInfo,
        OUT PCCERT_CONTEXT *ppProvCertContext
        );

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_FREE_FIND_CERT)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_CONTEXT pCertContext,
        IN void *pvStoreProvFindInfo,
        IN DWORD dwFlags
        );

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_GET_CERT_PROPERTY)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_CONTEXT pCertContext,
        IN DWORD dwPropId,
        IN DWORD dwFlags,
        OUT void *pvData,
        IN OUT DWORD *pcbData
        );
```

Le firme per le funzioni di callback CRL e CTL sono identiche a quanto sopra con il puntatore a [**CERT \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) sostituito con un puntatore a [**CRL \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) o [**CTL \_ CONTEXT.**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context)

Il \_ callback FIND CERT viene chiamato quando le API dell'archivio enumerano, trovano o aggiungono certificati. *pPrevCertContext* e *ppvStoreProvFindInfo* sono impostati su **NULL** per avviare una nuova operazione FIND. *L'oggetto ppvStoreProvFindInfo* restituito viene passato nuovamente alla ricerca successiva in cui può essere liberato dal provider. Il provider può impostare tutte, alcune o nessuna delle proprietà del certificato. Il provider ha la possibilità di rinviare fino a quando non viene chiamato il callback GET \_ CERT \_ PROPERTY. È consigliabile che i provider impostano il maggior numero possibile di proprietà per consentire la copia in un altro archivio.

I tipi di individuazione certificati seguenti sono supportati in [**CertFindCertificateInStore:**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)

-   CERT \_ FIND \_ ANY
-   CERT \_ FIND \_ SHA1 \_ HASH
-   CERT \_ FIND \_ MD5 \_ HASH
-   PROPRIETÀ \_ FIND DEL \_ CERTIFICATO
-   CERT \_ FIND \_ PUBLIC \_ KEY
-   CERT \_ FIND \_ SUBJECT \_ NAME
-   CERT \_ FIND \_ SUBJECT \_ ATTR
-   CERT \_ FIND \_ ISSUER \_ NAME
-   CERT \_ FIND \_ ISSUER \_ ATTR
-   CERT \_ FIND \_ SUBJECT \_ STR \_ A
-   CERT \_ FIND \_ SUBJECT \_ STR \_ W
-   CERT \_ FIND \_ ISSUER \_ STR \_ A
-   CERT \_ FIND \_ ISSUER \_ STR \_ W
-   CERT \_ FIND \_ KEY \_ SPEC
-   CERT \_ FIND \_ ENHKEY \_ USAGE

Il \_ callback FIND CERT viene chiamato per ognuno dei tipi di ricerca precedenti. I parametri passati a [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) vengono copiati direttamente nella struttura CERT STORE PROV FIND INFO prima che venga chiamato il \_ callback FIND \_ \_ \_ \_ CERT. Per informazioni dettagliate sui valori dei campi per i diversi tipi di ricerca della struttura \_ CERT STORE \_ PROV \_ FIND \_ INFO, vedere **CertFindCertificateInStore.**

I tipi di individuazione certificati seguenti supportano le API [**CertGetSubjectCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) e [**CertGetIssuerCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore) e consentono di determinare se il certificato esiste già nell'archivio prima dell'aggiunta:

-   CERT \_ FIND \_ SUBJECT \_ CERT
-   CERT \_ FIND \_ ISSUER \_ OF
-   CERT \_ FIND \_ EXISTING

Per CERT \_ FIND SUBJECT CERT, il parametro \_ \_ *pvFindPara* punta a una [**struttura CERT \_ INFO**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_info) che contiene issuer e SerialNumber dell'oggetto. Per CERT \_ FIND \_ ISSUER \_ OF, *pvFindPara* punta a una [**struttura CERT \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) dell'oggetto. Per CERT \_ FIND \_ EXISTING, *pvFindPara* punta a **un contesto CERT \_** del certificato per verificarne l'esistenza nell'archivio.

Il callback FREE FIND CERT viene chiamato quando il certificato restituito dal callback FIND CERT non è stato rilasciato mediante l'uso in un successivo FIND CERT successivo, con conseguente decremento del numero di riferimenti a zero o rilascio da parte di una chiamata \_ \_ a \_ \_ [**CertCloseStore.**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore) [](../secgloss/r-gly.md) Prima che venga chiamato il callback CLOSE, tutti i certificati restituiti dal callback FIND CERT devono essere rilasciati al provider tramite il metodo passato a una chiamata al callback FIND CERT o a una chiamata al \_ \_ callback FREE FIND \_ \_ CERT. Lo stesso vale per i callback CRL e CTL.

Il callback GET CERT PROPERTY viene chiamato da \_ \_ [**CertGetCertificateContextProperty**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) se non riesce a trovare la proprietà specificata per il *parametro pCertContext.* Lo stesso vale per GET \_ CRL \_ PROPERTY e GET \_ CTL \_ PROPERTY.

Il callback FIND CRL viene chiamato quando le API di archiviazione enumerano o \_ ottengono CRL e prima di aggiungere un CRL. Verranno definiti i tipi di ricerca CRL seguenti:

Per CRL \_ FIND \_ ISSUED \_ BY, *pvFindPara* è un puntatore a [**un contesto CERT \_**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) dell'autorità di certificazione CRL. Per CRL \_ FIND \_ EXISTING, *pvFindPara* è un puntatore a [**un contesto CRL \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) dell'elenco CRL per determinare se esiste già nell'archivio.

Il \_ callback find CTL viene chiamato quando le API di archiviazione enumerano o trovano elenchi di controllo di accesso. I tipi di ricerca CTL seguenti sono supportati in [**CertFindCTLInStore:**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore)

-   CTL \_ FIND \_ ANY
-   CTL \_ FIND \_ SHA1 \_ HASH
-   CTL \_ FIND \_ MD5 \_ HASH
-   CTL \_ FIND \_ USAGE
-   TROVA OGGETTO CTL \_ \_
-   CTL \_ FIND \_ EXISTING

Il \_ callback find CTL viene chiamato per ognuno dei tipi di ricerca precedenti. I parametri passati a [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore) vengono copiati direttamente nella struttura CERT STORE PROV FIND INFO prima che venga chiamato il \_ callback FIND \_ \_ \_ \_ CTL. Per informazioni dettagliate sui valori dei campi per i diversi tipi di ricerca della struttura \_ CERT STORE \_ PROV \_ FIND \_ INFO, vedere **CertFindCTLInStore.**

Il tipo di ricerca CTL FIND EXISTING CTL consente di determinare se l'elenco CTL esiste già nell'archivio prima di eseguire \_ \_ un'aggiunta CTL.

Per CTL \_ FIND \_ EXISTING, *pvFindPara* è un puntatore alla struttura [**CTL \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context) dell'elenco CTL per determinare se esiste già nell'archivio.

 

 
