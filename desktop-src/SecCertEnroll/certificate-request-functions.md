---
description: La CertEnroll.dll implementa cinque interfacce che possono essere usate per creare e gestire una richiesta di certificato.
ms.assetid: f4630095-6ba2-46f7-8825-e7a5b1cb185a
title: Funzioni di richiesta di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e07fb348b335562863f04226a2fb729bfbcbdaba27cb574a04c87075a64653a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902570"
---
# <a name="certificate-request-functions"></a>Funzioni di richiesta di certificato

La CertEnroll.dll implementa cinque interfacce che possono essere usate per creare e gestire una richiesta di certificato. Di questi, [**l'interfaccia IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) rappresenta un oggetto di base astratto che definisce le firme dei metodi ereditate dalle quattro interfacce seguenti.

| Interfaccia                                                                        | Descrizione                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Consente di creare un certificato direttamente senza applicarlo a [*un'autorità*](/windows/desktop/SecGloss/c-gly) di certificazione (CA).<br/>                                                                                                            |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Rappresenta una richiesta di certificato di Gestione certificati su [*CMS*](/windows/desktop/SecGloss/c-gly) (Certificate Management Message over CMS) che può contenere una richiesta PKCS 10 annidata o un altro \# oggetto richiesta CMC.<br/> |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Rappresenta un [*oggetto richiesta PKCS \# 7*](/windows/desktop/SecGloss/p-gly) certificate message syntax (CMS) che deve contenere una richiesta PKCS \# 10 annidata.<br/>                                                                                                         |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Rappresenta una richiesta di certificato PKCS \# 10. Una richiesta PKCS 10 può essere inviata direttamente a una CA oppure può essere incapsulata da una richiesta \# PKCS \# 7 o CMC.<br/>                                                                                                                                                            |



 

È possibile usare un oggetto richiesta di certificato per inizializzare un [**oggetto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per registrare un client in una gerarchia di certificati e installare la risposta del certificato restituita dalla CA.

Ognuna delle sezioni seguenti identifica una funzione esportata da Xenroll.dll creare, enumerare o eliminare le richieste di certificato. Ogni sezione illustra anche come usare CertEnroll.dll per sostituire la funzione o indica che non esiste alcun mapping tra le due librerie:

-   [createFilePKCS10WStr](#createfilepkcs10wstr)
-   [createFileRequestWStr](#createfilerequestwstr)
-   [createPKCS10WStr](#createpkcs10wstr)
-   [CreatePKCS7RequestFromRequest](#createpkcs7requestfromrequest)
-   [createRequestWStr](#createrequestwstr)
-   [DeleteRequestCert](#deleterequestcert)
-   [enumPendingRequestWStr](#enumpendingrequestwstr)
-   [removePendingRequestWStr](#removependingrequestwstr)
-   [Reimpostazione](#reset)
-   [setPendingRequestInfoWStr](#setpendingrequestinfowstr)
-   [Argomenti correlati](#related-topics)

## <a name="createfilepkcs10wstr"></a>createFilePKCS10WStr

La [**funzione createFilePKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) in Xenroll.dll crea una richiesta di certificato PKCS 10 con codifica Base64 e la salva \# in un file.

La CertEnroll.dll non implementa direttamente la funzionalità per scrivere una richiesta in un file. È tuttavia possibile recuperare una richiesta di certificato chiamando la proprietà [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) sull'oggetto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) e creando una funzione personalizzata per copiare il valore in un file.

## <a name="createfilerequestwstr"></a>createFileRequestWStr

La [**funzione createFileRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) in Xenroll.dll crea una richiesta di certificato \# PKCS 7, PKCS 10 o CMC e la salva \# in un file.

La CertEnroll.dll non implementa direttamente la funzionalità per scrivere una richiesta in un file. È tuttavia possibile recuperare una richiesta di certificato chiamando la proprietà [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) sull'oggetto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) e creando una funzione personalizzata per copiare il valore in un file.

## <a name="createpkcs10wstr"></a>createPKCS10WStr

La [**funzione createPKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) in Xenroll.dll crea una richiesta di certificato PKCS 10 e la copia \# in una matrice di byte.

È possibile usare un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) per inizializzare una richiesta PKCS 10 da una richiesta esistente, un certificato esistente, una chiave privata, una chiave pubblica o \# un modello. [](/windows/desktop/SecGloss/p-gly) [](/windows/desktop/SecGloss/p-gly)

## <a name="createpkcs7requestfromrequest"></a>CreatePKCS7RequestFromRequest

La [**funzione CreatePKCS7RequestFromRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) in Xenroll.dll crea una richiesta di certificato PKCS 7 e la copia \# in una matrice di byte.

È possibile usare un [**oggetto IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) per inizializzare una richiesta PKCS 7 da una richiesta esistente, un certificato esistente, un oggetto richiesta interno o \# un modello.

## <a name="createrequestwstr"></a>createRequestWStr

La [**funzione createRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) in Xenroll.dll crea una richiesta di certificato \# PKCS 7, PKCS 10 o CMC e la copia \# in una matrice di byte.

Per usare la libreria CertEnroll.dll per creare richieste PKCS 7, PKCS 10 o CMC, è possibile creare e inizializzare istanze degli oggetti \# \# [**IX509CertificateRequestPkcs7,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) [**IX509CertificateRequestPkcs10 o**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) [**IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)

## <a name="deleterequestcert"></a>DeleteRequestCert

La [**funzione DeleteRequestCert**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) in Xenroll.dll specifica o recupera un valore booleano che indica se un certificato fittizio viene rimosso dopo l'installazione di una risposta del certificato.

[**L'oggetto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) in CertEnroll.dll crea automaticamente certificati fittizi nell'archivio richieste per salvare temporaneamente varie proprietà del certificato inizializzate durante il processo di registrazione. Dopo l'emissione di un certificato da parte di una CA, le proprietà vengono copiate nel nuovo certificato e il certificato fittizio viene eliminato. La CertEnroll.dll non consente di forzare la permanere di un certificato fittizio dopo l'installazione della risposta del certificato.

## <a name="enumpendingrequestwstr"></a>enumPendingRequestWStr

La [**funzione enumPendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) in Xenroll.dll recupera un valore di proprietà specificato per una richiesta in sospeso.

La CertEnroll.dll non implementa direttamente la funzionalità per rimuovere una richiesta di certificato in sospeso.

## <a name="removependingrequestwstr"></a>removePendingRequestWStr

La [**funzione removePendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) Xenroll.dll una richiesta in sospeso dall'archivio richieste.

La CertEnroll.dll non implementa direttamente la funzionalità per rimuovere una richiesta di certificato in sospeso.

## <a name="reset"></a>Reset

La [**funzione Reset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) in Xenroll.dll restituisce lo stato iniziale del controllo di registrazione certificati.

È possibile ottenere lo stesso risultato usando Certenroll.dll creare un nuovo oggetto richiesta del tipo richiesto.

## <a name="setpendingrequestinfowstr"></a>setPendingRequestInfoWStr

La [**funzione setPendingRequestInfoWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) in Xenroll.dll specifica le proprietà per la richiesta in sospeso.

La CertEnroll.dll non implementa direttamente la funzionalità per rimuovere una richiesta di certificato in sospeso. È possibile chiamare la [**proprietà CAConfigString**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring) nell'oggetto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per recuperare una stringa di configurazione, ma solo per un oggetto di registrazione attivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)
</dt> <dt>

[**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)
</dt> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

