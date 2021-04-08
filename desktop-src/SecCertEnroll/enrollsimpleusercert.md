---
description: Registra un utente finale con un'autorità di certificazione (CA) usando un modello, il nome del soggetto e la lunghezza in bit della chiave.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050242"
---
# <a name="enrollsimpleusercert"></a>enrollSimpleUserCert

L'esempio enrollSimpleUserCert registra un utente finale con un'autorità di certificazione (CA) usando un modello, il nome del soggetto e la lunghezza in bit della chiave.

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, per impostazione predefinita viene installata una versione C++ dell'esempio, nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate di registrazione del certificato \\ VC \\ enrollSimpleUserCert. Una versione C# è installata nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ X509 CSharp EnrollSimpleUserCert per la registrazione del certificato \\ \\ .

## <a name="discussion"></a>Discussione

Esempio enrollSimpleUserCert:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere il nome del modello, il nome del soggetto e la lunghezza della chiave.
2.  Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e lo inizializza usando il modello.
3.  Recupera l'oggetto richiesta di certificato interno dall'oggetto di registrazione ed esegue una query per l'oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) . La richiesta più interna è sempre una \# richiesta PKCS 10.
4.  Recupera l'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) dalla richiesta PKCS \# 10 e imposta la lunghezza della chiave specificata nella riga di comando.
5.  Crea un oggetto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , lo utilizza per codificare il nome soggetto X. 500 e aggiunge il nome alla richiesta PKCS \# 10.
6.  Tenta di registrare l'utente finale con l'autorità di certificazione e monitora lo stato di avanzamento del processo di registrazione. La funzione checkEnrollStatus è definita in enrollCommon. cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\#Richiesta PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 



