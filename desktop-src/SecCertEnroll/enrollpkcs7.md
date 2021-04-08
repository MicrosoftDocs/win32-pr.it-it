---
description: Crea una \# richiesta PKCS 7 da un certificato esistente ereditando le chiavi pubbliche e private e il modello di certificato.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34bc7f9d7b7d5ae9fa88db0dd70c177c3aa69da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750018"
---
# <a name="enrollpkcs7"></a>enrollPKCS7

L'esempio enrollPKCS7 crea una \# richiesta PKCS 7 da un certificato esistente ereditando le chiavi pubbliche e private e il modello di certificato. Il certificato esistente viene usato per firmare la richiesta. In questo esempio l'utente viene registrato in una gerarchia di certificati e viene installata la risposta del certificato. Nell'esempio viene utilizzato un certificato esistente per registrarsi e installarne uno nuovo. Per ulteriori informazioni sul rinnovo di un certificato esistente, vedere [enrollRenewalPKCS7](enrollrenewalpkcs7.md).

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollPKCS7

## <a name="discussion"></a>Discussione

Esempio enrollPKCS7:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere il nome del modello di certificato usato per trovare un certificato esistente.
2.  Recupera un certificato esistente usando il nome del modello specificato nella riga di comando o, se non è possibile trovare un certificato, tenta di registrare un nuovo certificato creato usando il modello. Le funzioni findCertByTemplate e enrollCertByTemplate sono definite in enrollCommon. cpp.
3.  Verifica la catena di certificati e converte il certificato in un **BSTR**.
4.  Crea un oggetto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) e lo inizializza utilizzando il certificato esistente. Il nuovo \# oggetto della richiesta PKCS 7 eredita le chiavi pubbliche e private e il modello dal certificato esistente.
5.  Crea un oggetto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inizializza usando il certificato esistente e lo aggiunge all'oggetto della richiesta PKCS \# 7.
6.  Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inizializza usando l'oggetto della \# richiesta PKCS 7, tenta di registrarlo con l'autorità di certificazione e monitora lo stato del processo di registrazione. La funzione checkEnrollStatus è definita in enrollCommon. cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta CMC](cmc-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 



