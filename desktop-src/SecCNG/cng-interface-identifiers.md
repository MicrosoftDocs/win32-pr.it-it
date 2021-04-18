---
description: Gli identificatori seguenti vengono utilizzati per identificare un'interfaccia di crittografia CNG.
ms.assetid: 509c89ff-0c73-4e57-9c39-400522f2086e
title: Identificatori di interfaccia CNG (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f75de82e198e0471b48175a080012b9b40eed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305850"
---
# <a name="cng-interface-identifiers"></a>Identificatori di interfaccia CNG

Gli identificatori seguenti vengono utilizzati per identificare un'interfaccia di crittografia CNG. In CNG, un'interfaccia identifica il tipo di comportamento crittografico supportato da un provider. Ad esempio, un provider può essere un generatore di numeri casuali o un provider di hash.



| Costante/valore                                                                                                                                                                                                                                                                                             | Descrizione                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_CIPHER_INTERFACE"></span><span id="bcrypt_cipher_interface"></span><dl> <dt>**BCRYPT \_ \_Interfaccia di crittografia**</dt> <dt>0x00000001</dt> </dl>                                               | Interfaccia di crittografia simmetrica.<br/>                                                                                                                                        |
| <span id="BCRYPT_HASH_INTERFACE"></span><span id="bcrypt_hash_interface"></span><dl> <dt>**BCRYPT \_ \_Interfaccia hash**</dt> <dt>0x00000002</dt> </dl>                                                     | Interfaccia hash.<br/>                                                                                                                                                    |
| <span id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></span><span id="bcrypt_asymmetric_encryption_interface"></span><dl> <dt>**BCRYPT \_ \_ \_ Interfaccia di crittografia asimmetrica**</dt> <dt>0x00000003</dt> </dl> | Interfaccia di crittografia asimmetrica.<br/>                                                                                                                                   |
| <span id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></span><span id="bcrypt_secret_agreement_interface"></span><dl> <dt>**BCRYPT \_ \_ \_ Interfaccia del contratto di segreto**</dt> <dt>0x00000004</dt> </dl>                | Interfaccia dell'accordo di segreto.<br/>                                                                                                                                        |
| <span id="BCRYPT_SIGNATURE_INTERFACE"></span><span id="bcrypt_signature_interface"></span><dl> <dt>**BCRYPT \_ \_Interfaccia di firma**</dt> <dt>0x00000005</dt> </dl>                                      | Interfaccia della firma.<br/>                                                                                                                                               |
| <span id="BCRYPT_RNG_INTERFACE"></span><span id="bcrypt_rng_interface"></span><dl> <dt>**BCRYPT \_ \_Interfaccia RNG**</dt> <dt>0x00000006</dt> </dl>                                                        | Interfaccia del generatore di numeri casuali.<br/>                                                                                                                                 |
| <span id="NCRYPT_KEY_STORAGE_INTERFACE"></span><span id="ncrypt_key_storage_interface"></span><dl> <dt>**NCRYPT \_ \_ \_ Interfaccia di archiviazione chiavi**</dt> <dt>0x00010001</dt> </dl>                               | Interfaccia di archiviazione delle chiavi.<br/>                                                                                                                                             |
| <span id="NCRYPT_SCHANNEL_INTERFACE"></span><span id="ncrypt_schannel_interface"></span><dl> <dt>**NCRYPT \_ \_Interfaccia Schannel**</dt> <dt>0x00010002</dt> </dl>                                         | Interfaccia della firma Schannel.<br/>                                                                                                                                      |
| <span id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></span><span id="ncrypt_schannel_signature_interface"></span><dl> <dt>**NCRYPT \_ \_ \_ Interfaccia di firma Schannel**</dt> <dt>0x00010003</dt> </dl>          | Interfaccia del pacchetto di crittografia Schannel.<br/> **Windows server 2008, Windows Vista, Windows server 2003, Windows XP e windows 2000:** Questo valore non è supportato.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Bcrypt. h; </dt> <dt>Ncrypt. h</dt> </dl> |



 

 




