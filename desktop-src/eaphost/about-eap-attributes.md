---
title: Attributi EAP
description: È una \_ struttura di attributi EAP che contiene un tipo di dati predeterminato relativo a una sessione di autenticazione.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "106300722"
---
# <a name="eap-attributes"></a>Attributi EAP

Un attributo EAP è una struttura dell' [**\_ attributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) che contiene un tipo di dati predeterminato relativo a una sessione di autenticazione. Gli attributi vengono usati per comunicare le informazioni tra i metodi EAP e i supplicant o tra i metodi e gli autenticatori EAP. Le implementazioni peer e Authenticator di un metodo EAP possono scambiare questi attributi in una rete.

Nell'argomento [**\_ \_ tipo di attributo EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)viene visualizzato un elenco completo dei tipi di attributo supportati.

## <a name="attributes-consumed-by-supplicants"></a>Attributi utilizzati dai supplicant

I tipi di attributo seguenti vengono utilizzati dai supplicant 802.1 X.

-   **eatVendorSpecific**

I tipi di attributo seguenti vengono utilizzati dai supplicant client PPP.

-   **eatMinimum**
-   **eatEAPTLV**

I tipi di attributo seguenti vengono utilizzati dai supplicant server PPP.

-   **eatUserName**
-   **eatReplyMessage**
-   **eatState**
-   **eatSessionTimeout**
-   **eatEAPMessage**

## <a name="attributes-exported-by-methods"></a>Attributi esportati dai metodi

I tipi di attributo seguenti possono essere esportati dai metodi EAP.

-   **eatClearTextPassword**
-   **eatQuarantineSoH**
-   **eatMethodId**

Il tipo di attributo seguente viene esportato dai metodi [TLS (Transport Level Security](/previous-versions/windows/embedded/ms885336(v=msdn.10)) ) EAP (EAP-TLS).

-   **eatCertificateOID**

I tipi di attributo seguenti sono esportati dai metodi [Microsoft Challenge Handshake Authentication Protocol versione 2,0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2).

-   **eatUserName**
-   **eatCredentialsChanged**

Il tipo di attributo seguente viene utilizzato da server dei criteri di rete.

-   **eatCertificateOID**

I tipi di attributo seguenti sono esportati da metodi [PEAP (Protected Extensible Authentication Protocol)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) .

-   **eatUserName**
-   **eatPEAPEmbeddedEAPTypeId**
-   **eatPEAPFastRoamedSession**
-   **eatQuarantineSoH**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_attributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[**\_tipo di attributo EAP \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 