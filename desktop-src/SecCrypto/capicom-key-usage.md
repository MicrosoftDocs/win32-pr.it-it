---
description: L' \_ \_ enumerazione di utilizzo della chiave CAPICOM definisce i modi in cui è possibile utilizzare una chiave. Introdotta in capicol 2,0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: Enumerazione CAPICOM_KEY_USAGE (CAPICOM. h)
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
ms.openlocfilehash: 1d44c7f3ecf35ddeb55dd96e5513261691010990
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327639"
---
# <a name="capicom_key_usage-enumeration"></a>\_Enumerazione utilizzo chiave CApicol \_

L'enumerazione di **\_ \_ utilizzo della chiave CAPICOM** definisce i modi in cui è possibile utilizzare una chiave. Introdotta in capicol 2,0.

## <a name="members"></a>Membri



| Membro                                      | Descrizione                                                                                                                      | Valore      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| **\_ \_ \_ utilizzo chiave firma digitale CAPICOM \_** | La chiave può essere usata per creare una firma digitale.<br/>                                                                    | 0x00000080 |
| **\_utilizzo chiave di non \_ ripudio di \_ CAPICOM \_**   | La chiave può essere utilizzata per il non [*ripudio*](../secgloss/n-gly.md).<br/> | 0x00000040 |
| **\_ \_ utilizzo chiave di crittografia chiave \_ CAPICOM \_**  | La chiave può essere usata per crittografare una chiave.<br/>                                                                                 | 0x00000020 |
| **\_ \_ \_ utilizzo chiave crittografia dati CAPICOM \_** | La chiave può essere usata per crittografare i dati.<br/>                                                                                  | 0x00000010 |
| **utilizzo chiave di capicot Key \_ \_ Agreement \_ \_**     | La chiave può essere usata per il contratto di chiave.<br/>                                                                                | 0x00000008 |
| **\_utilizzo della chiave di \_ firma del certificato chiave \_ \_ CAPICOM \_**    | La chiave può essere usata per la firma del certificato chiave. Questo valore è equivalente all' \_ utilizzo della chiave di \_ firma CRL offline di CAPICOM \_ \_ \_ .<br/> | 0x00000004 |
| **\_ \_ \_ utilizzo chiave di firma CRL \_ offline \_ di CAPICOM** | La chiave può essere usata per la firma del certificato chiave. Questo valore è equivalente all' \_ utilizzo della chiave di firma del certificato chiave CApicol \_ \_ \_ \_ .<br/>    | 0x00000002 |
| **\_ \_ \_ utilizzo chiave del segno di capicol CRL \_**          | La chiave può essere usata per la firma.<br/>                                                                                      | 0x00000002 |
| **CAPICOM \_ \_ solo \_ \_ utilizzo chiavi**     | La chiave può essere utilizzata solo per la crittografia.<br/>                                                                                  | 0x00000001 |
| **CAPICOM \_ decifrare \_ solo \_ \_ utilizzo chiavi**     | La chiave può essere usata solo per la decrittografia.<br/>                                                                                  | 0x00008000 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
