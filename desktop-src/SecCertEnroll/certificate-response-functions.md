---
description: Implementa l'interfaccia metodo IX509Enrollment.
ms.assetid: bcf5c2f0-b99f-4de5-83f4-44f17dc31cd4
title: Funzioni di risposta del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eec71d0493fa4961988b86db0397d0fd516508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314726"
---
# <a name="certificate-response-functions"></a>Funzioni di risposta del certificato

CertEnroll.dll implementa l'interfaccia [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per inviare una richiesta di certificato client e installare la risposta da un' [*autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CA).

Il processo di registrazione può supportare i tre scenari seguenti:

<dl> Registrazione fuori banda

1.  Chiamare qualsiasi metodo di inizializzazione implementato dall'oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Chiamare il metodo [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) per recuperare la richiesta.
3.  Inviare la richiesta fuori banda (manualmente o tramite un altro processo).
4.  Ricevere la risposta da un'autorità di certificazione.
5.  Chiamare il metodo [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) .

  
Registrazione automatica

1.  Chiamare qualsiasi metodo di inizializzazione implementato dall'oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Chiamare il metodo di [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) .

  
Registrazione ritardata

1.  Chiamare qualsiasi metodo di inizializzazione implementato dall'oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Chiamare il metodo [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) per recuperare la richiesta.
3.  Archiviare la richiesta fino a quando non si è pronti per l'invio.
4.  Quando si è pronti per la registrazione, chiamare il metodo [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-initialize) per reinizializzare l'oggetto di registrazione.
5.  Chiamare il metodo [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) quando la CA restituisce un certificato.

  
</dl>

Durante il processo di registrazione, è possibile chiamare la proprietà [**status**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_status) nell'oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per recuperare un valore di enumerazione [**EnrollmentEnrollStatus**](/windows/desktop/api/CertEnroll/ne-certenroll-enrollmentenrollstatus) che indica se la registrazione ha avuto esito positivo, è in sospeso, è stata ignorata, ha generato un errore o è stata negata.

Ognuna delle sezioni seguenti identifica una funzione esportata da Xenroll.dll per installare una risposta del certificato da un'autorità di certificazione. In ogni sezione viene inoltre illustrato come utilizzare CertEnroll.dll per sostituire la funzione o indicare che non esiste alcun mapping tra le due librerie:

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

La funzione [**acceptFilePKCS7WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr) in Xenroll.dll installa una risposta [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) da un file.

La libreria CertEnroll.dll non implementa direttamente le funzionalità per installare una \# risposta del certificato PKCS 7 da un file. È tuttavia possibile creare una funzione personalizzata per leggere i dati del file in una matrice di byte e chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare la risposta.

Se si specifica il valore **AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario un certificato fittizio, in modo da consentire l'installazione di un certificato senza prima chiamare [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, deve esistere un certificato fittizio nell'archivio richieste. È pertanto necessario specificare **AllowNone** per il primo parametro.

## <a name="acceptfileresponsewstr"></a>acceptFileResponseWStr

La funzione [**acceptFileResponseWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptfileresponsewstr) in Xenroll.dll installa una \# risposta del certificato PKCS 7 o CMC da un file.

La libreria CertEnroll.dll non implementa direttamente le funzionalità per installare una risposta del certificato da un file. È tuttavia possibile creare una funzione personalizzata per leggere i dati dei file in una matrice di byte e chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare la \# risposta PKCS 7 o CMC.

Se si specifica il valore **AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario un certificato fittizio, in modo da consentire l'installazione di un certificato senza prima chiamare [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, deve esistere un certificato fittizio nell'archivio richieste. È pertanto necessario specificare **AllowNone** per il primo parametro.

## <a name="acceptpkcs7blob"></a>acceptPKCS7Blob

La funzione [**acceptPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob) in Xenroll.dll installa una \# risposta PKCS 7 contenuta in una matrice di byte.

Per installare un messaggio PKCS 7, è possibile chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) \# . Se si specifica il valore **AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario un certificato fittizio, in modo da consentire l'installazione della \# risposta PKCS 7 senza prima chiamare [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, deve esistere un certificato fittizio nell'archivio richieste. È pertanto necessario specificare **AllowNone** per il primo parametro.

## <a name="acceptresponseblob"></a>acceptResponseBlob

La funzione [**acceptResponseBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptresponseblob) in Xenroll.dll installa una \# risposta del certificato PKCS 7 o CMC contenuta in una matrice di byte.

È possibile chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare una \# risposta PKCS 7 o CMC. Se si specifica il valore **AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario un certificato fittizio, in modo da consentire l'installazione della risposta senza prima chiamare [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, deve esistere un certificato fittizio nell'archivio richieste. È pertanto necessario specificare **AllowNone** per il primo parametro.

## <a name="getcertcontextfromfileresponsewstr"></a>getCertContextFromFileResponseWStr

La funzione [**getCertContextFromFileResponseWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromfileresponsewstr) in Xenroll.dll Recupera il certificato client da un file.

La libreria CertEnroll.dll non implementa direttamente le funzionalità per recuperare un certificato da una risposta della CA salvata in un file. È tuttavia possibile creare una funzione personalizzata per leggere i dati dei file in una matrice di byte e chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare la \# risposta PKCS 7 o CMC e chiamare la proprietà [**Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) per recuperare il certificato.

Se si specifica il valore **AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario un certificato fittizio, in modo da consentire l'installazione di un certificato senza prima chiamare [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, deve esistere un certificato fittizio nell'archivio richieste. È pertanto necessario specificare **AllowNone** per il primo parametro.

## <a name="getcertcontextfrompkcs7"></a>getCertContextFromPKCS7

La funzione [**getCertContextFromPKCS7**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-getcertcontextfrompkcs7) in Xenroll.dll Recupera il certificato client da una \# risposta PKCS 7.

È possibile chiamare la proprietà [**Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) sull'oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per recuperare un certificato dopo aver chiamato il metodo di [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) .

## <a name="getcertcontextfromresponseblob"></a>getCertContextFromResponseBlob

La funzione [**getCertContextFromResponseBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromresponseblob) in Xenroll.dll recupera un certificato client da una \# risposta PKCS 7 o CMC.

È possibile chiamare la proprietà [**Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) sull'oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per recuperare un certificato dopo aver chiamato il metodo di [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) .

## <a name="installpkcs7blob"></a>InstallPKCS7Blob

La funzione [**InstallPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-installpkcs7blob) in Xenroll.dll installa una \# risposta PKCS 7.

È possibile chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare una \# risposta PKCS 7 o CMC. Se si specifica il valore **AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario un certificato fittizio, in modo da consentire l'installazione della risposta senza prima chiamare [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, deve esistere un certificato fittizio nell'archivio richieste. È pertanto necessario specificare **AllowNone** per il primo parametro.

## <a name="installpkcs7blobex"></a>InstallPKCS7BlobEx

La funzione [**InstallPKCS7BlobEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-installpkcs7blobex) in Xenroll.dll installa una \# risposta PKCS 7 e restituisce il numero di certificati installati.

È possibile chiamare [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) per installare una \# risposta PKCS 7 o CMC. Se si specifica il valore **AllowNoOutstandingRequest** dell'enumerazione [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) per il primo parametro di [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), non è necessario un certificato fittizio, in modo da consentire l'installazione della risposta senza prima chiamare [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) o [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Tuttavia, se si installa un certificato usando uno script Web, deve esistere un certificato fittizio nell'archivio richieste. È pertanto necessario specificare **AllowNone** per il primo parametro.

## <a name="spcfilenamewstr"></a>SPCFileNameWStr

La funzione [**SPCFileNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr) in Xenroll.dll specifica o Recupera il nome del file in cui salvare la risposta al certificato. La libreria CertEnroll.dll non implementa la funzionalità che consente di copiare un certificato in un file specifico. Il processo di registrazione installa automaticamente la catena di certificati in file negli archivi appropriati.

## <a name="writecerttocsp"></a>WriteCertToCSP

La funzione [**WriteCertToCSP**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp) in Xenroll.dll specifica o recupera un valore booleano che indica se un certificato deve essere scritto in un [*provider del servizio di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP). In genere, se questa funzione viene chiamata, il provider è una [*Smart Card*](/windows/desktop/SecGloss/s-gly).

In CertEnroll.dll, quando un client chiama il metodo di [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) per inviare una richiesta per un certificato smart card e viene emesso un certificato, [**registra**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) installa automaticamente il certificato nella smart card, presupponendo che la scheda sia installata nel lettore. Anche il metodo [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) scrive automaticamente il certificato nella smart card.

## <a name="writecerttouserds"></a>WriteCertToUserDS

La funzione [**WriteCertToUserDS**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds) in Xenroll.dll specifica o recupera un valore booleano che indica se un certificato deve essere salvato nell'archivio Active Directory. La libreria CertEnroll.dll non implementa la funzionalità che consente di specificare un archivio in cui copiare un certificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**Metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
