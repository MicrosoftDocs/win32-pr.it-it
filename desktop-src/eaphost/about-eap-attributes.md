---
title: Attributi EAP
description: Struttura ATTRIBUTE EAP \_ che contiene un tipo predeterminato di dati relativi a una sessione di autenticazione.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77898ccde0bbaf9660a7e4c3948cce9ec17d9e4f7773b0900333e7152520c013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117751"
---
# <a name="eap-attributes"></a>Attributi EAP

Un attributo EAP è una [**struttura ATTRIBUTE EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) che contiene un tipo predeterminato di dati relativi a una sessione di autenticazione. Gli attributi vengono usati per comunicare informazioni tra metodi EAP e supplicanti o tra metodi EAP e autenticatori. Le implementazioni di peer e autenticatori di un metodo EAP possono scambiare questi attributi in una rete.

Un elenco completo dei tipi di attributo supportati viene visualizzato nell'argomento [**EAP \_ ATTRIBUTE \_ TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="attributes-consumed-by-supplicants"></a>Attributi utilizzati dai supplicant

I tipi di attributo seguenti vengono utilizzati da supplicant 802.1X.

-   **VendorSpecific**

I tipi di attributo seguenti vengono utilizzati dai supplicant client PPP.

-   **aminimum**
-   **più di 1000**

I tipi di attributo seguenti vengono utilizzati dai supplicant del server PPP.

-   **nome utentesodeiemi**
-   **ErreplyMessage**
-   **stato di invasa**
-   **il tempo di sessione di una sessione di lavoro**
-   **1000000000000**

## <a name="attributes-exported-by-methods"></a>Attributi esportati dai metodi

I tipi di attributo seguenti possono essere esportati dai metodi EAP.

-   **passwordClearTextPassword**
-   **aquarantineSoH**
-   **idmetodo di metodo**

Il tipo di attributo seguente viene esportato dai metodi [TLS (Transport Level Security)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS) EAP.

-   **certificateOID**

I tipi di attributo seguenti vengono esportati dai [metodi di Microsoft Challenge Handshake Authentication Protocol versione 2.0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2).

-   **nome utentesodeiemi**
-   **proprietàcredentialsChanged**

Il tipo di attributo seguente viene utilizzato da Server dei criteri di rete.

-   **certificateOID**

I tipi di attributo seguenti vengono esportati dai [metodi PEAP (Protected Extensible Authentication Protocol).](/previous-versions/windows/embedded/ms899190(v=msdn.10))

-   **nome utentesodeiemi**
-   **ddedPEAPEmbeddedEAPTypeId**
-   **ssopeapFastRoamedSession**
-   **aquarantineSoH**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ATTRIBUTO \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[**TIPO DI \_ ATTRIBUTO \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 