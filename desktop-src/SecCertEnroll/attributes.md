---
description: Gli attributi possono essere aggiunti a una richiesta di certificato per fornire un'autorità di certificazione (CA) con informazioni aggiuntive che possono essere utilizzate durante la creazione e l'emissione di un certificato.
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
ms.openlocfilehash: e7a00c30be8bacf5593d78e21fb420c8a899dc7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753482"
---
# <a name="attributes-certificate-enrollment-api"></a>Attributi (API di registrazione certificati)

Gli attributi possono essere aggiunti a una richiesta di certificato per fornire un'autorità di certificazione (CA) con informazioni aggiuntive che possono essere utilizzate durante la creazione e l'emissione di un certificato. Ogni attributo è una struttura ad [*albero*](/windows/desktop/SecGloss/a-gly) (ASN. 1) codificata [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) che contiene un identificatore di oggetto (OID) e zero o più valori. Gli attributi vengono definiti usando le interfacce incluse con l'API di registrazione del certificato. Gli argomenti seguenti illustrano gli attributi in modo più dettagliato:

-   [Attributi supportati](supported-attributes.md)
-   [Architettura degli attributi](attribute-architecture.md)
-   [\#Attributi PKCS 7](pkcs--7-attributes.md)
-   [\#Attributi PKCS 10](pkcs--10-attributes.md)
-   [Attributi CMC](cmc-attributes.md)

 

 
