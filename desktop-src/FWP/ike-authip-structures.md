---
title: Strutture IKE/AuthIP
description: Strutture IKE/AuthIP
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1b5c8f69ec0ac667dee5fc541c84b8e9e66ceb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/27/2020
ms.locfileid: "104398695"
---
# <a name="ikeauthip-structures"></a>Strutture IKE/AuthIP

## <a name="in-this-section"></a>Contenuto della sezione

-   [**\_METHOD0 IKEEXT Authentication \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [**\_METHOD1 IKEEXT Authentication \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [**\_METHOD2 IKEEXT Authentication \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**\_Certificato IKEEXT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_Certificato IKEEXT \_ NAME0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_ \_ CONFIG0 radice certificato \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [**\_AUTHENTICATION0 certificato \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [**\_AUTHENTICATION1 certificato \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [**\_Accodare certificato \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**\_CREDENTIAL0 certificato \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [**\_CREDENTIAL1 certificato \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [**\_CRITERIA0 certificato \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**\_ALGORITHM0 di crittografia IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [**\_STATISTICS0 comuni \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [**\_STATISTICS1 comuni \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [**\_PAIR0 cookie \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [**\_CREDENTIAL0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [**\_CREDENTIAL1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [**\_CREDENTIAL2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [**\_CREDENTIALS0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [**\_CREDENTIALS1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [**\_CREDENTIALS2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [**\_PAIR0 credenziali \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [**\_PAIR1 credenziali \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [**\_Pair2 credenziali \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [**IKEEXT \_ EAP \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [**IKEEXT \_ em \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [**IKEEXT \_ em \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [**IKEEXT \_ em \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**\_ALGORITHM0 integrità \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [**\_STATISTICS0 IKEEXT \_ \_ comuni specifici \_ della versione IP \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [**\_STATISTICS1 IKEEXT \_ \_ comuni specifici \_ della versione IP \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [**\_STATISTICS0 del \_ \_ modulo IKEEXT specifico della versione IP \_ \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [**\_STATISTICS1 del \_ \_ modulo IKEEXT specifico della versione IP \_ \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [**\_ \_ AUTHENTICATION0 CGA IKEEXT per IPv6 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [**\_AUTHENTICATION0 Kerberos \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [**\_AUTHENTICATION1 Kerberos \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**\_STATISTICS0 del modulo \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [**\_STATISTICS1 del modulo \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [**\_Nome IKEEXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**IKEEXT \_ NTLM \_ v2 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [**\_POLICY0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [**\_POLICY1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [**\_POLICY2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**IKEEXT \_ chiave precondivisa \_ \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [**IKEEXT \_ chiave precondivisa \_ \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [**\_PROPOSAL0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**\_AUTHENTICATION0 riservato \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [**IKEEXT \_ sa \_ DETAILS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [**IKEEXT \_ sa \_ Dettagli**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [**IKEEXT \_ sa \_ DETAILS2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [**\_ \_ TEMPLATE0 enum IKEEXT \_ sa**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [**\_STATISTICS0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [**\_STATISTICS1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [**\_TRAFFIC0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




