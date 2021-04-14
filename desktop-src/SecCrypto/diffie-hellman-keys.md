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
# <a name="diffie-hellman-keys"></a><span data-ttu-id="ed8b0-103">Chiavi di Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="ed8b0-103">Diffie-Hellman Keys</span></span>

-   [<span data-ttu-id="ed8b0-104">Generazione di chiavi di Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="ed8b0-104">Generating Diffie-Hellman Keys</span></span>](#generating-diffie-hellman-keys)
-   [<span data-ttu-id="ed8b0-105">Scambio di chiavi di Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="ed8b0-105">Exchanging Diffie-Hellman Keys</span></span>](#exchanging-diffie-hellman-keys)
-   [<span data-ttu-id="ed8b0-106">Esportazione di una chiave privata Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="ed8b0-106">Exporting a Diffie-Hellman Private Key</span></span>](#exporting-a-diffie-hellman-private-key)
-   [<span data-ttu-id="ed8b0-107">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="ed8b0-107">Example Code</span></span>](#example-code)

## <a name="generating-diffie-hellman-keys"></a><span data-ttu-id="ed8b0-108">Generazione di chiavi di Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="ed8b0-108">Generating Diffie-Hellman Keys</span></span>

<span data-ttu-id="ed8b0-109">Per generare una chiave di Diffie-Hellman, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="ed8b0-109">To generate a Diffie-Hellman key, perform the following steps:</span></span>

1.  <span data-ttu-id="ed8b0-110">Chiamare la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia di Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-110">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="ed8b0-111">Genera la nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-111">Generate the new key.</span></span> <span data-ttu-id="ed8b0-112">Per eseguire questa operazione, è possibile procedere in due modi, perché CryptoAPI genera tutti i nuovi valori per G, P e X oppure usa i valori esistenti per G e P e genera un nuovo valore per X.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-112">There are two ways to accomplish this—by having CryptoAPI generate all new values for G, P, and X or by using existing values for G and P, and generating a new value for X.</span></span>

    <span data-ttu-id="ed8b0-113">**Per generare la chiave generando tutti i nuovi valori**</span><span class="sxs-lookup"><span data-stu-id="ed8b0-113">**To generate the key by generating all new values**</span></span>

    1.  <span data-ttu-id="ed8b0-114">Chiamare la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , passando **CALG \_ DH \_ SF** (Store e inoltro) o **CALG \_ DH \_ EPHEM** (effimero) nel parametro *algido* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-114">Call the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function, passing either **CALG\_DH\_SF** (store and forward) or **CALG\_DH\_EPHEM** (ephemeral) in the *Algid* parameter.</span></span> <span data-ttu-id="ed8b0-115">La chiave verrà generata usando nuovi valori casuali per G e P, un valore appena calcolato per X e il relativo handle verrà restituito nel parametro *phKey* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-115">The key will be generated using new, random values for G and P, a newly calculated value for X, and its handle will be returned in the *phKey* parameter.</span></span>
    2.  <span data-ttu-id="ed8b0-116">La nuova chiave è ora pronta per l'uso.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-116">The new key is now ready for use.</span></span> <span data-ttu-id="ed8b0-117">Quando si esegue uno [*scambio di chiave*](../secgloss/e-gly.md), i valori di G e P devono essere inviati al destinatario insieme alla chiave (o inviata da un altro metodo).</span><span class="sxs-lookup"><span data-stu-id="ed8b0-117">The values of G and P must be sent to the recipient along with the key (or sent by some other method) when doing a [*key exchange*](../secgloss/e-gly.md).</span></span>

    <span data-ttu-id="ed8b0-118">**Per generare la chiave utilizzando valori predefiniti per G e P**</span><span class="sxs-lookup"><span data-stu-id="ed8b0-118">**To generate the key by using predefined values for G and P**</span></span>

    1.  <span data-ttu-id="ed8b0-119">Chiamare [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) passando **CALG \_ DH \_ SF** (Store e inoltro) o **CALG \_ DH \_ EPHEM** (effimero) nel parametro *algido* e la **crypt \_ PreGen** per il parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-119">Call [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) passing either **CALG\_DH\_SF** (store and forward) or **CALG\_DH\_EPHEM** (ephemeral) in the *Algid* parameter and **CRYPT\_PREGEN** for the *dwFlags* parameter.</span></span> <span data-ttu-id="ed8b0-120">Un handle di chiave verrà generato e restituito nel parametro *phKey* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-120">A key handle will be generated and returned in the *phKey* parameter.</span></span>
    2.  <span data-ttu-id="ed8b0-121">Inizializzare una struttura [**\_ \_ BLOB di dati Crypt**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) con il membro **pbData** impostato sul valore P.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-121">Initialize a [**CRYPT\_DATA\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure with the **pbData** member set to the P value.</span></span> <span data-ttu-id="ed8b0-122">Il [*BLOB*](../secgloss/b-gly.md) non contiene informazioni di intestazione e il membro **pbData** è in formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-122">The [*BLOB*](../secgloss/b-gly.md) contains no header information and the **pbData** member is in [*little-endian*](../secgloss/l-gly.md) format.</span></span>
    3.  <span data-ttu-id="ed8b0-123">Il valore di P viene impostato chiamando la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , passando l'handle di chiave recuperato nel passaggio a nel parametro *HKEY* , il flag **KP \_ P** nel parametro *dwParam* e un puntatore alla struttura che contiene il valore di p nel parametro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-123">The value of P is set by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_P** flag in the *dwParam* parameter, and a pointer to the structure that contains the value of P in the *pbData* parameter.</span></span>
    4.  <span data-ttu-id="ed8b0-124">Inizializzare una struttura [**\_ \_ BLOB di dati Crypt**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) con il membro **pbData** impostato sul valore G.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-124">Initialize a [**CRYPT\_DATA\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure with the **pbData** member set to the G value.</span></span> <span data-ttu-id="ed8b0-125">Il BLOB non contiene informazioni di intestazione e il membro **pbData** è in formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-125">The BLOB contains no header information and the **pbData** member is in little-endian format.</span></span>
    5.  <span data-ttu-id="ed8b0-126">Il valore di G viene impostato chiamando la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , passando l'handle di chiave recuperato nel passaggio a nel parametro *HKEY* , il flag **KP \_ G** nel parametro *dwParam* e un puntatore alla struttura che contiene il valore di g nel parametro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-126">The value of G is set by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_G** flag in the *dwParam* parameter, and a pointer to the structure that contains the value of G in the *pbData* parameter.</span></span>
    6.  <span data-ttu-id="ed8b0-127">Il valore di X viene generato chiamando la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , passando l'handle di chiave recuperato nel passaggio a nel parametro *HKEY* , il flag **KP \_ X** nel parametro *dwParam* e **null** nel parametro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-127">The value of X is generated by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_X** flag in the *dwParam* parameter, and **NULL** in the *pbData* parameter.</span></span>
    7.  <span data-ttu-id="ed8b0-128">Se tutte le chiamate di funzione hanno avuto esito positivo, la chiave pubblica Diffie-Hellman è pronta per l'uso.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-128">If all the function calls succeeded, the Diffie-Hellman public key is ready for use.</span></span>

3.  <span data-ttu-id="ed8b0-129">Quando la chiave non è più necessaria, eliminarla passando l'handle della chiave alla funzione [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-129">When the key is no longer needed, destroy it by passing the key handle to the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function.</span></span>

<span data-ttu-id="ed8b0-130">Se nelle procedure precedenti è stato specificato **CALG \_ DH \_ SF** , i valori delle chiavi vengono salvati in modo permanente nella risorsa di archiviazione con ogni chiamata a [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span><span class="sxs-lookup"><span data-stu-id="ed8b0-130">If **CALG\_DH\_SF** was specified in the previous procedures, the key values are persisted to storage with each call to [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span></span> <span data-ttu-id="ed8b0-131">È quindi possibile recuperare i valori G e P tramite la funzione [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-131">The G and P values can then be retrieved by using the [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) function.</span></span> <span data-ttu-id="ed8b0-132">Alcuni DSN possono avere valori G e P hardcoded.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-132">Some CSPs may have hard-coded G and P values.</span></span> <span data-ttu-id="ed8b0-133">In questo caso viene restituito un errore **\_ FIXEDPARAMETER di NTE** se **CryptSetKeyParam** viene chiamato con il parametro **KP \_ G** o **KP \_ P** specificato nel parametro *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-133">In this case a **NTE\_FIXEDPARAMETER** error will be returned if **CryptSetKeyParam** is called with **KP\_G** or **KP\_P** specified in the *dwParam* parameter.</span></span> <span data-ttu-id="ed8b0-134">Se viene chiamato **CryptDestroyKey** , l'handle per la chiave viene eliminato definitivamente, ma i valori delle chiavi vengono conservati nel CSP.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-134">If **CryptDestroyKey** is called, the handle to the key is destroyed, but the key values are retained in the CSP.</span></span> <span data-ttu-id="ed8b0-135">Tuttavia, se è stato specificato **CALG \_ DH \_ EPHEM** , l'handle per la chiave viene eliminato definitivamente e tutti i valori vengono cancellati dal CSP.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-135">However, if **CALG\_DH\_EPHEM** was specified, the handle to the key is destroyed, and all values are cleared from the CSP.</span></span>

## <a name="exchanging-diffie-hellman-keys"></a><span data-ttu-id="ed8b0-136">Scambio di chiavi di Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="ed8b0-136">Exchanging Diffie-Hellman Keys</span></span>

<span data-ttu-id="ed8b0-137">Lo scopo dell'algoritmo Diffie-Hellman consiste nel consentire a due o più parti di creare e condividere una chiave di sessione segreta identica condividendo le informazioni su una rete non protetta.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-137">The purpose of the Diffie-Hellman algorithm is to make it possible for two or more parties to create and share an identical, secret session key by sharing information over a network that is not secure.</span></span> <span data-ttu-id="ed8b0-138">Le informazioni che vengono condivise sulla rete sono sotto forma di un paio di valori costanti e di una chiave pubblica Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-138">The information that gets shared over the network is in the form of a couple of constant values and a Diffie-Hellman public key.</span></span> <span data-ttu-id="ed8b0-139">Il processo usato da due parti di scambio delle chiavi è il seguente:</span><span class="sxs-lookup"><span data-stu-id="ed8b0-139">The process used by two key-exchange parties is as follows:</span></span>

-   <span data-ttu-id="ed8b0-140">Entrambe le parti accettano i parametri di Diffie-Hellman che sono un numero primo (P) e un numero di generatore (G).</span><span class="sxs-lookup"><span data-stu-id="ed8b0-140">Both parties agree to the Diffie-Hellman parameters which are a prime number (P) and a generator number (G).</span></span>
-   <span data-ttu-id="ed8b0-141">L'entità 1 Invia la chiave pubblica Diffie-Hellman alla parte 2.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-141">Party 1 sends its Diffie-Hellman public key to party 2.</span></span>
-   <span data-ttu-id="ed8b0-142">L'entità 2 calcola la chiave della sessione segreta usando le informazioni contenute nella relativa chiave privata e nella chiave pubblica dell'entità 1.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-142">Party 2 computes the secret session key by using the information contained in its private key and party 1's public key.</span></span>
-   <span data-ttu-id="ed8b0-143">L'entità 2 Invia la chiave pubblica Diffie-Hellman alla parte 1.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-143">Party 2 sends its Diffie-Hellman public key to party 1.</span></span>
-   <span data-ttu-id="ed8b0-144">L'entità 1 calcola la chiave della sessione segreta usando le informazioni contenute nella chiave privata e nella chiave pubblica dell'entità 2.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-144">Party 1 computes the secret session key by using the information contained in its private key and party 2's public key.</span></span>
-   <span data-ttu-id="ed8b0-145">Entrambe le parti hanno ora la stessa chiave di sessione, che può essere usata per crittografare e decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-145">Both parties now have the same session key, which can be used for encrypting and decrypting data.</span></span> <span data-ttu-id="ed8b0-146">Nella procedura riportata di seguito vengono illustrati i passaggi necessari.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-146">The steps necessary for this are shown in the following procedure.</span></span>

<span data-ttu-id="ed8b0-147">**Per preparare una chiave pubblica Diffie-Hellman per la trasmissione**</span><span class="sxs-lookup"><span data-stu-id="ed8b0-147">**To prepare a Diffie-Hellman public key for transmission**</span></span>

1.  <span data-ttu-id="ed8b0-148">Chiamare la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia di Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-148">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="ed8b0-149">Creare una chiave di Diffie-Hellman chiamando la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) per creare una nuova chiave o chiamando la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) per recuperare una chiave esistente.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-149">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="ed8b0-150">Ottenere le dimensioni necessarie per conservare il BLOB della chiave di Diffie-Hellman chiamando [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), passando **null** per il parametro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-150">Get the size needed to hold the Diffie-Hellman key BLOB by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), passing **NULL** for the *pbData* parameter.</span></span> <span data-ttu-id="ed8b0-151">Le dimensioni richieste verranno restituite in *pdwDataLen*.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-151">The required size will be returned in *pdwDataLen*.</span></span>
4.  <span data-ttu-id="ed8b0-152">Allocare memoria per il BLOB della chiave.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-152">Allocate memory for the key BLOB.</span></span>
5.  <span data-ttu-id="ed8b0-153">Creare un Diffie-Hellman [*BLOB di chiave pubblica*](../secgloss/p-gly.md) chiamando la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , passando **PublicKeyBlob** nel parametro *dwBlobType* e l'handle alla chiave Diffie-Hellman nel parametro *HKEY* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-153">Create a Diffie-Hellman [*public key BLOB*](../secgloss/p-gly.md) by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, passing **PUBLICKEYBLOB** in the *dwBlobType* parameter and the handle to the Diffie-Hellman key in the *hKey* parameter.</span></span> <span data-ttu-id="ed8b0-154">Questa chiamata di funzione causa il calcolo del valore della chiave pubblica (G ^ X) mod P.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-154">This function call causes the calculation of the public key value, (G^X) mod P.</span></span>
6.  <span data-ttu-id="ed8b0-155">Se tutte le chiamate di funzione precedenti hanno avuto esito positivo, il BLOB della chiave pubblica Diffie-Hellman è ora pronto per essere codificato e trasmesso.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-155">If all the preceding function calls were successful, the Diffie-Hellman public key BLOB is now ready to be encoded and transmitted.</span></span>

<span data-ttu-id="ed8b0-156">**Per importare una chiave pubblica Diffie-Hellman e calcolare la chiave della sessione segreta**</span><span class="sxs-lookup"><span data-stu-id="ed8b0-156">**To import a Diffie-Hellman public key and calculate the secret session key**</span></span>

1.  <span data-ttu-id="ed8b0-157">Chiamare la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia di Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-157">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="ed8b0-158">Creare una chiave di Diffie-Hellman chiamando la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) per creare una nuova chiave o chiamando la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) per recuperare una chiave esistente.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-158">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="ed8b0-159">Per importare la chiave pubblica Diffie-Hellman nel CSP, chiamare la funzione [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , passando un puntatore al BLOB di chiave pubblica nel parametro *pbData* , la lunghezza del BLOB nel parametro *dwDataLen* e l'handle alla chiave Diffie-Hellman nel parametro *hPubKey* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-159">To import the Diffie-Hellman public key into the CSP, call the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function, passing a pointer to the public key BLOB in the *pbData* parameter, the length of the BLOB in the *dwDataLen* parameter, and the handle to the Diffie-Hellman key in the *hPubKey* parameter.</span></span> <span data-ttu-id="ed8b0-160">In questo modo viene eseguito il calcolo, ovvero Y ^ X, mod P, creando la chiave privata condivisa e completando lo scambio di [*chiave*](../secgloss/e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ed8b0-160">This causes the calculation, (Y^X) mod P, to be performed, thus creating the shared, secret key and completing the [*key exchange*](../secgloss/e-gly.md).</span></span> <span data-ttu-id="ed8b0-161">Questa chiamata di funzione restituisce un handle per la nuova chiave di sessione, Secret, nel parametro *HKEY* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-161">This function call returns a handle to the new, secret, session key in the *hKey* parameter.</span></span>
4.  <span data-ttu-id="ed8b0-162">A questo punto, il Diffie-Hellman importato è di tipo **CALG \_ AGREEDKEY \_ any**.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-162">At this point, the imported Diffie-Hellman is of type **CALG\_AGREEDKEY\_ANY**.</span></span> <span data-ttu-id="ed8b0-163">Prima di poter utilizzare la chiave, è necessario convertirla in un tipo di chiave di sessione.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-163">Before the key can be used, it must be converted into a session key type.</span></span> <span data-ttu-id="ed8b0-164">Questa operazione viene eseguita chiamando la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con *DwParam* impostato su **KP \_ algido** e con *pbData* impostato su un puntatore a un valore di [**\_ ID ALG**](alg-id.md) che rappresenta una chiave di sessione, ad esempio **CALG \_ RC4**.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-164">This is accomplished by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function with *dwParam* set to **KP\_ALGID** and with *pbData* set to a pointer to a [**ALG\_ID**](alg-id.md) value that represents a session key, such as **CALG\_RC4**.</span></span> <span data-ttu-id="ed8b0-165">La chiave deve essere convertita prima di usare la chiave condivisa nella funzione [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) o [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-165">The key must be converted before using the shared key in the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) or [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span> <span data-ttu-id="ed8b0-166">Le chiamate effettuate a una di queste funzioni prima della conversione del tipo di chiave avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-166">Calls made to either of these functions prior to converting the key type will fail.</span></span>
5.  <span data-ttu-id="ed8b0-167">La chiave della sessione segreta è ora pronta per essere usata per la crittografia o la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-167">The secret session key is now ready to be used for encryption or decryption.</span></span>
6.  <span data-ttu-id="ed8b0-168">Quando la chiave non è più necessaria, eliminare l'handle della chiave chiamando la funzione [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-168">When the key is no longer needed, destroy the key handle by calling the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function.</span></span>

## <a name="exporting-a-diffie-hellman-private-key"></a><span data-ttu-id="ed8b0-169">Esportazione di una chiave privata Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="ed8b0-169">Exporting a Diffie-Hellman Private Key</span></span>

<span data-ttu-id="ed8b0-170">Per esportare una chiave privata Diffie-Hellman, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="ed8b0-170">To export a Diffie-Hellman private key, perform the following steps:</span></span>

1.  <span data-ttu-id="ed8b0-171">Chiamare la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle per il provider di crittografia di Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-171">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="ed8b0-172">Creare una chiave di Diffie-Hellman chiamando la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) per creare una nuova chiave o chiamando la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) per recuperare una chiave esistente.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-172">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="ed8b0-173">Creare una Diffie-Hellman [*BLOB della chiave privata*](../secgloss/p-gly.md) chiamando la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , passando **PRIVATEKEYBLOB** nel parametro *dwBlobType* e l'handle alla chiave Diffie-Hellman nel parametro *HKEY* .</span><span class="sxs-lookup"><span data-stu-id="ed8b0-173">Create a Diffie-Hellman [*private key BLOB*](../secgloss/p-gly.md) by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, passing **PRIVATEKEYBLOB** in the *dwBlobType* parameter and the handle to the Diffie-Hellman key in the *hKey* parameter.</span></span>
4.  <span data-ttu-id="ed8b0-174">Quando l'handle di chiave non è più necessario, chiamare la funzione [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) per eliminare l'handle di chiave.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-174">When the key handle is no longer needed, call the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function to destroy the key handle.</span></span>

## <a name="example-code"></a><span data-ttu-id="ed8b0-175">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="ed8b0-175">Example Code</span></span>

<span data-ttu-id="ed8b0-176">Nell'esempio seguente viene illustrato come creare, esportare, importare e utilizzare una chiave di Diffie-Hellman per eseguire uno scambio di chiave.</span><span class="sxs-lookup"><span data-stu-id="ed8b0-176">The following example shows how to create, export, import, and use a Diffie-Hellman key to perform a key exchange.</span></span>


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



 

 
