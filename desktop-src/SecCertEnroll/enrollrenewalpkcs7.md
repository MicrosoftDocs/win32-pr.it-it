---
description: Crea un \# oggetto richiesta PKCS 7 per rinnovare un certificato esistente. L'oggetto Request utilizza una nuova coppia di chiavi, ma mantiene il provider del crittografico associato al certificato da rinnovare.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8795758a2744dcee07a100f87eb1db0a1af49eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529389"
---
# <a name="enrollrenewalpkcs7"></a>enrollRenewalPKCS7

L'esempio enrollRenewalPKCS7 crea un \# oggetto richiesta PKCS 7 per rinnovare un certificato esistente. L'oggetto Request utilizza una nuova coppia di chiavi, ma mantiene il provider del crittografico associato al certificato da rinnovare.

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollRenewalPKCS7

## <a name="discussion"></a>Discussione

Esempio enrollRenewalPKCS7:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere il nome del modello utilizzato per creare la richiesta di certificato.
2.  Recupera un certificato esistente usando il nome del modello specificato nella riga di comando o, se non è possibile trovare un certificato, tenta di registrarne uno usando il modello. Le funzioni findCertByTemplate e enrollCertByTemplate sono definite in enrollCommon. cpp.
3.  Verifica la catena di certificati e converte il certificato in un **BSTR**.
4.  Crea un oggetto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) e lo inizializza utilizzando il certificato esistente. Poiché il parametro *inheritOptions* è impostato su InheritDefault, viene creata una nuova coppia di chiavi per la richiesta, ma viene utilizzato il provider del sistema di crittografia nel certificato esistente. Per ulteriori informazioni, vedere il metodo [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) .
5.  Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inizializza usando l'oggetto della \# richiesta PKCS 7, tenta di registrarlo con l'autorità di certificazione e monitora lo stato del processo di registrazione. La funzione checkEnrollStatus è definita in enrollCommon. cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta CMC](cmc-request.md)
</dt> <dt>

[\#Richiesta di rinnovo PKCS 7](pkcs--7--renewal-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 



