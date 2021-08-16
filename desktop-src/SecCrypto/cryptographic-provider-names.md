---
description: Usato con le funzioni CryptAcquireContext e CryptSetProvider.
ms.assetid: 97e9a708-83b5-48b3-9d16-f7b54367dc4e
title: Nomi dei provider del servizio di crittografia (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c9b41aaeacb0b03df4b2fc0c608ae1f98e59ac0a581a395eb9904d0ec8e235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768687"
---
# <a name="cryptographic-provider-names"></a>Nomi dei provider del servizio di crittografia

I nomi [*dei provider del servizio di*](../secgloss/c-gly.md) crittografia (CSP) seguenti sono definiti in Wincrypt.h. Queste costanti vengono usate con le [**funzioni CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) e [**CryptSetProvider.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera)



| Costante/valore                                                                                                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MS_DEF_DH_SCHANNEL_PROV"></span><span id="ms_def_dh_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ DH \_ SCHANNEL \_ PROV**</dt> <dt>"Microsoft DH Schannel Cryptographic Provider"</dt> </dl>      | Microsoft [DSS e Diffie-Hellman/Schannel Cryptographic Provider](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md).<br/>                                         |
| <span id="MS_DEF_DSS_DH_PROV"></span><span id="ms_def_dss_dh_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_ DH \_ PROV**</dt> <dt>"Microsoft Base DSS and Diffie-Hellman Cryptographic Provider"</dt> </dl>     | Microsoft [Base DSS e Diffie-Hellman Cryptographic Provider](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                                 |
| <span id="MS_DEF_DSS_PROV"></span><span id="ms_def_dss_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_ PROV**</dt> <dt>"Microsoft Base DSS Cryptographic Provider"</dt> </dl>                                  | Provider [del servizio di crittografia Microsoft DSS.](microsoft-dss-cryptographic-provider.md)<br/>                                                                                                 |
| <span id="MS_DEF_PROV"></span><span id="ms_def_prov"></span><dl> <dt>**MS \_ DEF \_ PROV**</dt> <dt>"Microsoft Base Cryptographic Provider v1.0"</dt> </dl>                                              | Provider [del servizio di crittografia di base Microsoft.](microsoft-base-cryptographic-provider.md)<br/>                                                                                               |
| <span id="MS_DEF_RSA_SCHANNEL_PROV"></span><span id="ms_def_rsa_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ SCHANNEL \_ PROV**</dt> <dt>"Microsoft RSA Schannel Cryptographic Provider"</dt> </dl>  | Provider [del servizio di crittografia Microsoft RSA/Schannel.](microsoft-rsa-schannel-cryptographic-provider.md)<br/>                                                                               |
| <span id="MS_DEF_RSA_SIG_PROV"></span><span id="ms_def_rsa_sig_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ SIG \_ PROV**</dt> <dt>"Microsoft RSA Signature Cryptographic Provider"</dt> </dl>                | Microsoft [RSA Signature Cryptographic Provider](microsoft-rsa-signature-cryptographic-provider.md) non è supportato.<br/>                                                            |
| <span id="MS_ENH_DSS_DH_PROV"></span><span id="ms_enh_dss_dh_prov"></span><dl> <dt>**MS \_ ENH \_ DSS \_ DH \_ PROV**</dt> <dt>"Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider"</dt> </dl> | Microsoft [Enhanced DSS e Diffie-Hellman Cryptographic Provider](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                         |
| <span id="MS_ENH_RSA_AES_PROV"></span><span id="ms_enh_rsa_aes_prov"></span><dl> <dt>**MS \_ ENH \_ RSA \_ AES \_ PROV**</dt> <dt>"Microsoft Enhanced RSA and AES Cryptographic Provider"</dt> </dl>         | Provider [del servizio di crittografia Microsoft AES.](microsoft-aes-cryptographic-provider.md)<br/> **Windows XP: **"Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype)"<br/> |
| <span id="MS_ENHANCED_PROV"></span><span id="ms_enhanced_prov"></span><dl> <dt>**MS \_ ENHANCED \_ PROV**</dt> <dt>"Microsoft Enhanced Cryptographic Provider v1.0"</dt> </dl>                           | Microsoft [Enhanced Cryptographic Provider.](microsoft-enhanced-cryptographic-provider.md)<br/>                                                                                       |
| <span id="MS_SCARD_PROV"></span><span id="ms_scard_prov"></span><dl> <dt>**MS \_ SCARD \_ PROV**</dt> <dt>"Microsoft Base Smart Card Crypto Provider"</dt> </dl>                                         | Provider [del servizio di crittografia della smart card microsoft di base.](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)<br/>                                                    |
| <span id="MS_STRONG_PROV"></span><span id="ms_strong_prov"></span><dl> <dt>**MS \_ STRONG \_ PROV**</dt> <dt>"Microsoft Strong Cryptographic Provider"</dt> </dl>                                        | Microsoft [Strong Cryptographic Provider.](microsoft-strong-cryptographic-provider.md)<br/>                                                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
