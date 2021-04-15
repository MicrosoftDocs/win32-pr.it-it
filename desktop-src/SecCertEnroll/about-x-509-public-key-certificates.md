---
description: La crittografia a chiave pubblica si basa su una coppia di chiavi pubblica e privata per crittografare e decrittografare il contenuto.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: Certificati di chiave pubblica X. 509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acd602e9b47cb7825f6d75df0fb74399b914db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569591"
---
# <a name="x509-public-key-certificates"></a>Certificati di chiave pubblica X. 509

La crittografia a chiave pubblica si basa su una coppia di chiavi pubblica e privata per crittografare e decrittografare il contenuto. Le chiavi sono correlate matematicamente e il contenuto crittografato tramite una delle chiavi può essere decrittografato solo utilizzando l'altro. La chiave privata viene mantenuta segreta. La chiave pubblica in genere è incorporata in un certificato binario e il certificato viene pubblicato in un database che può essere raggiunto da tutti gli utenti autorizzati.

Lo standard di infrastruttura a chiave pubblica (PKI) X. 509 identifica i requisiti per i certificati di chiave pubblica affidabili. Un certificato è una struttura di dati firmati che associa una chiave pubblica a una persona, un computer o un'organizzazione. I certificati vengono rilasciati da [*autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CAS). Tutti gli utenti che fanno parte di proteggere le comunicazioni che usano una chiave pubblica si affidano alla CA per verificare adeguatamente le identità dei singoli, dei sistemi o delle entità a cui rilascia i certificati. Il livello di verifica dipende in genere dal livello di sicurezza richiesto per la transazione. Se la CA può verificare adeguatamente l'identità del richiedente, firma (crittografa), codifica e rilascia il certificato.

Un certificato è una struttura di dati firmati che associa una chiave pubblica a un'entità. Nell'esempio seguente viene illustrata la sintassi [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN. 1) per il certificato [*X. 509*](/windows/desktop/SecGloss/x-gly) della versione 3.

``` syntax
-- X.509 signed certificate 

SignedContent ::= SEQUENCE 
{
  certificate         CertificateToBeSigned,
  algorithm           Object Identifier,
  signature           BITSTRING
}
 
-- X.509 certificate to be signed

CertificateToBeSigned ::= SEQUENCE 
{
  version                 [0] CertificateVersion DEFAULT v1,
  serialNumber            CertificateSerialNumber,
  signature               AlgorithmIdentifier,
  issuer                  Name
  validity                Validity,
  subject                 Name
  subjectPublicKeyInfo    SubjectPublicKeyInfo,
  issuerUniqueIdentifier  [1] IMPLICIT UniqueIdentifier OPTIONAL,
  subjectUniqueIdentifier [2] IMPLICIT UniqueIdentifier OPTIONAL,
  extensions              [3] Extensions OPTIONAL
}
```

Dall'inizio della 1998 sono state sviluppate tre versioni dello standard del certificato di chiave pubblica X. 509. Come illustrato nella figura seguente, ogni versione successiva della struttura di dati ha mantenuto i campi esistenti nelle versioni precedenti e ne ha aggiunto altri.

![certificati x. 509 versioni 1, 2 e 3](images/x509certificateversions.png)

Gli argomenti seguenti illustrano i campi disponibili in modo più dettagliato:

-   [Campi di base](about-basic-fields.md)
-   [Campi versione 2](about-version-2-fields.md)
-   [Estensioni versione 3](about-version-3-extensions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Infrastruttura a chiave pubblica (PKI)](public-key-infrastructure.md)
</dt> </dl>

 

 
