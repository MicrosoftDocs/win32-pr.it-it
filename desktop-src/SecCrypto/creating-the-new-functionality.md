---
description: Le funzioni seguenti sono tra le funzioni CryptoAPI che è possibile estendere.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Creazione della nuova funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525735"
---
# <a name="creating-the-new-functionality"></a><span data-ttu-id="f6055-103">Creazione della nuova funzionalità</span><span class="sxs-lookup"><span data-stu-id="f6055-103">Creating the New Functionality</span></span>

<span data-ttu-id="f6055-104">Le funzioni seguenti sono tra le funzioni CryptoAPI che è possibile estendere.</span><span class="sxs-lookup"><span data-stu-id="f6055-104">The following functions are among the CryptoAPI functions that can be extended.</span></span>



| <span data-ttu-id="f6055-105">CryptoAPI (funzione)</span><span class="sxs-lookup"><span data-stu-id="f6055-105">CryptoAPI function</span></span>                                   | <span data-ttu-id="f6055-106">Definizione nome funzione OID</span><span class="sxs-lookup"><span data-stu-id="f6055-106">OID function name define</span></span>                         | <span data-ttu-id="f6055-107">Stringa nome funzione OID</span><span class="sxs-lookup"><span data-stu-id="f6055-107">OID function name string</span></span>  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="f6055-108">**CryptEncodeObject**</span><span class="sxs-lookup"><span data-stu-id="f6055-108">**CryptEncodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | <span data-ttu-id="f6055-109">funzione \_ dell' \_ oggetto encode di Encode Crypt \_ \_</span><span class="sxs-lookup"><span data-stu-id="f6055-109">CRYPT\_OID\_ENCODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="f6055-110">"CryptDllEncodeObject"</span><span class="sxs-lookup"><span data-stu-id="f6055-110">"CryptDllEncodeObject"</span></span>    |
| [<span data-ttu-id="f6055-111">**CryptDecodeObject**</span><span class="sxs-lookup"><span data-stu-id="f6055-111">**CryptDecodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | <span data-ttu-id="f6055-112">CRYPT \_ OID \_ Decode \_ Object \_ Func</span><span class="sxs-lookup"><span data-stu-id="f6055-112">CRYPT\_OID\_DECODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="f6055-113">"CryptDllDecodeObject"</span><span class="sxs-lookup"><span data-stu-id="f6055-113">"CryptDllDecodeObject"</span></span>    |
| [<span data-ttu-id="f6055-114">**CertOpenStore**</span><span class="sxs-lookup"><span data-stu-id="f6055-114">**CertOpenStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | <span data-ttu-id="f6055-115">CRYPT \_ OID \_ Open \_ Store \_ prov \_ Func</span><span class="sxs-lookup"><span data-stu-id="f6055-115">CRYPT\_OID\_OPEN\_ STORE\_PROV\_FUNC</span></span><br/>  | <span data-ttu-id="f6055-116">"CertDllOpenStoreProv"</span><span class="sxs-lookup"><span data-stu-id="f6055-116">"CertDllOpenStoreProv"</span></span>    |
| [<span data-ttu-id="f6055-117">**CertVerifyCTLUsage**</span><span class="sxs-lookup"><span data-stu-id="f6055-117">**CertVerifyCTLUsage**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | <span data-ttu-id="f6055-118">CRYPT \_ OID \_ Verify \_ verifica \_ utilizzo \_</span><span class="sxs-lookup"><span data-stu-id="f6055-118">CRYPT\_OID\_VERIFY\_ CTL\_USAGE\_FUNC</span></span><br/> | <span data-ttu-id="f6055-119">"CertDllVerifyCTLUsage"</span><span class="sxs-lookup"><span data-stu-id="f6055-119">"CertDllVerifyCTLUsage"</span></span>   |
| [<span data-ttu-id="f6055-120">**CertVerifyRevocation**</span><span class="sxs-lookup"><span data-stu-id="f6055-120">**CertVerifyRevocation**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | <span data-ttu-id="f6055-121">CRYPT \_ OID \_ verifica \_ revoca funzione \_</span><span class="sxs-lookup"><span data-stu-id="f6055-121">CRYPT\_OID\_VERIFY\_ REVOCATION\_FUNC</span></span><br/> | <span data-ttu-id="f6055-122">"CertDllVerifyRevocation"</span><span class="sxs-lookup"><span data-stu-id="f6055-122">"CertDllVerifyRevocation"</span></span> |



 

<span data-ttu-id="f6055-123">Nell'uso normale con un OID e un tipo di codifica esistenti, viene usato il codice nella funzione CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="f6055-123">In normal use with an existing OID and encoding type, the code in the CryptoAPI function, itself, is used.</span></span> <span data-ttu-id="f6055-124">Se una di queste funzioni viene chiamata con un OID e un tipo di codifica che il codice nella funzione CryptoAPI non è stato progettato per gestire, è necessario creare una nuova funzione che contiene la nuova funzionalità in una DLL.</span><span class="sxs-lookup"><span data-stu-id="f6055-124">If one of these functions is called with an OID and encoding type that code in the CryptoAPI function was not designed to handle, a new function, containing the new functionality, must be created in a DLL.</span></span> <span data-ttu-id="f6055-125">Tale DLL deve essere registrata nel registro di sistema o installata in memoria.</span><span class="sxs-lookup"><span data-stu-id="f6055-125">That DLL must be registered in the registry or installed in memory.</span></span>

<span data-ttu-id="f6055-126">Quando una delle funzioni elencate viene chiamata con l'OID e il tipo di codifica appena designati, il codice nella nuova DLL viene utilizzato anziché il codice fornito come parte della funzione CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="f6055-126">When one of the listed functions is called with the newly designated OID and encoding type, the code in the new DLL is used rather than the code provided as part of the CryptoAPI function.</span></span>

<span data-ttu-id="f6055-127">Il nome della funzione appena sviluppata può essere il nome elencato in "nome funzione OID stringa" nella tabella precedente oppure è possibile assegnare un nome diverso quando il nuovo codice della funzione è registrato.</span><span class="sxs-lookup"><span data-stu-id="f6055-127">The name of the newly developed function can be the name listed under "OID function name string" in the previous table or a different name can be given when the new function code is registered.</span></span>

<span data-ttu-id="f6055-128">La nuova funzione deve usare un prototipo appropriato.</span><span class="sxs-lookup"><span data-stu-id="f6055-128">The new function must use an appropriate prototype.</span></span> <span data-ttu-id="f6055-129">In tutti i casi, ad eccezione di [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), questo prototipo corrisponde alla funzione CryptoAPI che chiama la nuova funzione.</span><span class="sxs-lookup"><span data-stu-id="f6055-129">In all cases except for [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), this prototype is the same as the CryptoAPI function that calls the new function.</span></span> <span data-ttu-id="f6055-130">Nel caso di **CertOpenStore** , il prototipo è il seguente.</span><span class="sxs-lookup"><span data-stu-id="f6055-130">In the case of **CertOpenStore** the prototype is as follows.</span></span>


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> <span data-ttu-id="f6055-131">Se i prototipi non corrispondono, lo stack di sistema sarà danneggiato.</span><span class="sxs-lookup"><span data-stu-id="f6055-131">If the prototypes do not match, the system stack will be corrupted.</span></span>

 

<span data-ttu-id="f6055-132">Oltre a fornire il codice per la nuova funzione in una DLL, l'estensione della funzionalità di [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) o [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) richiede una definizione di tipo per la nuova struttura di dati C da inserire in un file di intestazione incluso quando viene compilato il programma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f6055-132">In addition to providing the code for the new function in a DLL, extending the functionality of [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) or [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requires a type definition for the new C data structure to be placed in a header file included when the user's program is compiled.</span></span>

 

 




