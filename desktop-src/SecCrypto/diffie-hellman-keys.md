---
description: Viene illustrato come generare, scambiare, importare ed esportare Diffie-Hellman chiavi.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Diffie-Hellman chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4082650b030ab1643b83cb154718176d445c98788b15a7bcadd1db97c30bab7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875501"
---
# <a name="diffie-hellman-keys"></a>Diffie-Hellman chiavi

-   [Generazione di Diffie-Hellman chiavi](#generating-diffie-hellman-keys)
-   [Scambio di Diffie-Hellman chiavi](#exchanging-diffie-hellman-keys)
-   [Esportazione di una Diffie-Hellman privata](#exporting-a-diffie-hellman-private-key)
-   [Codice di esempio](#example-code)

## <a name="generating-diffie-hellman-keys"></a>Generazione di Diffie-Hellman chiavi

Per generare una Diffie-Hellman chiave, seguire questa procedura:

1.  Chiamare la [**funzione CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per microsoft Diffie-Hellman Cryptographic Provider.
2.  Generare la nuova chiave. A tale scopo, è possibile fare in modo che CryptoAPI generi tutti i nuovi valori per G, P e X o usando i valori esistenti per G e P e generando un nuovo valore per X.

    **Per generare la chiave generando tutti i nuovi valori**

    1.  Chiamare la funzione [**CryptGenKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) passando **CALG \_ DH \_ SF** (store and forward) o **CALG \_ DH \_ EPHEM (ephemeral)** nel *parametro Algid.* La chiave verrà generata usando nuovi valori casuali per G e P, un valore appena calcolato per X e il relativo handle verrà restituito nel *parametro phKey.*
    2.  La nuova chiave è ora pronta per l'uso. I valori di G e P devono essere inviati al destinatario insieme alla chiave (o inviati da un altro metodo) quando si esegue uno scambio [*di chiavi*](../secgloss/e-gly.md).

    **Per generare la chiave usando valori predefiniti per G e P**

    1.  Chiamare [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) passando **CALG \_ DH \_ SF** (store and forward) o **CALG \_ DH \_ EPHEM (ephemeral)** nel parametro *Algid* e **CRYPT \_ PREGEN** per *il parametro dwFlags.* Un handle di chiave verrà generato e restituito nel *parametro phKey.*
    2.  Inizializzare [**una struttura CRYPT DATA \_ \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) con il **membro pbData** impostato sul valore P. Il [*BLOB*](../secgloss/b-gly.md) non contiene informazioni di intestazione e il **membro pbData** è in [*formato little-endian.*](../secgloss/l-gly.md)
    3.  Il valore di P viene impostato chiamando la funzione [**CryptSetKeyParam,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) passando l'handle di chiave recuperato nel passaggio a nel *parametro hKey,* il flag **KP \_ P** nel *parametro dwParam* e un puntatore alla struttura che contiene il valore di P nel *parametro pbData.*
    4.  Inizializzare [**una struttura CRYPT DATA \_ \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) con il **membro pbData** impostato sul valore G. Il BLOB non contiene informazioni di intestazione e il **membro pbData** è in formato little-endian.
    5.  Il valore di G viene impostato chiamando la funzione [**CryptSetKeyParam,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) passando l'handle di chiave recuperato nel passaggio a nel *parametro hKey,* il flag **\_ KP G** nel parametro *dwParam* e un puntatore alla struttura che contiene il valore di G nel *parametro pbData.*
    6.  Il valore di X viene generato chiamando la funzione [**CryptSetKeyParam,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) passando l'handle di chiave recuperato nel passaggio a nel *parametro hKey,* il flag **\_ KP X** nel parametro *dwParam* e **NULL** nel *parametro pbData.*
    7.  Se tutte le chiamate di funzione hanno avuto esito positivo, Diffie-Hellman chiave pubblica è pronta per l'uso.

3.  Quando la chiave non è più necessaria, eliminarla passando l'handle di chiave alla funzione [**CryptDestroyKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey)

Se nelle procedure precedenti è stato specificato **CALG \_ DH \_ SF,** i valori delle chiavi vengono mantenuti nell'archiviazione con ogni chiamata a [**CryptSetKeyParam.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) I valori G e P possono quindi essere recuperati usando la [**funzione CryptGetKeyParam.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) Alcuni CSP possono avere valori G e P hard-coded. In questo caso verrà restituito un errore **NTE \_ FIXEDPARAMETER** se **CryptSetKeyParam** viene chiamato con **KP \_ G** o **KP \_ P** specificato nel *parametro dwParam.* Se **viene chiamato CryptDestroyKey,** l'handle per la chiave viene eliminato, ma i valori della chiave vengono mantenuti nel provider di servizi di crittografia. Tuttavia, se **è stato specificato CALG \_ DH \_ EPHEM,** l'handle per la chiave viene eliminato e tutti i valori vengono cancellati dal CSP.

## <a name="exchanging-diffie-hellman-keys"></a>Scambio di Diffie-Hellman chiavi

Lo scopo dell'algoritmo Diffie-Hellman è rendere possibile a due o più parti creare e condividere una chiave di sessione segreta identica condividendo informazioni su una rete non protetta. Le informazioni che vengono condivise in rete sono sotto forma di due valori costanti e una chiave Diffie-Hellman pubblica. Il processo usato da due parti di scambio di chiavi è il seguente:

-   Entrambe le parti accettano Diffie-Hellman parametri che sono un numero primo (P) e un numero generatore (G).
-   L'entità 1 invia la Diffie-Hellman pubblica all'entità 2.
-   L'entità 2 calcola la chiave di sessione privata usando le informazioni contenute nella chiave privata e nella chiave pubblica dell'entità 1.
-   L'entità 2 invia la Diffie-Hellman pubblica all'entità 1.
-   L'entità 1 calcola la chiave di sessione privata usando le informazioni contenute nella chiave privata e nella chiave pubblica dell'entità 2.
-   Entrambe le parti hanno ora la stessa chiave di sessione, che può essere usata per crittografare e decrittografare i dati. I passaggi necessari per questa operazione sono illustrati nella procedura seguente.

**Per preparare una chiave Diffie-Hellman pubblica per la trasmissione**

1.  Chiamare la [**funzione CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per microsoft Diffie-Hellman Cryptographic Provider.
2.  Creare una Diffie-Hellman chiamando la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) per creare una nuova chiave o chiamando la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) per recuperare una chiave esistente.
3.  Ottenere le dimensioni necessarie per contenere il BLOB Diffie-Hellman chiave chiamando [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), passando **NULL** per il *parametro pbData.* Le dimensioni richieste verranno restituite in *pdwDataLen*.
4.  Allocare memoria per il BLOB della chiave.
5.  Creare un [*BLOB*](../secgloss/p-gly.md) Diffie-Hellman chiave pubblica chiamando la funzione [**CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) passando **PUBLICKEYBLOB** nel *parametro dwBlobType* e l'handle alla chiave Diffie-Hellman nel *parametro hKey.* Questa chiamata di funzione causa il calcolo del valore della chiave pubblica, (G^X) mod P.
6.  Se tutte le chiamate di funzione precedenti hanno avuto esito positivo, Diffie-Hellman BLOB di chiave pubblica è ora pronto per essere codificato e trasmesso.

**Per importare una Diffie-Hellman pubblica e calcolare la chiave di sessione privata**

1.  Chiamare la [**funzione CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per microsoft Diffie-Hellman Cryptographic Provider.
2.  Creare una Diffie-Hellman chiamando la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) per creare una nuova chiave o chiamando la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) per recuperare una chiave esistente.
3.  Per importare la chiave pubblica Diffie-Hellman in CSP, chiamare la funzione [**CryptImportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) passando un puntatore al BLOB della chiave pubblica nel *parametro pbData,* la lunghezza del BLOB nel *parametro dwDataLen* e l'handle alla chiave Diffie-Hellman nel *parametro hPubKey.* In questo modo viene eseguito il calcolo (Y^X) mod P, creando così la chiave privata condivisa e completando lo [*scambio di chiavi.*](../secgloss/e-gly.md) Questa chiamata di funzione restituisce un handle per il nuovo segreto, chiave di sessione nel *parametro hKey.*
4.  A questo punto, il valore Diffie-Hellman è di tipo **CALG \_ AGREEDKEY \_ ANY**. Prima di poter usare la chiave, è necessario convertirla in un tipo di chiave di sessione. Questa operazione viene eseguita chiamando la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con *dwParam* impostato su **KP \_ ALGID** e con *pbData* impostato su un puntatore a un valore [**\_ ID ALG**](alg-id.md) che rappresenta una chiave di sessione, ad esempio **CALG \_ RC4.** La chiave deve essere convertita prima di usare la chiave condivisa nella [**funzione CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) o [**CryptDecrypt.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) Le chiamate effettuate a una di queste funzioni prima della conversione del tipo di chiave avranno esito negativo.
5.  La chiave di sessione privata è ora pronta per essere usata per la crittografia o la decrittografia.
6.  Quando la chiave non è più necessaria, eliminare l'handle di chiave chiamando la [**funzione CryptDestroyKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey)

## <a name="exporting-a-diffie-hellman-private-key"></a>Esportazione di una Diffie-Hellman privata

Per esportare una Diffie-Hellman privata, seguire questa procedura:

1.  Chiamare la [**funzione CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per microsoft Diffie-Hellman Cryptographic Provider.
2.  Creare una Diffie-Hellman chiamando la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) per creare una nuova chiave o chiamando la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) per recuperare una chiave esistente.
3.  Creare un [*BLOB*](../secgloss/p-gly.md) di chiave privata Diffie-Hellman chiamando la funzione [**CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) passando **PRIVATEKEYBLOB** nel *parametro dwBlobType* e l'handle alla chiave Diffie-Hellman nel *parametro hKey.*
4.  Quando l'handle di chiave non è più necessario, chiamare la [**funzione CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) per eliminare l'handle di chiave.

## <a name="example-code"></a>Codice di esempio

L'esempio seguente illustra come creare, esportare, importare e usare una chiave Diffie-Hellman per eseguire uno scambio di chiavi.


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



 

 
