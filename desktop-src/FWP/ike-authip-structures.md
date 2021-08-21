---
title: Strutture IKE/AuthIP
description: Strutture IKE/AuthIP
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de46cd72ec382dd360e6311930e946da3bf4189855adeaa49915b15ce3a9865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069091"
---
# <a name="ikeauthip-structures"></a>Strutture IKE/AuthIP

## <a name="in-this-section"></a>Contenuto della sezione

-   [**METODO DI \_ AUTENTICAZIONE IKEEXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [**METODO DI \_ AUTENTICAZIONE IKEEXT1 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [**METODO DI \_ AUTENTICAZIONE IKEEXT2 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**IKEEXT \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**IKEEXT \_ CERT \_ NAME0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**IKEEXT \_ CERT \_ ROOT \_ CONFIG0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [**AUTENTICAZIONE DEL \_ CERTIFICATO IKEEXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [**AUTENTICAZIONE DEL \_ CERTIFICATO IKEEXT1 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [**AUTENTICAZIONE DEL \_ CERTIFICATO IKEEXT2 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**CREDENZIALI DEL \_ CERTIFICATO IKEEXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [**CREDENZIALI CERTIFICATO \_ \_ IKEEXT1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [**CRITERI DEL \_ CERTIFICATO IKEEXT0 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**ALGORITMO \_ DI CRITTOGRAFIA IKEEXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [**STATISTICHE COMUNI \_ \_ IKEEXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [**STATISTICHE COMUNI \_ \_ IKEEXT1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [**COPPIA DI \_ COOKIE IKEEXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [**IKEEXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [**IKEEXT \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [**CREDENZIALI \_ IKEEXT2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [**CREDENZIALI \_ IKEEXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [**CREDENZIALI \_ IKEEXT1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [**CREDENZIALI \_ IKEEXT2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [**COPPIA DI \_ CREDENZIALI IKEEXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [**COPPIA DI \_ CREDENZIALI IKEEXT1 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [**COPPIA DI \_ CREDENZIALI IKEEXT2 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [**IKEEXT \_ EAP \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [**IKEEXT \_ EM \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [**IKEEXT \_ EM \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [**IKEEXT \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**ALGORITMO DI \_ INTEGRITÀ IKEEXT0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [**STATISTICHE COMUNI \_ SPECIFICHE DELLA VERSIONE IP IKEEXT0 \_ \_ \_ \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [**STATISTICHE COMUNI \_ SPECIFICHE DELLA VERSIONE IP IKEEXT1 \_ \_ \_ \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [**STATISTICHE \_ KEYMODULE SPECIFICHE DELLA VERSIONE IP IKEEXT0 \_ \_ \_ \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [**IKEEXT \_ IP \_ VERSION \_ SPECIFIC \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [**IKEEXT \_ IPV6 \_ CGA \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [**AUTENTICAZIONE \_ KERBEROS IKEEXT0 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [**AUTENTICAZIONE \_ KERBEROS IKEEXT1 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**IKEEXT \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [**STATISTICHE \_ KEYMODULE \_ IKEEXT1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [**IKEEXT \_ NAME \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**IKEEXT \_ NTLM \_ V2 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [**IKEEXT \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [**CRITERI \_ IKEEXT1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [**IKEEXT \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**AUTENTICAZIONE CON CHIAVE \_ \_ PRECONDIVISA IKEEXT0 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [**AUTENTICAZIONE CON \_ CHIAVE \_ PRECONDIVISA IKEEXT1 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [**PROPOSTA \_ IKEEXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**AUTENTICAZIONE RISERVATA \_ \_ IKEEXT0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [**DETTAGLI SA \_ \_ IKEEXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [**DETTAGLI SA \_ \_ IKEEXT1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [**IKEEXT \_ SA \_ DETAILS2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [**IKEEXT \_ SA \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [**STATISTICHE \_ IKEEXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [**STATISTICHE \_ IKEEXT1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [**TRAFFICO \_ IKEEXT0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




