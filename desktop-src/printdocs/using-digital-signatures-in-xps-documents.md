---
description: In questo argomento vengono elencate alcune considerazioni sull'uso dell'API Firma digitale XPS per aggiungere firme digitali a un documento XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Uso dell'API di firma digitale XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ea6e38704efa2a348a90fec247f37b9722857a3838b10233937e63dc37fdbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469353"
---
# <a name="using-xps-digital-signature-api"></a>Uso dell'API di firma digitale XPS

In questo argomento vengono elencate alcune considerazioni sull'uso dell'API Firma digitale XPS per aggiungere firme digitali a un documento XPS.

L'API Firma digitale XPS consente alle applicazioni di richiedere agli utenti di firmare documenti XPS e di verificare le firme presenti nei documenti XPS. L'API di firma digitale XPS può essere applicata a un documento XPS senza caricarlo in un OM XPS e può essere usato nei flussi di documenti XPS serializzati da un OM XPS.

La [sezione Attività di programmazione dell'API](#xps-digital-signature-api-programming-tasks) firma digitale XPS contiene argomenti che descrivono come programmare con l'API firma digitale XPS. In questo argomento vengono elencate le considerazioni seguenti per l'uso dell'API Firma digitale XPS quando si aggiunge il supporto della firma digitale a un'applicazione.

-   [Attività di programmazione dell'API di firma digitale XPS](#xps-digital-signature-api-programming-tasks)
-   [Note speciali sulla programmazione dell'API di firma digitale XPS](#special-notes-about-xps-digital-signature-api-programming)
    -   [Verifica delle firme digitali in un documento XPS](#verifying-digital-signatures-in-an-xps-document)
    -   [Criteri di firma della firma digitale](#digital-signature-signing-policy)
    -   [Incorporamento di una catena di certificati](#embedding-a-certificate-chain)
    -   [Uso della struttura CERT \_ CONTEXT](#using-the-cert\_context-structure)
-   [Argomenti correlati](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a>Attività di programmazione dell'API di firma digitale XPS

Questa sezione contiene argomenti che descrivono come eseguire attività di programmazione tramite l'API Firma digitale XPS.

-   [Attività comuni di programmazione delle firme digitali](basic-digital-signature-programming-tasks.md)<dl>

[Inizializzare Gestione firme](initialize-the-signature-manager.md)  
    [Firmare un documento](sign-a-document.md)  
    [Aggiungere una richiesta di firma a un documento XPS](add-a-signature-request-to-a-document.md)  
    [Verificare le firme dei documenti](verify-document-signatures.md)  
    </dl>
-   [Attività aggiuntive di programmazione delle firme digitali](advanced-digital-signature-programming-tasks.md)<dl>

[Caricare un certificato da un file](load-a-certificate-from-a-file.md)  
    [Verificare che un certificato supporti un metodo di firma](verify-a-certificate-supports-a-signature-method.md)  
    [Verificare che il sistema supporti un metodo digest](verify-a-certificate-supports-a-digest-method.md)  
    [Incorporare catene di certificati in un documento](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a>Note speciali sulla programmazione dell'API di firma digitale XPS

Gli argomenti seguenti richiedono alcune considerazioni speciali quando si usa l'API Firma digitale XPS.

-   [Verifica delle firme digitali in un documento XPS](#verifying-digital-signatures-in-an-xps-document)
-   [Criteri di firma della firma digitale](#digital-signature-signing-policy)
-   [Incorporamento di una catena di certificati](#embedding-a-certificate-chain)
-   [Uso della struttura CERT \_ CONTEXT](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a>Verifica delle firme digitali in un documento XPS

[**IXpsSignature::Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) controlla solo il contenuto firmato per determinare che non è stato modificato dopo la firma. **IXpsSignature::Verify** non verifica i certificati usati per firmare il contenuto del documento.

Per altre informazioni sui certificati e sulla crittografia, vedere [Informazioni sulla crittografia.](/windows/desktop/SecCrypto/about-cryptography)

Per un esempio di come verificare le firme dei documenti in un programma, vedere [Verify Document Signatures and Certificates](verify-document-signatures.md).

### <a name="digital-signature-signing-policy"></a>Criteri di firma della firma digitale

I criteri di firma della firma digitale determinano le parti di un documento XPS firmate. Un'opzione dei criteri di firma è firmare le relazioni di firma che iniziano dalla parte di origine della firma. Poiché le relazioni di firma cambiano con ogni firma aggiunta, le firme effettuate con questo criterio si interromperanno quando vengono aggiunte nuove firme. Assicurarsi di comprendere chiaramente le implicazioni e gli effetti dell'impostazione di questo criterio. in caso contrario, potrebbe verificarsi un comportamento imprevisto o indesiderato.

Per altre informazioni sui criteri di firma, vedere [**CRITERI \_ DI FIRMA \_ XPS.**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)

### <a name="embedding-a-certificate-chain"></a>Incorporamento di una catena di certificati

I certificati che costituiscono la catena di attendibilità di un certificato specifico possono essere aggiunti a un documento XPS. L'incorporamento di questi certificati può semplificare, in scenari non in linea, la verifica dei certificati utilizzati da una firma digitale da parte di un'applicazione.

Per altre informazioni su come incorporare certificati in un documento XPS, vedere [Incorporare catene di certificati in un documento](embedding-certificate-trust-chains-in-a-document.md).

### <a name="using-the-cert_context-structure"></a>Uso della struttura CERT \_ CONTEXT

Le [**strutture CERT \_ CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) e [**CERT \_ INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) sono le principali strutture di dati che contengono informazioni sul certificato. Per altre informazioni sull'uso di queste strutture, vedere [Uso di una struttura di dati CERT \_ INFO](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).

[**CERT \_ Le**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) strutture CONTEXT restituite dalle funzioni dell'API Crypto devono essere rilasciate quando non sono più necessarie. Per rilasciare **una struttura CERT \_ CONTEXT,** chiamare la [**funzione CertFreeCertificateContext.**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività comuni di programmazione delle firme digitali](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[Attività aggiuntive di programmazione delle firme digitali](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[**CONTESTO \_ CERT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**INFORMAZIONI SUL \_ CERTIFICATO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**CRITERI DI \_ FIRMA \_ XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
