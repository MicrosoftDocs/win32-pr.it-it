---
description: Questo argomento descrive come inizializzare Gestione firme per l'uso con un documento XPS.
ms.assetid: 4c4c6e8f-4ee0-4089-a283-1082baee5054
title: Inizializzazione di gestione firme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2796838a9cd041859f0eb47bf4aeafb2a8d5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318374"
---
# <a name="initialize-the-signature-manager"></a>Inizializzazione di gestione firme

Questo argomento descrive come inizializzare Gestione firme per l'uso con un documento XPS.

Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione della firma digitale](basic-digital-signature-programming-tasks.md).

Per usare le funzionalità di Windows 7 dell'API Crypto, definire le **informazioni sull'OID di Crypt \_ \_ con i \_ \_ \_ campi aggiuntivi** come indicato di seguito:


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



Successivamente, creare un'istanza di un'interfaccia [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), come illustrato nell'esempio di codice seguente.


```C++
IXpsSignatureManager    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsSignatureManager),
    NULL, 
    CLSCTX_INPROC_SERVER,
    __uuidof(IXpsSignatureManager),
    reinterpret_cast<LPVOID*>(&newInterface));

// make sure that you got a pointer 
// to the interface
if (SUCCEEDED(hr)) {
    // Load document into signature manager from file.
    //  xpsDocument is initialized with the file name
    //  of the document to load outside of this example.
    hr = newInterface->LoadPackageFile (xpsDocument);

    // Use newInterface

    // Release interface pointers when finished with them 
    newInterface->Release();
}    
```



L'interfaccia di cui è stata creata un'istanza da [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) può essere utilizzata da un solo documento XPS, che deve essere caricato chiamando [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) o [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) prima di chiamare qualsiasi altro metodo.

Dopo che è stata creata un'istanza dell'interfaccia [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) ed è stato caricato un documento XPS, il gestore delle firme è pronto per l'uso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Firmare un documento](sign-a-document.md)
</dt> <dt>

[Aggiungere una richiesta di firma a un documento XPS](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Verificare le firme del documento](verify-document-signatures.md)
</dt> <dt>

**Usato in questa sezione**
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

**Per ulteriori informazioni**
</dt> <dt>

[Errori dell'API firma digitale XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Errori del documento XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
