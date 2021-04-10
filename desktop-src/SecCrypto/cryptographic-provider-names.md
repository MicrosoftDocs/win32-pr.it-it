---
description: Utilizzato con le funzioni CryptAcquireContext e CryptSetProvider.
ms.assetid: 97e9a708-83b5-48b3-9d16-f7b54367dc4e
title: Nomi dei provider del crittografia (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a5cbe497e56144a9948dab96be0c03dd5a99f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966594"
---
# <a name="cryptographic-provider-names"></a>Nomi dei provider di crittografia

I nomi del [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) seguenti sono definiti in WinCrypt. h. Queste costanti vengono usate con le funzioni [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) e [**CryptSetProvider**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera) .



| Costante/valore                                                                                                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MS_DEF_DH_SCHANNEL_PROV"></span><span id="ms_def_dh_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ DH \_ Schannel \_ prova**</dt> <dt>"Microsoft DH SChannel Cryptographic Provider"</dt> </dl>      | Il [provider di crittografia Microsoft DSS e Diffie-Hellman/SChannel](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md).<br/>                                         |
| <span id="MS_DEF_DSS_DH_PROV"></span><span id="ms_def_dss_dh_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_ DH \_ prova**</dt> <dt>"Microsoft Base DSS e Diffie-Hellman provider di crittografia"</dt> </dl>     | Il [provider di crittografia Microsoft Base DSS e Diffie-Hellman](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                                 |
| <span id="MS_DEF_DSS_PROV"></span><span id="ms_def_dss_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_ prova**</dt> <dt>"Microsoft Base DSS Cryptographic Provider"</dt> </dl>                                  | Il [provider di crittografia Microsoft DSS](microsoft-dss-cryptographic-provider.md).<br/>                                                                                                 |
| <span id="MS_DEF_PROV"></span><span id="ms_def_prov"></span><dl> <dt>**MS \_ DEF \_ prova**</dt> <dt>"Microsoft Base Cryptographic Provider v 1.0"</dt> </dl>                                              | [Provider di crittografia di base Microsoft](microsoft-base-cryptographic-provider.md).<br/>                                                                                               |
| <span id="MS_DEF_RSA_SCHANNEL_PROV"></span><span id="ms_def_rsa_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ Schannel \_ prova**</dt> <dt>"Microsoft RSA SChannel Cryptographic Provider"</dt> </dl>  | Il [provider di crittografia Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md).<br/>                                                                               |
| <span id="MS_DEF_RSA_SIG_PROV"></span><span id="ms_def_rsa_sig_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ sig \_ prova**</dt> <dt>"Microsoft RSA Signature Cryptographic Provider"</dt> </dl>                | Il [provider di crittografia Microsoft RSA Signature](microsoft-rsa-signature-cryptographic-provider.md) non è supportato.<br/>                                                            |
| <span id="MS_ENH_DSS_DH_PROV"></span><span id="ms_enh_dss_dh_prov"></span><dl> <dt>**MS \_ ENH \_ DSS \_ DH \_ prova**</dt> <dt>"Microsoft Enhanced DSS e Diffie-Hellman provider di crittografia"</dt> </dl> | [Microsoft Enhanced DSS e Diffie-Hellman provider di crittografia](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                         |
| <span id="MS_ENH_RSA_AES_PROV"></span><span id="ms_enh_rsa_aes_prov"></span><dl> <dt>**MS \_ ENH \_ RSA \_ AES \_ prova**</dt> <dt>"Microsoft Enhanced RSA and AES Cryptographic Provider"</dt> </dl>         | [Provider di crittografia AES Microsoft](microsoft-aes-cryptographic-provider.md).<br/> * * Windows XP: * * "Microsoft Enhanced RSA and AES Cryptographic Provider (prototipo)"<br/> |
| <span id="MS_ENHANCED_PROV"></span><span id="ms_enhanced_prov"></span><dl> <dt>**MS \_ AVANZATA \_ prova**</dt> <dt>"Microsoft Enhanced Cryptographic Provider v 1.0"</dt> </dl>                           | [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md).<br/>                                                                                       |
| <span id="MS_SCARD_PROV"></span><span id="ms_scard_prov"></span><dl> <dt>**MS \_ SPAVENTATO \_ prova**</dt> <dt>"provider di crittografia Smart Card Microsoft base"</dt> </dl>                                         | [Provider del servizio di crittografia per Smart Card di Microsoft base](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider).<br/>                                                    |
| <span id="MS_STRONG_PROV"></span><span id="ms_strong_prov"></span><dl> <dt>**MS \_ \_Prova forte**</dt> <dt>"provider di crittografia Microsoft Strong"</dt> </dl>                                        | [Microsoft Strong Cryptographic Provider](microsoft-strong-cryptographic-provider.md).<br/>                                                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
