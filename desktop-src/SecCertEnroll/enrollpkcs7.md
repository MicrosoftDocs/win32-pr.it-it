---
description: Crea una richiesta PKCS \# 7 da un certificato esistente ereditando le chiavi pubbliche e private e il modello di certificato.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0635fdf4daacc9c7a04db98c7e34e9d3495c6f18ca3e145b166f19e3cd49610a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779952"
---
# <a name="enrollpkcs7"></a>enrollPKCS7

L'esempio enrollPKCS7 crea una richiesta PKCS 7 da un certificato esistente ereditando le chiavi \# pubbliche e private e il modello di certificato. Il certificato esistente viene usato per firmare la richiesta. Questo esempio registra l'utente in una gerarchia di certificati e installa la risposta del certificato. L'esempio usa un certificato esistente per registrare e installare un nuovo certificato. Per altre informazioni sul rinnovo di un certificato esistente, vedere [enrollRenewalPKCS7.](enrollrenewalpkcs7.md)

## <a name="location"></a>Località

Quando si installa Microsoft Windows Software Development Kit (SDK), l'esempio viene installato, per impostazione predefinita, nella cartella *%ProgramFiles%* \\ Microsoft SDK Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollPKCS7 .

## <a name="discussion"></a>Discussione

Esempio enrollPKCS7:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere il nome del modello di certificato usato per trovare un certificato esistente.
2.  Recupera un certificato esistente usando il nome del modello specificato nella riga di comando o, se non è possibile trovare un certificato, tenta di registrarne uno nuovo creato usando il modello. Le funzioni findCertByTemplate e enrollCertByTemplate sono definite in enrollCommon.cpp.
3.  Verifica la catena di certificati e converte il certificato in **BSTR.**
4.  Crea un [**oggetto IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) e lo inizializza usando il certificato esistente. Il nuovo oggetto richiesta PKCS 7 eredita le chiavi private e pubbliche e il \# modello dal certificato esistente.
5.  Crea un [**oggetto ISignerCertificate,**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) lo inizializza usando il certificato esistente e lo aggiunge all'oggetto richiesta PKCS \# 7.
6.  Crea un [**oggetto IX509Enrollment,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) lo inizializza usando l'oggetto richiesta PKCS 7, tenta di registrarlo con la CA e monitora lo stato del processo \# di registrazione. La funzione checkEnrollStatus è definita in enrollCommon.cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta CMC](cmc-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 



