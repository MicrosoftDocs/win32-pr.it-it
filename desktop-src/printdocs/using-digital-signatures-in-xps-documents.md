---
description: In questo argomento vengono elencate alcune considerazioni relative all'utilizzo dell'API di firma digitale XPS per aggiungere firme digitali a un documento XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Uso dell'API di firma digitale XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9037a1442a44b082caec21309c94390b3f783e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881598"
---
# <a name="using-xps-digital-signature-api"></a>Uso dell'API di firma digitale XPS

In questo argomento vengono elencate alcune considerazioni relative all'utilizzo dell'API di firma digitale XPS per aggiungere firme digitali a un documento XPS.

L'API di firma digitale XPS consente alle applicazioni di richiedere agli utenti di firmare i documenti XPS e di verificare le firme presenti nei documenti XPS. L'API di firma digitale XPS può essere applicata a un documento XPS senza caricarla in un OM XPS e può essere usata nei flussi di documenti XPS serializzati da un OM XPS.

La sezione [attività di programmazione API di firma digitale XPS](#xps-digital-signature-api-programming-tasks) contiene argomenti che descrivono come programmare con l'API di firma digitale XPS. Questo argomento elenca le considerazioni seguenti per l'uso dell'API di firma digitale XPS quando si aggiunge il supporto per la firma digitale a un'applicazione.

-   [Attività di programmazione API per la firma digitale XPS](#xps-digital-signature-api-programming-tasks)
-   [Note speciali sulla programmazione dell'API per la firma digitale XPS](#special-notes-about-xps-digital-signature-api-programming)
    -   [Verifica delle firme digitali in un documento XPS](#verifying-digital-signatures-in-an-xps-document)
    -   [Criteri firma digitale firma](#digital-signature-signing-policy)
    -   [Incorporamento di una catena di certificati](#embedding-a-certificate-chain)
    -   [Uso della struttura del contesto del certificato \_](#using-the-cert\_context-structure)
-   [Argomenti correlati](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a>Attività di programmazione API per la firma digitale XPS

Questa sezione contiene argomenti che descrivono come eseguire attività di programmazione tramite l'API di firma digitale XPS.

-   [Attività comuni di programmazione della firma digitale](basic-digital-signature-programming-tasks.md)<dl>

[Inizializzazione di gestione firme](initialize-the-signature-manager.md)  
    [Firmare un documento](sign-a-document.md)  
    [Aggiungere una richiesta di firma a un documento XPS](add-a-signature-request-to-a-document.md)  
    [Verificare le firme del documento](verify-document-signatures.md)  
    </dl>
-   [Attività aggiuntive di programmazione della firma digitale](advanced-digital-signature-programming-tasks.md)<dl>

[Caricare un certificato da un file](load-a-certificate-from-a-file.md)  
    [Verificare che un certificato supporti un metodo di firma](verify-a-certificate-supports-a-signature-method.md)  
    [Verificare che il sistema supporti un metodo digest](verify-a-certificate-supports-a-digest-method.md)  
    [Incorporare catene di certificati in un documento](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a>Note speciali sulla programmazione dell'API per la firma digitale XPS

Gli argomenti seguenti richiedono una particolare attenzione quando si usa l'API di firma digitale XPS.

-   [Verifica delle firme digitali in un documento XPS](#verifying-digital-signatures-in-an-xps-document)
-   [Criteri firma digitale firma](#digital-signature-signing-policy)
-   [Incorporamento di una catena di certificati](#embedding-a-certificate-chain)
-   [Uso della struttura del contesto del certificato \_](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a>Verifica delle firme digitali in un documento XPS

[**IXpsSignature:: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) controlla solo il contenuto firmato per determinare che non è stato modificato dopo che è stato firmato. **IXpsSignature:: Verify** non verifica alcun certificato usato per firmare il contenuto del documento.

Per ulteriori informazioni sui certificati e sulla crittografia, vedere [informazioni sulla crittografia](/windows/desktop/SecCrypto/about-cryptography).

Per un esempio di come verificare le firme dei documenti in un programma, vedere [verificare le firme e i certificati del documento](verify-document-signatures.md).

### <a name="digital-signature-signing-policy"></a>Criteri firma digitale firma

I criteri di firma della firma digitale determinano quali parti di un documento XPS sono firmate. Un'opzione per i criteri di firma consiste nel firmare le relazioni di firma che iniziano dalla parte dell'origine della firma. Poiché le relazioni di firma cambiano con ogni firma aggiunta, le firme eseguite in questo criterio si interrompono quando vengono aggiunte nuove firme. Assicurarsi di comprendere chiaramente le implicazioni e gli effetti dell'impostazione di questi criteri. in caso contrario, potrebbe verificarsi un comportamento imprevisto o indesiderato.

Per ulteriori informazioni sui criteri di firma, [**vedere \_ \_ criteri**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)di firma XPS.

### <a name="embedding-a-certificate-chain"></a>Incorporamento di una catena di certificati

I certificati che costituiscono la catena di attendibilità di un certificato specifico possono essere aggiunti a un documento XPS. Incorporando questi certificati è possibile semplificare, in scenari non in linea, che un'applicazione verifichi i certificati utilizzati da una firma digitale.

Per altre informazioni su come incorporare i certificati in un documento XPS, vedere [incorporare le catene di certificati in un documento](embedding-certificate-trust-chains-in-a-document.md).

### <a name="using-the-cert_context-structure"></a>Uso della struttura del contesto del certificato \_

Il [**\_ contesto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) del certificato e le strutture di [**\_ informazioni**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) sui certificati sono le strutture di dati principali che contengono le informazioni sul certificato. Per altre informazioni sull'uso di queste strutture, vedere [uso di una \_ struttura di dati CERT info](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).

[**Certificato \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Le strutture di contesto restituite dalle funzioni API di crittografia devono essere rilasciate quando non sono più necessarie. Per rilasciare una struttura del **\_ contesto del certificato** , chiamare la funzione [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività comuni di programmazione della firma digitale](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[Attività aggiuntive di programmazione della firma digitale](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[**contesto del certificato \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**informazioni sul certificato \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**\_criteri di firma XPS \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
