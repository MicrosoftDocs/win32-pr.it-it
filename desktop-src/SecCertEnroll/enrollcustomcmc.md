---
description: Consente di creare una richiesta di certificato CMC e di registrare un computer in una gerarchia di certificati.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: enrollCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752735"
---
# <a name="enrollcustomcmc"></a>enrollCustomCMC

Nell'esempio enrollCustomCMC viene creata una richiesta di certificato CMC e viene registrato un computer in una gerarchia di certificati.

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollCustomCMC

## <a name="discussion"></a>Discussione

Esempio enrollCustomCMC:

1.  Elabora gli argomenti della riga di comando seguenti:
    -   Coppia nome/valore personalizzata da aggiungere alla richiesta di certificato.
    -   Nome soggetto alternativo.
    -   Identificatore di oggetto (OID) per l'estensione utilizzo chiavi avanzato (EKU).
2.  Crea un oggetto richiesta [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e lo inizializza usando il contesto del computer.
3.  Usa la \# richiesta PKCS 10 per inizializzare un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .
4.  Crea un oggetto [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) usando l'OID specificato nella riga di comando e lo aggiunge alla raccolta Extensions per la richiesta CMC.
5.  Crea l'oggetto [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) usando il nome specificato nella riga di comando, lo aggiunge alla raccolta [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , usa la raccolta per inizializzare un'estensione [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) e la aggiunge alla raccolta Extensions per la richiesta CMC.
6.  Crea un oggetto [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) usando il nome e il valore specificati nella riga di comando e lo aggiunge alla raccolta [**IX509NAMEVALUEPAIRS**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) nella richiesta CMC.
7.  Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inizializza usando l'oggetto della richiesta CMC e recupera una stringa che contiene una richiesta con codifica Base64.
8.  Crea un oggetto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e lo usa per recuperare una stringa che contiene la configurazione della CA.
9.  Crea un oggetto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) e lo usa più le stringhe che contengono la configurazione della CA e la richiesta di certificato per inviare la richiesta all'autorità di certificazione.
10. Controlla lo stato dell'invio e, in caso di esito positivo, installa il certificato nell'archivio certificati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta CMC](cmc-request.md)
</dt> <dt>

[\#Richiesta PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 
