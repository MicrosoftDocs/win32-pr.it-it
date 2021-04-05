---
title: Come firmare un pacchetto dell'applicazione a livello di codice (C++)
description: Informazioni su come firmare un pacchetto dell'app usando la funzione SignerSignEx2.
ms.assetid: 1183D665-83C9-4BE7-9C8D-834484B8C57F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310ba2a934a6986809329a12afa8ee20b2f6591
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724682"
---
# <a name="how-to-programmatically-sign-an-app-package-c"></a>Come firmare un pacchetto dell'applicazione a livello di codice (C++)

Informazioni su come firmare un pacchetto dell'app usando la funzione [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .

Se si desidera creare pacchetti di app Windows a livello di codice tramite l' [API](interfaces.md)di creazione pacchetti, è necessario firmare anche i pacchetti dell'applicazione prima di poterli distribuire. L'API di creazione pacchetti non fornisce un metodo specializzato per la firma dei pacchetti dell'app. Usare invece le funzioni di [crittografia](/windows/desktop/SecCrypto/cryptography-functions) standard per firmare i pacchetti dell'applicazione.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Creazione di pacchetti, distribuzione e query delle app di Windows](appx-portal.md)
-   [funzioni di crittografia](/windows/desktop/SecCrypto/cryptography-functions)

### <a name="prerequisites"></a>Prerequisiti

-   È necessario disporre di un'app di Windows in pacchetto. Per informazioni sulla creazione di un pacchetto dell'app, vedere [come creare un pacchetto dell'](how-to-create-a-package.md)app.
-   È necessario disporre di un certificato di firma codice appropriato per la firma del pacchetto dell'app. Per informazioni sulla creazione di un certificato di firma del codice di test, vedere [come creare un certificato di firma del pacchetto dell'app](how-to-create-a-package-signing-certificate.md). Caricare il certificato di firma in una struttura del [**\_ contesto del certificato**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) . Ad esempio, è possibile usare [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) e [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) per caricare un certificato di firma.
-   In Windows 8 è stata introdotta la funzione [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) . Usare **SignerSignEx2** quando si firmano i pacchetti dell'applicazione Windows.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-define-the-required-structures-for-signersignex2"></a>Passaggio 1: definire le strutture necessarie per SignerSignEx2

Oltre all'intestazione Wincrypt. h, la funzione [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) dipende da molte strutture che non sono definite in alcun file di intestazione SDK. Per usare **SignerSignEx2**, è necessario definire manualmente queste strutture:


```C++
typedef struct _SIGNER_FILE_INFO
{
    DWORD cbSize;
    LPCWSTR pwszFileName;
    HANDLE hFile;
}SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
 
typedef struct _SIGNER_BLOB_INFO
{
    DWORD cbSize;
    GUID *pGuidSubject;
    DWORD cbBlob;
    BYTE *pbBlob;
    LPCWSTR pwszDisplayName;
}SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
 
typedef struct _SIGNER_SUBJECT_INFO
{
    DWORD cbSize;
    DWORD *pdwIndex;
    DWORD dwSubjectChoice;
    union
    {
        SIGNER_FILE_INFO *pSignerFileInfo;
        SIGNER_BLOB_INFO *pSignerBlobInfo;
    };
}SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
 
// dwSubjectChoice should be one of the following:
#define SIGNER_SUBJECT_FILE    0x01
#define SIGNER_SUBJECT_BLOB    0x02
 
typedef struct _SIGNER_ATTR_AUTHCODE
{
    DWORD cbSize;
    BOOL fCommercial;
    BOOL fIndividual;
    LPCWSTR pwszName;
    LPCWSTR pwszInfo;
}SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
 
typedef struct _SIGNER_SIGNATURE_INFO
{
    DWORD cbSize;
    ALG_ID algidHash;
    DWORD dwAttrChoice;
    union
    {
        SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
    };
    PCRYPT_ATTRIBUTES psAuthenticated;
    PCRYPT_ATTRIBUTES psUnauthenticated;
}SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
 
// dwAttrChoice should be one of the following:
#define SIGNER_NO_ATTR          0x00
#define SIGNER_AUTHCODE_ATTR    0x01
 
typedef struct _SIGNER_PROVIDER_INFO
{
    DWORD cbSize;
    LPCWSTR pwszProviderName;
    DWORD dwProviderType;
    DWORD dwKeySpec;
    DWORD dwPvkChoice;
    union
    {
        LPWSTR pwszPvkFileName;
        LPWSTR pwszKeyContainer;
    };
}SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
 
//dwPvkChoice should be one of the following:
#define PVK_TYPE_FILE_NAME       0x01
#define PVK_TYPE_KEYCONTAINER    0x02
 
typedef struct _SIGNER_SPC_CHAIN_INFO
{
    DWORD cbSize;
    LPCWSTR pwszSpcFile;
    DWORD dwCertPolicy; 
    HCERTSTORE hCertStore;
}SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
 
typedef struct _SIGNER_CERT_STORE_INFO
{
    DWORD cbSize;
    PCCERT_CONTEXT pSigningCert;
    DWORD dwCertPolicy;
    HCERTSTORE hCertStore;
}SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
 
//dwCertPolicy can be a combination of the following flags:
#define SIGNER_CERT_POLICY_STORE            0x01
#define SIGNER_CERT_POLICY_CHAIN            0x02
#define SIGNER_CERT_POLICY_SPC              0x04
#define SIGNER_CERT_POLICY_CHAIN_NO_ROOT    0x08
 
typedef struct _SIGNER_CERT
{
    DWORD cbSize;
    DWORD dwCertChoice;
    union
    {
        LPCWSTR pwszSpcFile;
        SIGNER_CERT_STORE_INFO *pCertStoreInfo;
        SIGNER_SPC_CHAIN_INFO *pSpcChainInfo;
    };
    HWND hwnd;
}SIGNER_CERT, *PSIGNER_CERT;
 
//dwCertChoice should be one of the following
#define SIGNER_CERT_SPC_FILE     0x01
#define SIGNER_CERT_STORE        0x02
#define SIGNER_CERT_SPC_CHAIN    0x03
 
typedef struct _SIGNER_CONTEXT
{
    DWORD cbSize;
    DWORD cbBlob;
    BYTE *pbBlob;
}SIGNER_CONTEXT, *PSIGNER_CONTEXT;
 
typedef struct _SIGNER_SIGN_EX2_PARAMS
{
    DWORD dwFlags;
    PSIGNER_SUBJECT_INFO pSubjectInfo;
    PSIGNER_CERT pSigningCert;
    PSIGNER_SIGNATURE_INFO pSignatureInfo;
    PSIGNER_PROVIDER_INFO pProviderInfo;
    DWORD dwTimestampFlags;
    PCSTR pszAlgorithmOid;
    PCWSTR pwszTimestampURL;
    PCRYPT_ATTRIBUTES pCryptAttrs;
    PVOID pSipData;
    PSIGNER_CONTEXT *pSignerContext;
    PVOID pCryptoPolicy;
    PVOID pReserved;
} SIGNER_SIGN_EX2_PARAMS, *PSIGNER_SIGN_EX2_PARAMS;
 
typedef struct _APPX_SIP_CLIENT_DATA
{
    PSIGNER_SIGN_EX2_PARAMS pSignerParams;
    IUnknown* pAppxSipState;
} APPX_SIP_CLIENT_DATA, *PAPPX_SIP_CLIENT_DATA;
```



### <a name="step-2-call-signersignex2-to-sign-the-app-package"></a>Passaggio 2: chiamare SignerSignEx2 per firmare il pacchetto dell'app

Dopo aver definito le strutture obbligatorie specificate nel passaggio precedente, è possibile usare una qualsiasi delle opzioni disponibili nella funzione [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) per firmare un pacchetto dell'app. Quando si usa **SignerSignEx2** con i pacchetti dell'app Windows, si applicano le restrizioni seguenti:

-   Quando si firma un pacchetto dell'app, è necessario specificare un puntatore a una struttura di **\_ \_ \_ dati client SIP appx** come parametro *pSipData* . È necessario popolare il membro **pSignerParams** dei **\_ \_ \_ dati del client SIP appx** con gli stessi parametri usati per firmare il pacchetto dell'app. A tale scopo, definire i parametri desiderati nella struttura del segno di EX2 per la **firma del firmatario, assegnare l'indirizzo di questa struttura \_ \_ \_** a **pSignerParams** e quindi fare direttamente riferimento ai membri della struttura quando si chiama [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).
-   Dopo aver chiamato [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2), è necessario liberare **pAppxSipState** in *PSipData* chiamando [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su **pAppxSipState** se non è **null**.
-   Il membro **algidHash** della struttura di **\_ \_ informazioni sulla firma del firmatario** deve essere lo stesso algoritmo hash usato per la creazione del pacchetto dell'applicazione. Per informazioni su come determinare l'algoritmo hash dal pacchetto dell'app, vedere [come firmare un pacchetto dell'app con SignTool](how-to-sign-a-package-using-signtool.md). L'algoritmo predefinito di Windows 8 usato da [MakeAppx](make-appx-package--makeappx-exe-.md) e Visual Studio per creare i pacchetti dell'app è "ALGIDHASH = CALG \_ Sha \_ 256".
-   Se si vuole contrassegnare il timestamp della firma anche nel pacchetto dell'app, è necessario eseguire questa operazione durante la chiamata a [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) fornendo i parametri facoltativi per l'indicatore di tempo di **SignerSignEx2**(*dwTimestampFlags*, *pszTimestampAlgorithmOid*, *pwszHttpTimeStamp*, *psRequest*). La chiamata a [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) o alle relative varianti in un pacchetto dell'app già firmato non è supportata.

Di seguito è riportato un esempio di codice che illustra come chiamare [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):


```C++
HRESULT SignAppxPackage(
    _In_ PCCERT_CONTEXT signingCertContext,
    _In_ LPCWSTR packageFilePath)
{
    HRESULT hr = S_OK;
 
    // Initialize the parameters for SignerSignEx2
    DWORD signerIndex = 0;
 
    SIGNER_FILE_INFO fileInfo = {};
    fileInfo.cbSize = sizeof(SIGNER_FILE_INFO);
    fileInfo.pwszFileName = packageFilePath;
 
    SIGNER_SUBJECT_INFO subjectInfo = {};
    subjectInfo.cbSize = sizeof(SIGNER_SUBJECT_INFO);
    subjectInfo.pdwIndex = &signerIndex;
    subjectInfo.dwSubjectChoice = SIGNER_SUBJECT_FILE;
    subjectInfo.pSignerFileInfo = &fileInfo;
 
    SIGNER_CERT_STORE_INFO certStoreInfo = {};
    certStoreInfo.cbSize = sizeof(SIGNER_CERT_STORE_INFO);
    certStoreInfo.dwCertPolicy = SIGNER_CERT_POLICY_CHAIN_NO_ROOT;
    certStoreInfo.pSigningCert = signingCertContext;
 
    SIGNER_CERT cert = {};
    cert.cbSize = sizeof(SIGNER_CERT);
    cert.dwCertChoice = SIGNER_CERT_STORE;
    cert.pCertStoreInfo = &certStoreInfo;
 
    // The algidHash of the signature to be created must match the
    // hash algorithm used to create the app package
    SIGNER_SIGNATURE_INFO signatureInfo = {};
    signatureInfo.cbSize = sizeof(SIGNER_SIGNATURE_INFO);
    signatureInfo.algidHash = CALG_SHA_256; 
    signatureInfo.dwAttrChoice = SIGNER_NO_ATTR;
 
    SIGNER_SIGN_EX2_PARAMS signerParams = {};
    signerParams.pSubjectInfo = &subjectInfo;
    signerParams.pSigningCert = &cert;
    signerParams.pSignatureInfo = &signatureInfo;
 
    APPX_SIP_CLIENT_DATA sipClientData = {};
    sipClientData.pSignerParams = &signerParams;
    signerParams.pSipData = &sipClientData;
 
    // Type definition for invoking SignerSignEx2 via GetProcAddress
    typedef HRESULT (WINAPI *SignerSignEx2Function)(
        DWORD,
        PSIGNER_SUBJECT_INFO,
        PSIGNER_CERT,
        PSIGNER_SIGNATURE_INFO,
        PSIGNER_PROVIDER_INFO,
        DWORD,
        PCSTR,
        PCWSTR,
        PCRYPT_ATTRIBUTES,
        PVOID,
        PSIGNER_CONTEXT *,
        PVOID,
        PVOID); 
 
    // Load the SignerSignEx2 function from MSSign32.dll
    HMODULE msSignModule = LoadLibraryEx(
        L"MSSign32.dll", 
        NULL, 
        LOAD_LIBRARY_SEARCH_SYSTEM32);

    if (msSignModule)
    {
        SignerSignEx2Function SignerSignEx2 = reinterpret_cast<SignerSignEx2Function>(
            GetProcAddress(msSignModule, "SignerSignEx2"));
        if (SignerSignEx2)
        {
            hr = SignerSignEx2(
                signerParams.dwFlags,
                signerParams.pSubjectInfo,
                signerParams.pSigningCert,
                signerParams.pSignatureInfo,
                signerParams.pProviderInfo,
                signerParams.dwTimestampFlags,
                signerParams.pszAlgorithmOid,
                signerParams.pwszTimestampURL,
                signerParams.pCryptAttrs,
                signerParams.pSipData,
                signerParams.pSignerContext,
                signerParams.pCryptoPolicy,
                signerParams.pReserved);
        }
        else
        {
            DWORD lastError = GetLastError();
            hr = HRESULT_FROM_WIN32(lastError);
        }
 
        FreeLibrary(msSignModule);
    }
    else
    {
        DWORD lastError = GetLastError();
        hr = HRESULT_FROM_WIN32(lastError);
    }
 
    // Free any state used during app package signing
    if (sipClientData.pAppxSipState)
    {
        sipClientData.pAppxSipState->Release();
    }
 
    return hr;
}
```



## <a name="remarks"></a>Commenti

Dopo aver firmato il pacchetto dell'app, è anche possibile provare a convalidare la firma a livello di codice usando la funzione [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) con l' **\_ azione Wintrust \_ Generic \_ Verify \_ v2**. Non esistono considerazioni speciali in questo caso per l'uso di **WinVerifyTrust** con i pacchetti dell'applicazione Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[API per la creazione di pacchetti](interfaces.md)
</dt> <dt>

[funzioni di crittografia](/windows/desktop/SecCrypto/cryptography-functions)
</dt> </dl>

 

 