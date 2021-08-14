---
description: Gli identificatori seguenti vengono usati per identificare un'interfaccia crittografica CNG.
ms.assetid: 509c89ff-0c73-4e57-9c39-400522f2086e
title: Identificatori di interfaccia CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ebadf561df916eedde1175a39911da55628b113022378cee9e74b61d021792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908272"
---
# <a name="cng-interface-identifiers"></a>Identificatori di interfaccia CNG

Gli identificatori seguenti vengono usati per identificare un'interfaccia crittografica CNG. In CNG un'interfaccia identifica il tipo di comportamento crittografico supportato da un provider. Ad esempio, un provider può essere un generatore di numeri casuali o un provider di hash.



| Costante/valore                                                                                                                                                                                                                                                                                             | Descrizione                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_CIPHER_INTERFACE"></span><span id="bcrypt_cipher_interface"></span><dl> <dt>**BCRYPT \_ INTERFACCIA \_ CIPHER**</dt> <dt>0x00000001</dt> </dl>                                               | Interfaccia di crittografia simmetrica.<br/>                                                                                                                                        |
| <span id="BCRYPT_HASH_INTERFACE"></span><span id="bcrypt_hash_interface"></span><dl> <dt>**BCRYPT \_ INTERFACCIA \_ HASH**</dt> <dt>0x00000002</dt> </dl>                                                     | Interfaccia hash.<br/>                                                                                                                                                    |
| <span id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></span><span id="bcrypt_asymmetric_encryption_interface"></span><dl> <dt>**BCRYPT \_ INTERFACCIA \_ DI \_ CRITTOGRAFIA ASIMMETRICA**</dt> <dt>0X00000003</dt> </dl> | Interfaccia di crittografia asimmetrica.<br/>                                                                                                                                   |
| <span id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></span><span id="bcrypt_secret_agreement_interface"></span><dl> <dt>**BCRYPT \_ INTERFACCIA \_ \_ DELL'ACCORDO**</dt> <dt>SEGRETO 0x00000004</dt> </dl>                | Interfaccia dell'accordo segreto.<br/>                                                                                                                                        |
| <span id="BCRYPT_SIGNATURE_INTERFACE"></span><span id="bcrypt_signature_interface"></span><dl> <dt>**BCRYPT \_ INTERFACCIA \_ DI**</dt> <dt>FIRMA 0x00000005</dt> </dl>                                      | Interfaccia della firma.<br/>                                                                                                                                               |
| <span id="BCRYPT_RNG_INTERFACE"></span><span id="bcrypt_rng_interface"></span><dl> <dt>**BCRYPT \_ Interfaccia \_ RNG**</dt> <dt>0x00000006</dt> </dl>                                                        | Interfaccia del generatore di numeri casuali.<br/>                                                                                                                                 |
| <span id="NCRYPT_KEY_STORAGE_INTERFACE"></span><span id="ncrypt_key_storage_interface"></span><dl> <dt>**NCRYPT \_ INTERFACCIA \_ DI \_ ARCHIVIAZIONE DELLE**</dt> CHIAVI <dt>0x00010001</dt> </dl>                               | Interfaccia di archiviazione delle chiavi.<br/>                                                                                                                                             |
| <span id="NCRYPT_SCHANNEL_INTERFACE"></span><span id="ncrypt_schannel_interface"></span><dl> <dt>**NCRYPT \_ Interfaccia \_ SCHANNEL**</dt> <dt>0x00010002</dt> </dl>                                         | Interfaccia di firma Schannel.<br/>                                                                                                                                      |
| <span id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></span><span id="ncrypt_schannel_signature_interface"></span><dl> <dt>**NCRYPT \_ INTERFACCIA DI \_ FIRMA \_ SCHANNEL**</dt> <dt>0x00010003</dt> </dl>          | Interfaccia della suite di crittografia Schannel.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP e Windows 2000:** Questo valore non è supportato.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Bcrypt.h; </dt> <dt>Ncrypt.h</dt> </dl> |



 

 




