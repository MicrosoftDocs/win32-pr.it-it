---
description: Crea una richiesta PKCS \# 10 personalizzata e tenta di registrarla in un'autorità di certificazione globale (enterprise).
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb88a2295217874a12da8b701a46f8dafe3db1cbf53d01273222e607195a789a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780040"
---
# <a name="enrollcustompkcs10_2"></a>enrollCustomPKCS10 \_ 2

L'esempio enrollCustomPKCS10 2 crea una richiesta PKCS 10 personalizzata e tenta di registrarla in un'autorità di \_ \# certificazione globale (enterprise). [](/windows/desktop/SecGloss/c-gly)

## <a name="location"></a>Località

Quando si installa Microsoft Windows Software Development Kit (SDK), l'esempio viene installato per impostazione predefinita nella cartella *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCustomPKCS10 \_ 2.

## <a name="discussion"></a>Discussione

L'esempio enrollCustomPKCS10 \_ 2:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere il nome di un modello e il nome di un provider del servizio di crittografia.
2.  Crea un [**oggetto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e lo inizializza usando il nome del modello specificato nella riga di comando.
3.  Recupera la richiesta [*di certificato dall'oggetto*](/windows/desktop/SecGloss/c-gly) di registrazione.
4.  Recupera la richiesta PKCS \# 10 più interna dall'oggetto richiesta di certificato ottenuto nel passaggio 3.
5.  Recupera una [*chiave privata*](/windows/desktop/SecGloss/p-gly) dalla richiesta PKCS \# 10.
6.  Crea una [**raccolta ICspInformations,**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) aggiunge i provider di crittografia disponibili alla raccolta e quindi recupera un [**oggetto ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) per il provider specificato nella riga di comando.
7.  Imposta l'oggetto stato sulla chiave privata.
8.  Tenta di registrare la [*richiesta di certificato*](/windows/desktop/SecGloss/c-gly).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta PKCS \# 10](pkcs--10-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 
