---
description: La crittografia a chiave pubblica si basa su una coppia di chiavi pubblica e privata per crittografare e decrittografare il contenuto.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: Certificati a chiave pubblica X.509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1eb40e57114f4509884df3a5ac36e7ae8ea0486817ff300d58f4273d51c123
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903254"
---
# <a name="x509-public-key-certificates"></a>Certificati a chiave pubblica X.509

La crittografia a chiave pubblica si basa su una coppia di chiavi pubblica e privata per crittografare e decrittografare il contenuto. Le chiavi sono matematicamente correlate e il contenuto crittografato usando una delle chiavi può essere decrittografato solo usando l'altro. La chiave privata viene mantenuta segreta. La chiave pubblica è in genere incorporata in un certificato binario e il certificato viene pubblicato in un database raggiungibile da tutti gli utenti autorizzati.

Lo standard X.509 public key infrastructure (PKI) identifica i requisiti per certificati a chiave pubblica affidabili. Un certificato è una struttura di dati firmati che associa una chiave pubblica a una persona, un computer o un'organizzazione. I certificati vengono [*rilasciati dalle*](/windows/desktop/SecGloss/c-gly) autorità di certificazione (CA). Tutti gli utenti che sono parti per proteggere le comunicazioni che usano una chiave pubblica si basano sulla CA per verificare in modo adeguato le identità delle persone, dei sistemi o delle entità a cui emissione certificati. Il livello di verifica dipende in genere dal livello di sicurezza necessario per la transazione. Se l'autorità di certificazione è in grado di verificare in modo idoneo l'identità del richiedente, firma (crittografa), codifica ed elava il certificato.

Un certificato è una struttura di dati firmati che associa una chiave pubblica a un'entità. La sintassi ASN.1 [*(Abstract Syntax Notation One)*](/windows/desktop/SecGloss/a-gly) per il certificato [*X.509*](/windows/desktop/SecGloss/x-gly) versione 3 è illustrata nell'esempio seguente.

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

Dal suo inizio nel 1998, si sono evolute tre versioni dello standard del certificato a chiave pubblica X.509. Come illustrato nella figura seguente, in ogni versione successiva della struttura dei dati sono stati mantenuti i campi esistenti nelle versioni precedenti e ne sono stati aggiunti altri.

![Certificati x.509 versioni 1, 2 e 3](images/x509certificateversions.png)

Gli argomenti seguenti illustrano i campi disponibili in modo più dettagliato:

-   [Campi di base](about-basic-fields.md)
-   [Campi della versione 2](about-version-2-fields.md)
-   [Estensioni della versione 3](about-version-3-extensions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Infrastruttura a chiave pubblica (PKI)](public-key-infrastructure.md)
</dt> </dl>

 

 
