---
description: "Attributi (API di registrazione certificati): è possibile aggiungere attributi a una richiesta di certificato per fornire a un'autorità di certificazione (CA) informazioni aggiuntive che può usare durante la creazione e il rilascio di un certificato."
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attributi (API di registrazione certificati)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 93414156c7fa6e46fe80995d8d01eadc28796ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118429"
---
# <a name="attributes-certificate-enrollment-api"></a>Attributi (API di registrazione certificati)

È possibile aggiungere attributi a una richiesta di certificato per fornire a un'autorità di certificazione (CA) informazioni aggiuntive che può usare durante la creazione e il rilascio di un certificato. Ogni attributo è una [*struttura*](/windows/desktop/SecGloss/d-gly) ASN.1 [*(Abstract Syntax Notation One)*](/windows/desktop/SecGloss/a-gly) codificata Distinguished Encoding Rules (DER) che contiene un identificatore di oggetto (OID) e zero o più valori. Gli attributi vengono definiti usando le interfacce incluse nell'API di registrazione certificati. Gli argomenti seguenti illustrano gli attributi in modo più dettagliato:

-   [Attributi supportati](supported-attributes.md)
-   [Architettura degli attributi](attribute-architecture.md)
-   [Attributi PKCS \# 7](pkcs--7-attributes.md)
-   [Attributi PKCS \# 10](pkcs--10-attributes.md)
-   [Attributi CMC](cmc-attributes.md)

 

 
