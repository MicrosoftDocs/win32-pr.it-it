---
description: Viene illustrato come generare, recuperare, verificare ed esportare chiavi e firme DSS.
ms.assetid: d28fe531-af4b-4b5e-ab67-47ef70f8fa5b
title: Chiavi DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6ab8adcc4d551c4196e99ce48f5afdd380dc3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306441"
---
# <a name="dss-keys"></a>Chiavi DSS

-   [Generazione e recupero di chiavi DSS](#generating-and-retrieving-dss-keys)
-   [Generazione di firme DSS](#generating-dss-signatures)
-   [Verifica di una firma DSS](#verifying-a-dss-signature)
-   [Esportazione di chiavi DSS](#exporting-dss-keys)

## <a name="generating-and-retrieving-dss-keys"></a>Generazione e recupero di chiavi DSS

Le chiavi DSS possono essere generate da una chiamata alla funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) . La chiamata a **CryptGenKey** richiede che \_ \_ venga passato il segno alla firma o CALG DSS \_ nell'argomento *algido* . Questa chiamata genererà i valori P (primo modulo), Q (prime), G (Generator), X (esponente Secret) e Y (chiave pubblica) da zero e li manterrà in un [*BLOB di chiavi*](../secgloss/k-gly.md) nella risorsa di archiviazione locale.

**Per generare una coppia di chiavi di firma DSS**

1.  Chiamare la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia Microsoft DSS.
2.  Chiamare [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) per generare le chiavi. È \_ necessario passare il segno di firma o CALG \_ DSS \_ per l'argomento *algido* e i 16 bit superiori dell'argomento *dwFlags* devono essere impostati sulla dimensione della chiave desiderata. Se i 16 bit superiori sono pari a zero, verranno usate le dimensioni predefinite della chiave di 1.024 bit. Nell'argomento *HKEY* viene restituito un handle [**HCRYPTKEY**](hcryptkey.md) .

**Per recuperare un puntatore alle chiavi di firma generate in precedenza**

1.  Chiamare [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia Microsoft DSS.
2.  Chiamare la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) con l'argomento *DWKEYSPEC* impostato su at \_ Signature o CALG \_ DSS \_ Sign.

**Per recuperare i valori P, Q e G**

1.  Chiamare [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia Microsoft DSS.
2.  Chiamare [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) con l'argomento *dwKeySpec* impostato su \_ Signature o CALG \_ DSS \_ Sign.
3.  Chiamare [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) con l'argomento *HKEY* impostato sul puntatore recuperato nel passaggio precedente. L'argomento *dwParam* deve essere impostato sul flag desiderato; KP \_ P, KP \_ Q o KP \_ G. Il valore viene restituito nell'argomento *pbData* e la lunghezza dei dati viene restituita nell'argomento *pdwDataLen* . Il valore viene restituito senza informazioni di intestazione e in formato [*Little-Endian*](../secgloss/l-gly.md) .

## <a name="generating-dss-signatures"></a>Generazione di firme DSS

Per i dati da firmare è necessario innanzitutto eseguire l' [*hashing*](../secgloss/h-gly.md) usando l'algoritmo [*Sha*](../secgloss/s-gly.md) . Una volta eseguito l'hashing dei dati, viene generata una firma [*DSS*](../secgloss/d-gly.md) chiamando la funzione [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) .

**Per generare una firma DSS**

1.  Chiamare [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia Microsoft DSS.
2.  Chiamare [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con l'argomento *ALGIDO* impostato su CALG \_ SHA per ottenere un handle per un oggetto hash SHA.
3.  Chiamare [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) con l'argomento *hHash* impostato sull'handle recuperato nel passaggio precedente. Viene creato un hash dei dati e viene restituito un handle all'hash nell'argomento *phHash* della chiamata di funzione [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) .
4.  Chiamare [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) con l'argomento *hHash* impostato sull'handle recuperato nel passaggio precedente. \_ \_ \_ È possibile passare il segno di firma o CALG DSS nel parametro *dwKeySpec* . La firma viene restituita all'indirizzo fornito nell'argomento *pbSignature* e la lunghezza della firma viene restituita all'indirizzo fornito nell'argomento *pdwSigLen* . Un puntatore **null** può essere passato nell'argomento *pbSignature* e, in questo caso, la firma non viene generata, ma la lunghezza della firma viene restituita all'indirizzo fornito nel parametro *pdwSigLen* .

## <a name="verifying-a-dss-signature"></a>Verifica di una firma DSS

Per verificare una firma DSS, è necessario importare la chiave pubblica DSS del firmatario, eseguire l'hashing dei [*dati firmati*](../secgloss/s-gly.md) e quindi verificare la firma.

**Per verificare una firma DSS**

1.  Chiamare [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia Microsoft DSS.
2.  Chiamare [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) per importare la chiave pubblica DSS del firmatario.
3.  Chiamare [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con l'argomento *ALGIDO* impostato su CALG \_ SHA per ottenere un handle per un oggetto hash SHA.
4.  Chiamare [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) con l'argomento *hHash* impostato sull'handle recuperato nel passaggio precedente e con *pbData* che punta ai dati firmati. Viene creato un hash dei dati e viene restituito un handle all'hash nell'argomento *phHash* della chiamata di funzione [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) .
5.  Chiamare [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) con le impostazioni seguenti:

    *hHash* viene impostato sull'handle per l'hash eseguito nel passaggio precedente.

    *pbSignature* punta alla firma da verificare.

    *dwSigLen* è impostato sulla lunghezza della firma.

    *hPubKey* è impostato sull'handle della chiave pubblica importata nel passaggio 2.

    *dwFlags* è impostato su zero.

## <a name="exporting-dss-keys"></a>Esportazione di chiavi DSS

Quando si inviano [*dati firmati*](../secgloss/s-gly.md) a un utente in cui la firma deve essere verificata dal destinatario, la chiave pubblica del firmatario deve essere fornita al destinatario e viene in genere inviata insieme ai dati firmati. Pertanto, è necessario essere in grado di esportare le chiavi [*DSS*](../secgloss/d-gly.md) in un formato [*BLOB della chiave*](../secgloss/k-gly.md) .

**Per esportare la chiave pubblica DSS**

1.  Chiamare [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia Microsoft DSS.
2.  Chiamare [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) con l'argomento *dwKeySpec* impostato su \_ Signature o CALG \_ DSS \_ Sign.
3.  Chiamare [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) con *HKEY* impostato sull'handle recuperato nel passaggio precedente, *DwBlobType* impostato su PublicKeyBlob e *dwFlags* impostato su zero. Il [*BLOB della chiave pubblica*](../secgloss/p-gly.md) DSS viene restituito in *pbData* e la lunghezza del [*BLOB della chiave*](../secgloss/k-gly.md) viene restituita in *pdwDataLen*. Un puntatore **null** può essere passato in *pbData* e, in questo caso, verrà restituita solo la lunghezza del BLOB della chiave DSS. Il BLOB restituito quando si effettua la chiamata a **CryptExportKey** è nel formato descritto in [BLOB di chiavi del provider DSS](dss-provider-key-blobs.md).

**Per esportare la chiave privata DSS**

-   Seguire la stessa procedura per esportare una chiave pubblica DSS, ad eccezione del fatto che quando si effettua la chiamata a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), *dwBlobType* è impostato su PRIVATEKEYBLOB. Il BLOB restituito quando si effettua la chiamata a **CryptExportKey** è nel formato descritto in [BLOB di chiavi del provider DSS](dss-provider-key-blobs.md).

 

 
