---
description: L'archivio certificati è fondamentale per tutte le operazioni di gestione dei certificati.
ms.assetid: e5c7c882-cbfc-4343-952c-b13c67326756
title: Estensione della funzionalità CertOpenStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce198578cc482ba0488bd97ae0f1d7f923511b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550034"
---
# <a name="extending-certopenstore-functionality"></a>Estensione della funzionalità CertOpenStore

L' [*archivio certificati*](../secgloss/c-gly.md) è fondamentale per tutte le operazioni di gestione dei certificati. La funzionalità della funzione [**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) può essere estesa tramite l'uso di una funzione installabile (o registrata) del provider di certificati. Per una panoramica su come installare o registrare le funzioni da usare con CryptoAPI, vedere [Cenni preliminari sull'OID](oid-overview.md).

> [!Note]  
> Gli archivi certificati personalizzati non vengono migrati automaticamente durante l'esecuzione di distribuzioni automatiche. Per eseguire la migrazione degli archivi certificati personalizzati, è necessario creare un manifesto per la migrazione degli archivi personalizzati e utilizzare il Utilità di migrazione stato utente Windows (USMT). USMT è disponibile per il download dall'area download Microsoft all'indirizzo <https://www.microsoft.com/download/details.aspx?id=10837> .

 

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) apre un archivio vuoto in memoria e chiama la funzione del provider di archiviazione (se è registrata o installata) usando l' [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) passato nel parametro *lpszStoreProvider* . Per un elenco dei tipi di provider predefiniti forniti con CryptoAPI, vedere **CertOpenStore**.

La funzione del provider dell'archivio copia i certificati e gli [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL) nell'archivio in memoria specificato dall'handle *hCertStore* passato. La nuova funzione del provider dell'archivio può utilizzare una qualsiasi delle funzioni dell'archivio certificati CryptoAPI, ad esempio, [**CertAddCertificateContextToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore) o [**CertAddSerializedElementToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore), per aggiungere i certificati e i CRL all'archivio in memoria. Inoltre, la funzione del provider di archiviazione restituisce facoltativamente i valori per tutti i membri dati della struttura [**di \_ \_ \_ informazioni di archivio certificati**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) . La funzione deve solo aggiornare questa struttura se supporta funzioni di callback aggiuntive. Se, ad esempio, l'archivio doveva essere di sola lettura, il supporto di altre funzioni di callback potrebbe non essere necessario. Per informazioni dettagliate e prototipi delle possibili funzioni di callback, vedere [funzioni di callback del provider dell'archivio certificati](cryptography-functions.md).

L'archivio TrustedPeople per utente è limitato a archivi fisici predefiniti. Non è possibile estendere l'archivio TrustedPeople per utente. Tuttavia, è possibile estendere l'archivio TrustedPeople del computer locale.

**Windows XP e Windows Server 2003:** L'archivio TrustedPeople per utente non è limitato agli archivi fisici predefiniti.

Uno dei membri dati della struttura [**Certificate \_ Store \_ di \_ prova**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) è la matrice *rgpvStoreProvFunc* . Se la funzione del provider dell'archivio deve supportare una o più funzioni di callback, deve fornire i puntatori per questa matrice. Questi puntatori devono puntare alle funzioni di callback da usare per altre attività di archivio certificati, ad esempio la chiusura dell'archivio. Nella figura seguente viene illustrato il flusso di questo processo.

![funzionalità CertOpenStore](images/openstor.png)

Come illustrato nella figura seguente, dopo l'apertura dell'archivio, altre funzioni CryptoAPI (ad esempio [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)) utilizzano la matrice di puntatori per accedere alle funzioni di callback che eseguono l'attività desiderata. Le [funzioni di callback del provider dell'archivio certificati](cryptography-functions.md)sono visualizzate nella definizione della struttura di [**informazioni di \_ \_ prova \_ dell'archivio**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) certificati e nei prototipi delle funzioni di callback predefinite fornite con CryptoAPI.

![funzionalità certclosestore](images/closstor.png)

Le API Store consentono a un provider di archiviazione di gestire i certificati, i CRL e gli elenchi di certificati [*attendibili*](../secgloss/c-gly.md) (scopi consentiti) all'esterno della cache dell'archivio (ad esempio, un database esterno di certificati, ad esempio fornito dal database del server di certificati Microsoft).

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) invia il parametro *pszStoreProvider* alla funzione del provider installabile [**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) appropriata. Il provider restituisce le informazioni nel parametro *pStoreProvInfo* che punta a una struttura di informazioni di [**prova dell' \_ archivio \_ \_ certificati**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) . La struttura dei **dati di \_ prova dell'archivio \_ \_ certificati** contiene un membro **dwStoreProvFlags** . \_ \_ \_ \_ È stato aggiunto il flag del flag esterno per l'archivio certificati per consentire al provider di indicare che i certificati, i CRL e scopi consentiti sono esterni alla cache dell'archivio.

[**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) restituisce una matrice di funzioni di callback. Un provider può implementare le funzioni di callback seguenti:

-   punto di ripristino del certificato di \_ \_ prova \_ Close \_
-   CERT per la lettura dell' \_ archivio certificati \_ \_ \_ \_
-   CERT \_ Store \_ prova \_ Write \_ CERT \_ Func
-   CERT \_ Store \_ prova \_ Delete \_ CERT \_ Func
-   \_Proprietà CERT dell'archivio certificati \_ prov \_ set \_ \_ \_
-   \_archivio certificati \_ prova a \_ leggere \_ CRL \_ Func
-   \_archivio certificati \_ prova a \_ scrivere \_ CRL \_ Func
-   \_archivio certificati \_ prov \_ Delete \_ CRL \_ Func
-   il set di certificati della \_ \_ \_ \_ \_ proprietà \_ CRL dell'archivio certificati
-   \_archivio certificati \_ prova a \_ leggere \_ CTL \_ Func
-   \_archivio certificati \_ prova a \_ scrivere \_ CTL \_ Func
-   \_archivio certificati \_ prova \_ Delete \_ CTL \_ Func
-   \_Proprietà CTL dell'archivio certificati \_ prova \_ set \_ \_ \_

Durante le chiamate alle \_ funzioni di callback Write certificate, Write \_ CRL e Write \_ CTL quando si imposta il flag di aggiunta della scrittura di certificati per l'archivio dei certificati \_ \_ \_ \_ \_ , i 16 bit superiori del parametro *dwFlags* contengono il valore *dwAddDisposition* . Per supportare gli archivi esterni, un provider può implementare le funzioni di callback seguenti:

-   CERT \_ Store \_ prov \_ Find \_ CERT \_ Func
-   CERT \_ Store \_ prove \_ Free \_ Find \_ CERT \_ Func
-   funzione CERT \_ Store prove \_ \_ get \_ CERT \_ Property \_
-   \_archivio certificati \_ prov \_ Find \_ CRL \_ Func
-   l' \_ archivio certificati \_ prova a trovare il \_ \_ \_ CRL \_ Func
-   \_archivio certificati \_ prova \_ get \_ \_ Proprietà CRL \_
-   \_archivio certificati \_ prov \_ Find \_ CTL \_ Func
-   l' \_ archivio certificati \_ prova la \_ \_ ricerca gratuita \_ CTL \_ Func
-   \_archivio certificati \_ prova \_ get \_ CTL \_ proprietà \_ Func

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

Le firme per le funzioni di callback CRL e CTL sono identiche a quelle riportate sopra con il puntatore al [**\_ contesto del certificato**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) sostituito da un puntatore a un contesto [**CRL \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) o a un [**\_ contesto CTL**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context).

Il \_ callback Find Cert viene chiamato quando le API dell'archivio enumerano, trovano o aggiungono i certificati. *pPrevCertContext* e *ppvStoreProvFindInfo* sono impostati su **null** per avviare una nuova ricerca. Il *ppvStoreProvFindInfo* restituito viene restituito alla ricerca successiva, a cui può essere liberato dal provider. Il provider può impostare tutte, alcune o nessuna delle proprietà del certificato. Il provider ha la possibilità di rinviare fino a quando non \_ \_ viene chiamato il callback della proprietà Get cert. È consigliabile per i provider impostare il maggior numero possibile di proprietà per consentire la copia in un altro archivio.

I tipi di ricerca dei certificati seguenti sono supportati in [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore):

-   CERT \_ trova \_ qualsiasi
-   \_ \_ Hash SHA1 Find \_ CERT
-   \_ \_ Hash MD5 Find \_ CERT
-   \_Proprietà CERT Find \_
-   \_ \_ chiave pubblica CERT \_ Find
-   \_ \_ nome soggetto ricerca \_ certificato
-   \_attr trovare l' \_ oggetto \_ attr
-   \_nome dell' \_ autorità emittente \_ trovare il certificato
-   autorità di certificazione per trovare l'autorità di certificazione \_ \_ \_ attr
-   CERT \_ trovare \_ \_ l'oggetto Str \_ A
-   CERTIFICATO \_ trovare l' \_ oggetto \_ Str \_ W
-   CERT \_ trova \_ emittente \_ Str \_ A
-   CERT \_ trova \_ emittente \_ Str \_ W
-   \_ \_ specifica chiave CERT \_ Find
-   uso di CERT \_ Find \_ ENHKEY \_

Il \_ callback Find Cert viene chiamato per ognuno dei tipi Find precedenti. I parametri passati a [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) vengono copiati direttamente nell' \_ archivio certificati \_ prova a trovare la \_ \_ struttura delle informazioni prima della chiamata a Find \_ CERT callback. Per informazioni dettagliate sui valori dei campi per i diversi tipi di ricerca dell' \_ archivio certificati \_ prova a trovare la struttura delle \_ \_ informazioni, vedere **CertFindCertificateInStore**.

I tipi di ricerca dei certificati seguenti supportano le API [**CertGetSubjectCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) e [**CertGetIssuerCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore) e consentono di determinare se il certificato esiste già nell'archivio prima di aggiungere:

-   \_CERT trova \_ oggetto \_ CERT
-   \_autorità di certificazione Find CERT \_ \_ di
-   CERT \_ trova \_ esistente

Per CERT \_ Find \_ Subject \_ CERT, il *parametro pvFindPara* punta a una struttura di [**\_ informazioni del certificato**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_info) che contiene l'emittente e SerialNumber dell'oggetto. Per CERT \_ Find \_ Issuer \_ di, *pvFindPara* punta a una struttura del [**\_ contesto del certificato**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) , dell'oggetto. Per CERT \_ Find \_ existing, *pvFindPara* punta a **un \_ contesto** del certificato per verificarne l'esistenza nell'archivio.

Il callback del certificato \_ Find gratuito \_ viene chiamato quando il certificato restituito dal callback di Find \_ CERT non è stato rilasciato da usato in un successivo certificato di ricerca successivo \_ , quindi il [*conteggio dei riferimenti*](../secgloss/r-gly.md) viene decrementato a zero o rilasciato da una chiamata a [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore). Prima che venga chiamato il callback di chiusura, tutti i certificati restituiti dal \_ callback Find CERT devono essere rilasciati al provider tramite il passaggio a una chiamata al \_ callback Find CERT o a una chiamata al callback della ricerca gratuita del \_ \_ certificato. Lo stesso vale per i callback CRL e CTL.

Il \_ callback della proprietà Get CERT \_ viene chiamato da [**CertGetCertificateContextProperty**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) se non riesce a trovare la proprietà specificata per il parametro *pCertContext* . Lo stesso vale per GET \_ CRL \_ Property e Get \_ CTL \_ Property.

Il \_ callback Find CRL viene chiamato quando le API dell'archivio enumerano o ottengono CRL e prima di aggiungere un CRL. Verranno definiti i seguenti tipi di ricerca CRL:

Per \_ la ricerca CRL \_ rilasciata \_ da, *pvFindPara* è un puntatore a un [**\_ contesto del certificato**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) dell'emittente CRL. Per CRL \_ Find \_ existing, *pvFindPara* è un puntatore a [**un \_ contesto CRL**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) del CRL per determinare se esiste già nell'archivio.

Il \_ callback Find CTL viene chiamato quando le API dell'archivio enumerano o trovano scopi consentiti. In [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore)sono supportati i tipi di ricerca CTL seguenti:

-   CTL \_ trovare \_ qualsiasi
-   \_ \_ Hash SHA1 per Find CTL \_
-   \_ \_ Hash MD5 Find \_ CTL
-   \_utilizzo ricerca \_ CTL
-   \_oggetto trovato \_ CTL
-   CTL \_ trova \_ esistente

Il \_ callback Find CTL viene chiamato per ognuno dei tipi Find precedenti. I parametri passati a [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore) vengono copiati direttamente nell' \_ archivio certificati \_ prova a trovare la \_ \_ struttura delle informazioni prima della chiamata a Find \_ CTL callback. Per informazioni dettagliate sui valori dei campi per i diversi tipi di ricerca dell' \_ archivio certificati \_ prova a trovare la struttura delle \_ \_ informazioni, vedere **CertFindCTLInStore**.

Il \_ tipo CTL Find \_ existing CTL Find consente di determinare se l'elenco di scopi consentiti esiste già nell'archivio prima di eseguire un CTL Add.

Per CTL \_ Find \_ existing, *pvFindPara* è un puntatore alla struttura del [**\_ contesto CTL**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context) del CTL per determinare se esiste già nell'archivio.

 

 
