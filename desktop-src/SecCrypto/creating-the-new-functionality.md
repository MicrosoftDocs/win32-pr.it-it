---
description: Le funzioni seguenti sono tra le funzioni CryptoAPI che possono essere estese.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Creazione della nuova funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ccd528e7e9cf62896c74de07f042dec0e77a7dba5fe5fee32b9b1e2eb229da7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768870"
---
# <a name="creating-the-new-functionality"></a>Creazione della nuova funzionalità

Le funzioni seguenti sono tra le funzioni CryptoAPI che possono essere estese.



| Funzione CryptoAPI                                   | Definizione del nome della funzione OID                         | Stringa del nome della funzione OID  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | FUNC \_ DI CODIFICA \_ DELL'OGGETTO OID CRYPT \_ \_<br/>     | "CryptDllEncodeObject"    |
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | FUNC \_ DELL'OGGETTO DECODIFICA OID CRYPT \_ \_ \_<br/>     | "CryptDllDecodeObject"    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | CRYPT \_ OID \_ OPEN \_ STORE \_ PROV \_ FUNC<br/>  | "CertDllOpenStoreProv"    |
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | CRYPT \_ OID \_ VERIFY \_ CTL \_ USAGE \_ FUNC<br/> | "CertDllVerifyCTLUsage"   |
| [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | CRYPT \_ OID \_ VERIFY \_ REVOCATION \_ FUNC<br/> | "CertDllVerifyRevocation" |



 

Nel normale uso con un OID e un tipo di codifica esistenti, viene usato il codice nella funzione CryptoAPI stessa. Se una di queste funzioni viene chiamata con un OID e il tipo di codifica che il codice nella funzione CryptoAPI non è stato progettato per gestire, è necessario creare una nuova funzione, contenente la nuova funzionalità, in una DLL. Tale DLL deve essere registrata nel Registro di sistema o installata in memoria.

Quando una delle funzioni elencate viene chiamata con l'OID e il tipo di codifica appena designati, viene usato il codice nella nuova DLL anziché il codice fornito come parte della funzione CryptoAPI.

Il nome della funzione appena sviluppata può essere il nome elencato in "Stringa nome funzione OID" nella tabella precedente oppure è possibile specificare un nome diverso quando viene registrato il nuovo codice della funzione.

La nuova funzione deve usare un prototipo appropriato. In tutti i casi, ad eccezione di [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), questo prototipo è lo stesso della funzione CryptoAPI che chiama la nuova funzione. Nel caso di **CertOpenStore il** prototipo è il seguente.


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

 

Oltre a fornire il codice per la nuova funzione in una DLL, l'estensione della funzionalità [**di CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) o [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) richiede una definizione del tipo per la nuova struttura di dati C da inserire in un file di intestazione incluso quando viene compilato il programma dell'utente.

 

 




