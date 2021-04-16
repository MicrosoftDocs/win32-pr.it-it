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
# <a name="creating-the-new-functionality"></a>Creazione della nuova funzionalità

Le funzioni seguenti sono tra le funzioni CryptoAPI che è possibile estendere.



| CryptoAPI (funzione)                                   | Definizione nome funzione OID                         | Stringa nome funzione OID  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | funzione \_ dell' \_ oggetto encode di Encode Crypt \_ \_<br/>     | "CryptDllEncodeObject"    |
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | CRYPT \_ OID \_ Decode \_ Object \_ Func<br/>     | "CryptDllDecodeObject"    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | CRYPT \_ OID \_ Open \_ Store \_ prov \_ Func<br/>  | "CertDllOpenStoreProv"    |
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | CRYPT \_ OID \_ Verify \_ verifica \_ utilizzo \_<br/> | "CertDllVerifyCTLUsage"   |
| [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | CRYPT \_ OID \_ verifica \_ revoca funzione \_<br/> | "CertDllVerifyRevocation" |



 

Nell'uso normale con un OID e un tipo di codifica esistenti, viene usato il codice nella funzione CryptoAPI. Se una di queste funzioni viene chiamata con un OID e un tipo di codifica che il codice nella funzione CryptoAPI non è stato progettato per gestire, è necessario creare una nuova funzione che contiene la nuova funzionalità in una DLL. Tale DLL deve essere registrata nel registro di sistema o installata in memoria.

Quando una delle funzioni elencate viene chiamata con l'OID e il tipo di codifica appena designati, il codice nella nuova DLL viene utilizzato anziché il codice fornito come parte della funzione CryptoAPI.

Il nome della funzione appena sviluppata può essere il nome elencato in "nome funzione OID stringa" nella tabella precedente oppure è possibile assegnare un nome diverso quando il nuovo codice della funzione è registrato.

La nuova funzione deve usare un prototipo appropriato. In tutti i casi, ad eccezione di [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), questo prototipo corrisponde alla funzione CryptoAPI che chiama la nuova funzione. Nel caso di **CertOpenStore** , il prototipo è il seguente.


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
> Se i prototipi non corrispondono, lo stack di sistema sarà danneggiato.

 

Oltre a fornire il codice per la nuova funzione in una DLL, l'estensione della funzionalità di [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) o [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) richiede una definizione di tipo per la nuova struttura di dati C da inserire in un file di intestazione incluso quando viene compilato il programma dell'utente.

 

 




