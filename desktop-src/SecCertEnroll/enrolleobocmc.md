---
description: Consente di creare una richiesta di certificato CMC per conto di un altro utente e di registrare l'utente in una gerarchia di certificati.
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: enrollEOBOCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca888d949054d695056d42045335f17dfca2f4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526994"
---
# <a name="enrolleobocmc"></a>enrollEOBOCMC

L'esempio enrollEOBOCMC consente di creare una richiesta di certificato CMC per conto di un altro utente e di registrare l'utente in una gerarchia di certificati. Per conto di un altro utente, la registrazione richiede che la richiesta di certificato venga firmata utilizzando un certificato dell'agente di registrazione.

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollEOBOCMC

## <a name="discussion"></a>Discussione

Esempio enrollEOBOCMC:

1.  Elabora gli argomenti della riga di comando seguenti:
    -   Nome di un modello di certificato.
    -   Nome dell'utente che ha richiesto il certificato.
    -   Nome di un file PFX (Personal Information Exchange) in cui salvare la richiesta.
    -   Password da utilizzare con il file PFX.
    -   Nome del modello di agente di registrazione facoltativo. Il modello viene usato per creare un certificato dell'agente di registrazione, se non ne esiste alcuno nell'archivio certificati.
2.  Crea un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e lo inizializza usando il modello di certificato specificato nella riga di comando.
3.  Aggiunge il nome del richiedente all'oggetto della richiesta CMC.
4.  Recupera un certificato dell'agente di registrazione esistente o, se non è possibile trovarne uno, crea una richiesta di certificato dal modello dell'agente di registrazione specificato nella riga di comando e tenta di registrarla.
5.  Verifica la catena di certificati che contiene il certificato dell'agente di registrazione.
6.  Crea un oggetto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inizializza usando il certificato dell'agente di registrazione, recupera la raccolta [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) dall'oggetto della richiesta CMC e aggiunge l'oggetto certificato di firma dell'agente di registrazione alla raccolta. L'oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) illustrato nel passaggio successivo usa il certificato per firmare la richiesta CMC.
7.  Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inizializza usando la richiesta CMC, tenta di registrarlo e controlla lo stato di avanzamento del processo di registrazione.
8.  Esporta il certificato installato in un file PFX. Il file è protetto tramite la password specificata nella riga di comando. La funzione EncodeToFileW è definita in enrollCommon. cpp.
9.  Elimina il certificato dall'archivio certificati. Le funzioni usate nell'esempio di codice seguente sono reperibili nella documentazione di CryptoAPI.
10. Elimina la chiave privata dal computer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta EOBO di CMC](cmc-eobo-request.md)
</dt> <dt>

[\#Richiesta PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 



