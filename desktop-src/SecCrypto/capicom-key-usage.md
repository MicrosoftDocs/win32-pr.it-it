---
description: L'enumerazione CAPICOM \_ KEY USAGE definisce le modalità di utilizzo di una \_ chiave. Introdotto in CAPICOM 2.0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: CAPICOM_KEY_USAGE di controllo (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bb477ee12b33c3d32fd2c48a56831dc2f56244b1e8a564cd2d0482e6e4a5d5bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772426"
---
# <a name="capicom_key_usage-enumeration"></a>Enumerazione CAPICOM \_ KEY \_ USAGE

**L'enumerazione CAPICOM \_ KEY \_ USAGE** definisce le modalità di utilizzo di una chiave. Introdotto in CAPICOM 2.0.

## <a name="members"></a>Membri



| Membro                                      | Descrizione                                                                                                                      | Valore      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| **UTILIZZO DELLA \_ CHIAVE \_ DI FIRMA DIGITALE \_ CAPICOM \_** | La chiave può essere usata per creare una firma digitale.<br/>                                                                    | 0x00000080 |
| **UTILIZZO DELLA CHIAVE \_ DI NON \_ \_ RIPUDIO \_ CAPICOM**   | La chiave può essere usata [*per il non ripudio.*](../secgloss/n-gly.md)<br/> | 0x00000040 |
| **UTILIZZO DELLA \_ CHIAVE \_ DI CRITTOGRAFIA CAPICOM \_ \_**  | La chiave può essere usata per crittografare una chiave.<br/>                                                                                 | 0x00000020 |
| **UTILIZZO DELLA \_ CHIAVE \_ DI CRITTOGRAFIA DEI \_ DATI CAPICOM \_** | La chiave può essere usata per crittografare i dati.<br/>                                                                                  | 0x00000010 |
| **CAPICOM \_ KEY \_ AGREEMENT \_ KEY \_ USAGE**     | La chiave può essere usata per il contratto di chiave.<br/>                                                                                | 0x00000008 |
| **UTILIZZO DELLA \_ CHIAVE DI FIRMA DEL CERTIFICATO DELLA \_ \_ \_ CHIAVE \_ CAPICOM**    | La chiave può essere usata per la firma del certificato della chiave. Questo valore equivale a CAPICOM \_ OFFLINE \_ CRL \_ SIGN KEY \_ \_ USAGE.<br/> | 0x00000004 |
| **UTILIZZO DELLA CHIAVE \_ \_ DI FIRMA CRL OFFLINE \_ \_ CAPICOM \_** | La chiave può essere usata per la firma del certificato della chiave. Questo valore equivale a CAPICOM \_ KEY \_ CERT \_ SIGN KEY \_ \_ USAGE.<br/>    | 0x00000002 |
| **UTILIZZO DELLA \_ CHIAVE DI FIRMA CRL CAPICOM \_ \_ \_**          | La chiave può essere usata per la firma.<br/>                                                                                      | 0x00000002 |
| **CAPICOM \_ ENCIPHER \_ ONLY \_ KEY \_ USAGE**     | La chiave può essere usata solo per crittografare.<br/>                                                                                  | 0x00000001 |
| **CAPICOM \_ DECIPHER \_ ONLY \_ KEY \_ USAGE**     | La chiave può essere usata solo per decrittografare.<br/>                                                                                  | 0x00008000 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
