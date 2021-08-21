---
description: Il formato del certificato X.509 versione 3 identifica più estensioni che possono essere aggiunte a un certificato.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Estensioni (API di registrazione certificati)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 534c3cf9268f21c36d982a627de2e1b293ffdca1e1fd4ffc2acd0db9f7d6059b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867941"
---
# <a name="extensions-certificate-enrollment-api"></a>Estensioni (API di registrazione certificati)

Il formato del certificato X.509 versione 3 identifica più estensioni che possono essere aggiunte a un certificato. Le estensioni forniscono informazioni avanzate sull'utilizzo delle chiavi, i criteri e i vincoli dei certificati, i moduli dei nomi alternativi e altro ancora. È possibile usare [**l'interfaccia IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) per definire un valore di estensione. Molte delle estensioni comuni possono essere create usando interfacce predefinite derivate da **IX509Extension.** Una raccolta di estensioni viene aggiunta a una richiesta di certificato includendo la raccolta negli attributi della richiesta. Per altre informazioni, vedere i seguenti argomenti:

-   [Estensioni supportate](supported-extensions.md)
-   [Estensioni PKCS \# 10](pkcs--10-extensions.md)
-   [Estensioni CMC](cmc-extensions.md)

 

 



