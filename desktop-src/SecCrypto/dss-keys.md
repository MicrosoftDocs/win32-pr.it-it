---
description: Viene illustrato come generare, recuperare, verificare ed esportare chiavi e firme DSS.
ms.assetid: d28fe531-af4b-4b5e-ab67-47ef70f8fa5b
title: Chiavi DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5497a2a02ac5614c056f819a3999ee3cca6c5da78229f92e57002ae6a9e401ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875311"
---
# <a name="dss-keys"></a>Chiavi DSS

-   [Generazione e recupero di chiavi DSS](#generating-and-retrieving-dss-keys)
-   [Generazione di firme DSS](#generating-dss-signatures)
-   [Verifica di una firma DSS](#verifying-a-dss-signature)
-   [Esportazione di chiavi DSS](#exporting-dss-keys)

## <a name="generating-and-retrieving-dss-keys"></a>Generazione e recupero di chiavi DSS

Le chiavi DSS possono essere generate da una chiamata alla [**funzione CryptGenKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) La chiamata a **CryptGenKey** richiede che AT SIGNATURE o CALG DSS SIGN sia passato \_ \_ \_ *nell'argomento Algid.* Questa chiamata genererà i valori P (modulo primo), Q (primo), G (generatore), X (esponente segreto) e Y (chiave pubblica) da zero e li rende persistenti in un [*BLOB*](../secgloss/k-gly.md) della chiave nell'archiviazione locale.

**Per generare una coppia di chiavi di firma DSS**

1.  Chiamare la [**funzione CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider del servizio di crittografia Microsoft DSS.
2.  Chiamare [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) per generare le chiavi. È necessario passare AT SIGNATURE o CALG DSS SIGN per l'argomento Algid e i 16 bit superiori dell'argomento \_ \_ \_ *dwFlags*  devono essere impostati sulle dimensioni della chiave desiderate. Se i 16 bit superiori sono pari a zero, verranno usate le dimensioni predefinite della chiave di 1.024 bit. Nell'argomento *hKey* viene restituito un handle [**HCRYPTKEY.**](hcryptkey.md)

**Per recuperare un puntatore alle chiavi di firma generate in precedenza**

1.  Chiamare [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia Microsoft DSS.
2.  Chiamare la [**funzione CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) con l'argomento *dwKeySpec* impostato su AT SIGNATURE o \_ CALG \_ DSS \_ SIGN.

**Per recuperare i valori P, Q e G**

1.  Chiamare [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia Microsoft DSS.
2.  Chiamare [**CryptGetUserKey con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) l'argomento *dwKeySpec* impostato su AT \_ SIGNATURE o CALG \_ DSS \_ SIGN.
3.  Chiamare [**CryptGetKeyParam con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) l'argomento *hKey* impostato sul puntatore recuperato nel passaggio precedente. *L'argomento dwParam* deve essere impostato sul flag desiderato. KP \_ P, KP \_ Q o KP \_ G. Il valore viene restituito *nell'argomento pbData* e la lunghezza dei dati viene restituita nell'argomento *pdwDataLen.* Il valore viene restituito senza informazioni di intestazione e in [*formato little-endian.*](../secgloss/l-gly.md)

## <a name="generating-dss-signatures"></a>Generazione di firme DSS

I dati da firmare devono prima essere [*con hash usando*](../secgloss/h-gly.md) l'algoritmo [*SHA.*](../secgloss/s-gly.md) Dopo l'hashing dei dati, viene generata una firma [*DSS*](../secgloss/d-gly.md) chiamando la [**funzione CryptSignHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha)

**Per generare una firma DSS**

1.  Chiamare [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia Microsoft DSS.
2.  Chiamare [**CryptCreateHash con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) l'argomento *Algid* impostato su CALG SHA per ottenere un \_ handle per un oggetto hash SHA.
3.  Chiamare [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) con *l'argomento hHash* impostato sull'handle recuperato nel passaggio precedente. Viene creato un hash dei dati e viene restituito un handle per l'hash nell'argomento *phHash* della chiamata di funzione [**CryptCreateHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)
4.  Chiamare [**CryptSignHash con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) *l'argomento hHash* impostato sull'handle recuperato nel passaggio precedente. È possibile passare AT \_ SIGNATURE o CALG \_ DSS \_ SIGN nel parametro *dwKeySpec.* La firma viene restituita all'indirizzo fornito nell'argomento *pbSignature* e la lunghezza della firma viene restituita all'indirizzo fornito nell'argomento *pdwSigLen.* È possibile passare un puntatore **NULL** nell'argomento *pbSignature* e, in questo caso, la firma non viene generata, ma la lunghezza della firma viene restituita all'indirizzo fornito nel *parametro pdwSigLen.*

## <a name="verifying-a-dss-signature"></a>Verifica di una firma DSS

Per verificare una firma DSS, è necessario importare la chiave [](../secgloss/s-gly.md) pubblica DSS del firmatario, eseguire l'hashing dei dati firmati e quindi verificare la firma.

**Per verificare una firma DSS**

1.  Chiamare [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia Microsoft DSS.
2.  Chiamare [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) per importare la chiave pubblica DSS del firmatario.
3.  Chiamare [**CryptCreateHash con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) l'argomento *Algid* impostato su CALG SHA per ottenere un \_ handle per un oggetto hash SHA.
4.  Chiamare [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) con *l'argomento hHash* impostato sull'handle recuperato nel passaggio precedente e con *pbData* che punta ai dati firmati. Viene creato un hash dei dati e viene restituito un handle per l'hash nell'argomento *phHash* della chiamata di funzione [**CryptCreateHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)
5.  Chiamare [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) con le impostazioni seguenti:

    *hHash* è impostato sull'handle per l'hash eseguito nel passaggio precedente.

    *pbSignature* punta alla firma da verificare.

    *dwSigLen* è impostato sulla lunghezza della firma.

    *hPubKey* è impostato sull'handle della chiave pubblica importata nel passaggio 2.

    *dwFlags* è impostato su zero.

## <a name="exporting-dss-keys"></a>Esportazione di chiavi DSS

Quando si [](../secgloss/s-gly.md) inviano dati firmati a un utente in cui la firma dovrà essere verificata dal destinatario, la chiave pubblica del firmatario deve essere fornita al destinatario e in genere viene inviata insieme ai dati firmati. Pertanto, è necessario essere in grado di esportare le chiavi [*DSS*](../secgloss/d-gly.md) in un [*formato BLOB di*](../secgloss/k-gly.md) chiavi.

**Per esportare la chiave pubblica DSS**

1.  Chiamare [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia Microsoft DSS.
2.  Chiamare [**CryptGetUserKey con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) l'argomento *dwKeySpec* impostato su AT \_ SIGNATURE o CALG \_ DSS \_ SIGN.
3.  Chiamare [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) con *hKey* impostato sull'handle recuperato nel passaggio precedente, *dwBlobType* impostato su PUBLICKEYBLOB e *dwFlags* impostato su zero. Il [*BLOB*](../secgloss/p-gly.md) di chiave pubblica DSS viene restituito in *pbData* e la lunghezza del [*BLOB*](../secgloss/k-gly.md) della chiave viene restituita in *pdwDataLen*. È possibile passare un puntatore **NULL** in *pbData* e, in questo caso, verrà restituita solo la lunghezza del BLOB della chiave DSS. Il BLOB restituito quando si effettua la chiamata a **CryptExportKey** è nel formato descritto in BLOB delle chiavi [del provider DSS.](dss-provider-key-blobs.md)

**Per esportare la chiave privata DSS**

-   Seguire la stessa procedura per l'esportazione di una chiave pubblica DSS, ad eccezione del fatto che quando si effettua la chiamata a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), *dwBlobType* è impostato su PRIVATEKEYBLOB. Il BLOB restituito quando si effettua la chiamata a **CryptExportKey** è nel formato descritto in BLOB delle chiavi [del provider DSS.](dss-provider-key-blobs.md)

 

 
