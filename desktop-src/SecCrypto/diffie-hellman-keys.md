---
description: Viene illustrato come generare, scambiare, importare ed esportare chiavi di Diffie-Hellman.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Chiavi di Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00eaddd580ac74e18e26498175f87b5d81b8e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350146"
---
# <a name="diffie-hellman-keys"></a>Chiavi di Diffie-Hellman

-   [Generazione di chiavi di Diffie-Hellman](#generating-diffie-hellman-keys)
-   [Scambio di chiavi di Diffie-Hellman](#exchanging-diffie-hellman-keys)
-   [Esportazione di una chiave privata Diffie-Hellman](#exporting-a-diffie-hellman-private-key)
-   [Codice di esempio](#example-code)

## <a name="generating-diffie-hellman-keys"></a>Generazione di chiavi di Diffie-Hellman

Per generare una chiave di Diffie-Hellman, seguire questa procedura:

1.  Chiamare la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia di Microsoft Diffie-Hellman.
2.  Genera la nuova chiave. Per eseguire questa operazione, è possibile procedere in due modi, perché CryptoAPI genera tutti i nuovi valori per G, P e X oppure usa i valori esistenti per G e P e genera un nuovo valore per X.

    **Per generare la chiave generando tutti i nuovi valori**

    1.  Chiamare la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , passando **CALG \_ DH \_ SF** (Store e inoltro) o **CALG \_ DH \_ EPHEM** (effimero) nel parametro *algido* . La chiave verrà generata usando nuovi valori casuali per G e P, un valore appena calcolato per X e il relativo handle verrà restituito nel parametro *phKey* .
    2.  La nuova chiave è ora pronta per l'uso. Quando si esegue uno [*scambio di chiave*](../secgloss/e-gly.md), i valori di G e P devono essere inviati al destinatario insieme alla chiave (o inviata da un altro metodo).

    **Per generare la chiave utilizzando valori predefiniti per G e P**

    1.  Chiamare [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) passando **CALG \_ DH \_ SF** (Store e inoltro) o **CALG \_ DH \_ EPHEM** (effimero) nel parametro *algido* e la **crypt \_ PreGen** per il parametro *dwFlags* . Un handle di chiave verrà generato e restituito nel parametro *phKey* .
    2.  Inizializzare una struttura [**\_ \_ BLOB di dati Crypt**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) con il membro **pbData** impostato sul valore P. Il [*BLOB*](../secgloss/b-gly.md) non contiene informazioni di intestazione e il membro **pbData** è in formato [*Little-Endian*](../secgloss/l-gly.md) .
    3.  Il valore di P viene impostato chiamando la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , passando l'handle di chiave recuperato nel passaggio a nel parametro *HKEY* , il flag **KP \_ P** nel parametro *dwParam* e un puntatore alla struttura che contiene il valore di p nel parametro *pbData* .
    4.  Inizializzare una struttura [**\_ \_ BLOB di dati Crypt**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) con il membro **pbData** impostato sul valore G. Il BLOB non contiene informazioni di intestazione e il membro **pbData** è in formato little-endian.
    5.  Il valore di G viene impostato chiamando la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , passando l'handle di chiave recuperato nel passaggio a nel parametro *HKEY* , il flag **KP \_ G** nel parametro *dwParam* e un puntatore alla struttura che contiene il valore di g nel parametro *pbData* .
    6.  Il valore di X viene generato chiamando la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , passando l'handle di chiave recuperato nel passaggio a nel parametro *HKEY* , il flag **KP \_ X** nel parametro *dwParam* e **null** nel parametro *pbData* .
    7.  Se tutte le chiamate di funzione hanno avuto esito positivo, la chiave pubblica Diffie-Hellman è pronta per l'uso.

3.  Quando la chiave non è più necessaria, eliminarla passando l'handle della chiave alla funzione [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .

Se nelle procedure precedenti è stato specificato **CALG \_ DH \_ SF** , i valori delle chiavi vengono salvati in modo permanente nella risorsa di archiviazione con ogni chiamata a [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam). È quindi possibile recuperare i valori G e P tramite la funzione [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) . Alcuni DSN possono avere valori G e P hardcoded. In questo caso viene restituito un errore **\_ FIXEDPARAMETER di NTE** se **CryptSetKeyParam** viene chiamato con il parametro **KP \_ G** o **KP \_ P** specificato nel parametro *dwParam* . Se viene chiamato **CryptDestroyKey** , l'handle per la chiave viene eliminato definitivamente, ma i valori delle chiavi vengono conservati nel CSP. Tuttavia, se è stato specificato **CALG \_ DH \_ EPHEM** , l'handle per la chiave viene eliminato definitivamente e tutti i valori vengono cancellati dal CSP.

## <a name="exchanging-diffie-hellman-keys"></a>Scambio di chiavi di Diffie-Hellman

Lo scopo dell'algoritmo Diffie-Hellman consiste nel consentire a due o più parti di creare e condividere una chiave di sessione segreta identica condividendo le informazioni su una rete non protetta. Le informazioni che vengono condivise sulla rete sono sotto forma di un paio di valori costanti e di una chiave pubblica Diffie-Hellman. Il processo usato da due parti di scambio delle chiavi è il seguente:

-   Entrambe le parti accettano i parametri di Diffie-Hellman che sono un numero primo (P) e un numero di generatore (G).
-   L'entità 1 Invia la chiave pubblica Diffie-Hellman alla parte 2.
-   L'entità 2 calcola la chiave della sessione segreta usando le informazioni contenute nella relativa chiave privata e nella chiave pubblica dell'entità 1.
-   L'entità 2 Invia la chiave pubblica Diffie-Hellman alla parte 1.
-   L'entità 1 calcola la chiave della sessione segreta usando le informazioni contenute nella chiave privata e nella chiave pubblica dell'entità 2.
-   Entrambe le parti hanno ora la stessa chiave di sessione, che può essere usata per crittografare e decrittografare i dati. Nella procedura riportata di seguito vengono illustrati i passaggi necessari.

**Per preparare una chiave pubblica Diffie-Hellman per la trasmissione**

1.  Chiamare la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia di Microsoft Diffie-Hellman.
2.  Creare una chiave di Diffie-Hellman chiamando la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) per creare una nuova chiave o chiamando la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) per recuperare una chiave esistente.
3.  Ottenere le dimensioni necessarie per conservare il BLOB della chiave di Diffie-Hellman chiamando [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), passando **null** per il parametro *pbData* . Le dimensioni richieste verranno restituite in *pdwDataLen*.
4.  Allocare memoria per il BLOB della chiave.
5.  Creare un Diffie-Hellman [*BLOB di chiave pubblica*](../secgloss/p-gly.md) chiamando la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , passando **PublicKeyBlob** nel parametro *dwBlobType* e l'handle alla chiave Diffie-Hellman nel parametro *HKEY* . Questa chiamata di funzione causa il calcolo del valore della chiave pubblica (G ^ X) mod P.
6.  Se tutte le chiamate di funzione precedenti hanno avuto esito positivo, il BLOB della chiave pubblica Diffie-Hellman è ora pronto per essere codificato e trasmesso.

**Per importare una chiave pubblica Diffie-Hellman e calcolare la chiave della sessione segreta**

1.  Chiamare la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia di Microsoft Diffie-Hellman.
2.  Creare una chiave di Diffie-Hellman chiamando la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) per creare una nuova chiave o chiamando la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) per recuperare una chiave esistente.
3.  Per importare la chiave pubblica Diffie-Hellman nel CSP, chiamare la funzione [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , passando un puntatore al BLOB di chiave pubblica nel parametro *pbData* , la lunghezza del BLOB nel parametro *dwDataLen* e l'handle alla chiave Diffie-Hellman nel parametro *hPubKey* . In questo modo viene eseguito il calcolo, ovvero Y ^ X, mod P, creando la chiave privata condivisa e completando lo scambio di [*chiave*](../secgloss/e-gly.md). Questa chiamata di funzione restituisce un handle per la nuova chiave di sessione, Secret, nel parametro *HKEY* .
4.  A questo punto, il Diffie-Hellman importato è di tipo **CALG \_ AGREEDKEY \_ any**. Prima di poter utilizzare la chiave, è necessario convertirla in un tipo di chiave di sessione. Questa operazione viene eseguita chiamando la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con *DwParam* impostato su **KP \_ algido** e con *pbData* impostato su un puntatore a un valore di [**\_ ID ALG**](alg-id.md) che rappresenta una chiave di sessione, ad esempio **CALG \_ RC4**. La chiave deve essere convertita prima di usare la chiave condivisa nella funzione [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) o [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) . Le chiamate effettuate a una di queste funzioni prima della conversione del tipo di chiave avranno esito negativo.
5.  La chiave della sessione segreta è ora pronta per essere usata per la crittografia o la decrittografia.
6.  Quando la chiave non è più necessaria, eliminare l'handle della chiave chiamando la funzione [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .

## <a name="exporting-a-diffie-hellman-private-key"></a>Esportazione di una chiave privata Diffie-Hellman

Per esportare una chiave privata Diffie-Hellman, seguire questa procedura:

1.  Chiamare la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia di Microsoft Diffie-Hellman.
2.  Creare una chiave di Diffie-Hellman chiamando la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) per creare una nuova chiave o chiamando la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) per recuperare una chiave esistente.
3.  Creare una Diffie-Hellman [*BLOB della chiave privata*](../secgloss/p-gly.md) chiamando la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , passando **PRIVATEKEYBLOB** nel parametro *dwBlobType* e l'handle alla chiave Diffie-Hellman nel parametro *HKEY* .
4.  Quando l'handle di chiave non è più necessario, chiamare la funzione [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) per eliminare l'handle di chiave.

## <a name="example-code"></a>Codice di esempio

Nell'esempio seguente viene illustrato come creare, esportare, importare e utilizzare una chiave di Diffie-Hellman per eseguire uno scambio di chiave.


```C++
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// The key size, in bits.
#define DHKEYSIZE 512

// Prime in little-endian format.
static const BYTE g_rgbPrime[] = 
{
    0x91, 0x02, 0xc8, 0x31, 0xee, 0x36, 0x07, 0xec, 
    0xc2, 0x24, 0x37, 0xf8, 0xfb, 0x3d, 0x69, 0x49, 
    0xac, 0x7a, 0xab, 0x32, 0xac, 0xad, 0xe9, 0xc2, 
    0xaf, 0x0e, 0x21, 0xb7, 0xc5, 0x2f, 0x76, 0xd0, 
    0xe5, 0x82, 0x78, 0x0d, 0x4f, 0x32, 0xb8, 0xcb,
    0xf7, 0x0c, 0x8d, 0xfb, 0x3a, 0xd8, 0xc0, 0xea, 
    0xcb, 0x69, 0x68, 0xb0, 0x9b, 0x75, 0x25, 0x3d,
    0xaa, 0x76, 0x22, 0x49, 0x94, 0xa4, 0xf2, 0x8d 
};

// Generator in little-endian format.
static BYTE g_rgbGenerator[] = 
{
    0x02, 0x88, 0xd7, 0xe6, 0x53, 0xaf, 0x72, 0xc5,
    0x8c, 0x08, 0x4b, 0x46, 0x6f, 0x9f, 0x2e, 0xc4,
    0x9c, 0x5c, 0x92, 0x21, 0x95, 0xb7, 0xe5, 0x58, 
    0xbf, 0xba, 0x24, 0xfa, 0xe5, 0x9d, 0xcb, 0x71, 
    0x2e, 0x2c, 0xce, 0x99, 0xf3, 0x10, 0xff, 0x3b,
    0xcb, 0xef, 0x6c, 0x95, 0x22, 0x55, 0x9d, 0x29,
    0x00, 0xb5, 0x4c, 0x5b, 0xa5, 0x63, 0x31, 0x41,
    0x13, 0x0a, 0xea, 0x39, 0x78, 0x02, 0x6d, 0x62
};

BYTE g_rgbData[] = {0x01, 0x02, 0x03, 0x04,    0x05, 0x06, 0x07, 0x08};

int _tmain(int argc, _TCHAR* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    BOOL fReturn;
    HCRYPTPROV hProvParty1 = NULL; 
    HCRYPTPROV hProvParty2 = NULL; 
    DATA_BLOB P;
    DATA_BLOB G;
    HCRYPTKEY hPrivateKey1 = NULL;
    HCRYPTKEY hPrivateKey2 = NULL;
    PBYTE pbKeyBlob1 = NULL;
    PBYTE pbKeyBlob2 = NULL;
    HCRYPTKEY hSessionKey1 = NULL;
    HCRYPTKEY hSessionKey2 = NULL;
    PBYTE pbData = NULL;

    /************************
    Construct data BLOBs for the prime and generator. The P and G 
    values, represented by the g_rgbPrime and g_rgbGenerator arrays 
    respectively, are shared values that have been agreed to by both 
    parties.
    ************************/
    P.cbData = DHKEYSIZE/8;
    P.pbData = (BYTE*)(g_rgbPrime);

    G.cbData = DHKEYSIZE/8;
    G.pbData = (BYTE*)(g_rgbGenerator);

    /************************
    Create the private Diffie-Hellman key for party 1. 
    ************************/
    // Acquire a provider handle for party 1.
    fReturn = CryptAcquireContext(
        &hProvParty1, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 1.
    fReturn = CryptGenKey(
        hProvParty1, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Create the private Diffie-Hellman key for party 2. 
    ************************/
    // Acquire a provider handle for party 2.
    fReturn = CryptAcquireContext(
        &hProvParty2, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 2.
    fReturn = CryptGenKey(
        hProvParty2, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 1's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen1;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob1 = (PBYTE)malloc(dwDataLen1)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob1,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 2's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen2;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob2 = (PBYTE)malloc(dwDataLen2)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob2,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Party 1 imports party 2's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty1,
        pbKeyBlob2,
        dwDataLen2,
        hPrivateKey1,
        0,
        &hSessionKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }
    
    /************************
    Party 2 imports party 1's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty2,
        pbKeyBlob1,
        dwDataLen1,
        hPrivateKey2,
        0,
        &hSessionKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Convert the agreed keys to symmetric keys. They are currently of 
    the form CALG_AGREEDKEY_ANY. Convert them to CALG_RC4.
    ************************/
    ALG_ID Algid = CALG_RC4;

    // Enable the party 1 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey1,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Enable the party 2 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey2,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Encrypt some data with party 1's session key. 
    ************************/
    // Get the size.
    DWORD dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        NULL, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate a buffer to hold the encrypted data.
    pbData = (PBYTE)malloc(dwLength);
    if(!pbData)
    {
        goto ErrorExit;
    }

    // Copy the unencrypted data to the buffer. The data will be 
    // encrypted in place.
    memcpy(pbData, g_rgbData, sizeof(g_rgbData)); 

    // Encrypt the data.
    dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        pbData, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }
  
    /************************
    Decrypt the data with party 2's session key. 
    ************************/
    dwLength = sizeof(g_rgbData);
    fReturn = CryptDecrypt(
        hSessionKey2,
        0,
        TRUE,
        0,
        pbData,
        &dwLength);
    if(!fReturn)
    {
        goto ErrorExit;
    }


ErrorExit:
    if(pbData)
    {
        free(pbData);
        pbData = NULL;
    }

    if(hSessionKey2)
    {
        CryptDestroyKey(hSessionKey2);
        hSessionKey2 = NULL;
    }

    if(hSessionKey1)
    {
        CryptDestroyKey(hSessionKey1);
        hSessionKey1 = NULL;
    }

    if(pbKeyBlob2)
    {
        free(pbKeyBlob2);
        pbKeyBlob2 = NULL;
    }

    if(pbKeyBlob1)
    {
        free(pbKeyBlob1);
        pbKeyBlob1 = NULL;
    }

    if(hPrivateKey2)
    {
        CryptDestroyKey(hPrivateKey2);
        hPrivateKey2 = NULL;
    }

    if(hPrivateKey1)
    {
        CryptDestroyKey(hPrivateKey1);
        hPrivateKey1 = NULL;
    }

    if(hProvParty2)
    {
        CryptReleaseContext(hProvParty2, 0);
        hProvParty2 = NULL;
    }

    if(hProvParty1)
    {
        CryptReleaseContext(hProvParty1, 0);
        hProvParty1 = NULL;
    }

    return 0;
}
```



 

 
