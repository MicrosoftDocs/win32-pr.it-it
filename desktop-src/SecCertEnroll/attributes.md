---
description: "Attributi (API registrazione certificati): è possibile aggiungere attributi a una richiesta di certificato per fornire a un'autorità di certificazione (CA) informazioni aggiuntive che può usare durante la creazione e il rilascio di un certificato."
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attributi (API registrazione certificati)
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
ms.openlocfilehash: aec93ec47a700902cb1275e25af6649e6988b76f7204b01487249e0130dd35b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903103"
---
# <a name="attributes-certificate-enrollment-api"></a>Attributi (API registrazione certificati)

Gli attributi possono essere aggiunti a una richiesta di certificato per fornire a un'autorità di certificazione (CA) informazioni aggiuntive che può usare durante la creazione e il rilascio di un certificato. Ogni attributo è una struttura ASN.1 [](/windows/desktop/SecGloss/d-gly) [*(Abstract Syntax Notation One)*](/windows/desktop/SecGloss/a-gly) codificata Distinguished Encoding Rules (DER) che contiene un identificatore di oggetto (OID) e zero o più valori. Gli attributi vengono definiti usando le interfacce incluse nell'API Di registrazione certificati. Gli argomenti seguenti illustrano gli attributi in modo più dettagliato:

-   [Attributi supportati](supported-attributes.md)
-   [Architettura degli attributi](attribute-architecture.md)
-   [Attributi PKCS \# 7](pkcs--7-attributes.md)
-   [Attributi PKCS \# 10](pkcs--10-attributes.md)
-   [Attributi CMC](cmc-attributes.md)

 

 
