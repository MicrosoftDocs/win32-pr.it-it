---
description: Implementa l'interfaccia IX509Enrollment.
ms.assetid: bcf5c2f0-b99f-4de5-83f4-44f17dc31cd4
title: Funzioni di risposta ai certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f82922ce2b0cdfad370bbfbf4d1fd3a135c19d5ba613110364f7283ec12a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902401"
---
# <a name="certificate-response-functions"></a>Funzioni di risposta ai certificati

CertEnroll.dll implementa [**l'interfaccia IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per inviare una richiesta di certificato client e installare la risposta da [*un'autorità*](/windows/desktop/SecGloss/c-gly) di certificazione (CA).

Il processo di registrazione può soddisfare i tre scenari seguenti:

<dl> Registrazione fuori banda

1.  Chiamare qualsiasi metodo di inizializzazione implementato [**dall'oggetto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
2.  Chiamare il [**metodo CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) per recuperare la richiesta.
3.  Inviare la richiesta fuori banda (manualmente o usando un altro processo).
4.  Ricevere la risposta da una CA.
5.  Chiamare il [**metodo InstallResponse.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)

  
Registrazione automatica

1.  Chiamare qualsiasi metodo di inizializzazione implementato [**dall'oggetto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
2.  Chiamare il [**metodo Enroll.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll)

  
Registrazione ritardata

1.  Chiamare qualsiasi metodo di inizializzazione implementato [**dall'oggetto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
2.  Chiamare il [**metodo CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) per recuperare la richiesta.
3.  Archiviare la richiesta fino a quando non si è pronti per inviarla.
4.  Quando si è pronti per la registrazione, chiamare il [**metodo Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-initialize) per reinizializzare l'oggetto di registrazione.
5.  Chiamare il [**metodo InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) quando la CA restituisce un certificato.

  
</dl>

Durante il processo di registrazione, è possibile chiamare la proprietà [**Status**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_status) sull'oggetto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per recuperare un valore di enumerazione [**EnrollmentEnrollStatus**](/windows/desktop/api/CertEnroll/ne-certenroll-enrollmentenrollstatus) che identifica se la registrazione è riuscita, è in sospeso, è stata ignorata, ha generato un errore o è stata negata.

Ognuna delle sezioni seguenti identifica una funzione esportata da Xenroll.dll per installare una risposta del certificato da una CA. Ogni sezione illustra anche come usare CertEnroll.dll per sostituire la funzione o indica che non esiste alcun mapping tra le due librerie:

-   [acceptFilePKCS7WStr](#acceptfilepkcs7wstr)
-   [acceptFileResponseWStr](#acceptfileresponsewstr)
-   [acceptPKCS7Blob](#acceptpkcs7blob)
-   [acceptResponseBlob](#acceptresponseblob)
-   [getCertContextFromFileResponseWStr](#getcertcontextfromfileresponsewstr)
-   [getCertContextFromPKCS7](#getcertcontextfrompkcs7)
-   [getCertContextFromResponseBlob](#getcertcontextfromresponseblob)
-   [InstallPKCS7Blob](#installpkcs7blobex)
-   [InstallPKCS7BlobEx](#installpkcs7blobex)
-   [SPCFileNameWStr](#spcfilenamewstr)
-   [WriteCertToCSP](#writecerttocsp)
-   [WriteCertToUserDS](#writecerttouserds)
-   [Argomenti correlati](#related-topics)

## <a name="acceptfilepkcs7wstr"></a>acceptFilePKCS7WStr

La [**funzione acceptFilePKCS7WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr) in Xenroll.dll installa una risposta [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) da un file.

La CertEnroll.dll non implementa direttamente la funzionalità per installare una risposta di certificato PKCS \# 7 da un file. È tuttavia possibile creare una funzione personalizzata per leggere i dati del file in una matrice di byte e chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare la risposta.

Se si specifica il **valore AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario che esista un certificato fittizio, consentendo di installare un certificato senza prima chiamare [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) [**o CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, è necessario che nell'archivio richieste sia presente un certificato fittizio. È quindi necessario specificare **AllowNone** per il primo parametro.

## <a name="acceptfileresponsewstr"></a>acceptFileResponseWStr

La [**funzione acceptFileResponseWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptfileresponsewstr) in Xenroll.dll installa una risposta di certificato PKCS 7 o \# CMC da un file.

La CertEnroll.dll non implementa direttamente la funzionalità per installare una risposta del certificato da un file. È tuttavia possibile creare una funzione personalizzata per leggere i dati del file in una matrice di byte e chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare la risposta PKCS \# 7 o CMC.

Se si specifica il **valore AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario che esista un certificato fittizio, consentendo di installare un certificato senza prima chiamare [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) [**o CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, è necessario che nell'archivio richieste sia presente un certificato fittizio. È quindi necessario specificare **AllowNone** per il primo parametro.

## <a name="acceptpkcs7blob"></a>acceptPKCS7Blob

La [**funzione acceptPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob) in Xenroll.dll installa una risposta PKCS \# 7 contenuta in una matrice di byte.

È possibile chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare un messaggio PKCS \# 7. Se si specifica il valore **AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario che esista un certificato fittizio, consentendo di installare la risposta PKCS 7 senza prima chiamare Enroll o \# [**CreateRequest.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) [](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) Tuttavia, se si installa un certificato usando uno script Web, è necessario che nell'archivio richieste sia presente un certificato fittizio. È quindi necessario specificare **AllowNone** per il primo parametro.

## <a name="acceptresponseblob"></a>acceptResponseBlob

La [**funzione acceptResponseBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptresponseblob) in Xenroll.dll una risposta di certificato PKCS 7 o \# CMC contenuta in una matrice di byte.

È possibile chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare una risposta PKCS \# 7 o CMC. Se si specifica il **valore AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario che esista un certificato fittizio, consentendo di installare la risposta senza prima chiamare [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) [**o CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, è necessario che nell'archivio richieste sia presente un certificato fittizio. È quindi necessario specificare **AllowNone** per il primo parametro.

## <a name="getcertcontextfromfileresponsewstr"></a>getCertContextFromFileResponseWStr

La [**funzione getCertContextFromFileResponseWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromfileresponsewstr) in Xenroll.dll recupera il certificato client da un file.

La CertEnroll.dll libreria non implementa direttamente la funzionalità per recuperare un certificato da una risposta ca salvata in un file. È tuttavia possibile creare una funzione personalizzata per leggere i dati del file in una matrice di byte e chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare la risposta PKCS 7 o CMC e chiamare la proprietà Certificate per recuperare il \# certificato. [](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate)

Se si specifica il **valore AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario che esista un certificato fittizio, consentendo di installare un certificato senza prima chiamare [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) [**o CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, è necessario che nell'archivio richieste sia presente un certificato fittizio. È quindi necessario specificare **AllowNone** per il primo parametro.

## <a name="getcertcontextfrompkcs7"></a>getCertContextFromPKCS7

La [**funzione getCertContextFromPKCS7**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-getcertcontextfrompkcs7) in Xenroll.dll recupera il certificato client da una risposta PKCS \# 7.

È possibile chiamare la [**proprietà Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) sull'oggetto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per recuperare un certificato dopo aver chiamato il metodo [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) [**o InstallResponse.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)

## <a name="getcertcontextfromresponseblob"></a>getCertContextFromResponseBlob

La [**funzione getCertContextFromResponseBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromresponseblob) in Xenroll.dll recupera un certificato client da una risposta PKCS \# 7 o CMC.

È possibile chiamare la [**proprietà Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) sull'oggetto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per recuperare un certificato dopo aver chiamato il metodo [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) [**o InstallResponse.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse)

## <a name="installpkcs7blob"></a>InstallPKCS7Blob

La [**funzione InstallPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-installpkcs7blob) in Xenroll.dll installa una risposta PKCS \# 7.

È possibile chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare una risposta PKCS \# 7 o CMC. Se si specifica il **valore AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario che esista un certificato fittizio, consentendo di installare la risposta senza prima chiamare [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) [**o CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, è necessario che nell'archivio richieste sia presente un certificato fittizio. È quindi necessario specificare **AllowNone** per il primo parametro.

## <a name="installpkcs7blobex"></a>InstallPKCS7BlobEx

La [**funzione InstallPKCS7BlobEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-installpkcs7blobex) in Xenroll.dll installa una risposta PKCS 7 e restituisce il \# numero di certificati installati.

È possibile chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare una risposta PKCS \# 7 o CMC. Se si specifica il **valore AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario che esista un certificato fittizio, consentendo di installare la risposta senza prima chiamare [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) [**o CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, è necessario che nell'archivio richieste sia presente un certificato fittizio. È quindi necessario specificare **AllowNone** per il primo parametro.

## <a name="spcfilenamewstr"></a>SPCFileNameWStr

La [**funzione SPCFileNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr) in Xenroll.dll specifica o recupera il nome del file in cui salvare la risposta del certificato. La CertEnroll.dll non implementa funzionalità che consentono di copiare un certificato in un file specifico. Il processo di registrazione installa automaticamente la catena di certificati nei file negli archivi appropriati.

## <a name="writecerttocsp"></a>WriteCertToCSP

La [**funzione WriteCertToCSP**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp) in Xenroll.dll specifica o recupera un valore booleano che indica se un certificato deve essere scritto in un [*provider*](/windows/desktop/SecGloss/c-gly) del servizio di crittografia (CSP). In genere, se questa funzione viene chiamata, il provider è un [*smart card*](/windows/desktop/SecGloss/s-gly).

In CertEnroll.dll, quando un client chiama il metodo [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) per inviare una richiesta per un certificato smart card e viene emesso un certificato, [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) installa automaticamente il certificato nel smart card, presupponendo che la scheda sia installata nel lettore. Anche [**il metodo InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) scrive automaticamente il certificato nel smart card.

## <a name="writecerttouserds"></a>WriteCertToUserDS

La [**funzione WriteCertToUserDS**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds) in Xenroll.dll specifica o recupera un valore booleano che indica se un certificato deve essere salvato nell'archivio di Active Directory. La CertEnroll.dll non implementa funzionalità che consentono di specificare un archivio in cui copiare un certificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**Registrazione IX509**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
