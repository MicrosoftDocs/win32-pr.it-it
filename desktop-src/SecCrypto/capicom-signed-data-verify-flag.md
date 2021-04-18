---
description: Indica cosa viene verificato quando viene verificata una firma digitale.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: Enumerazione CAPICOM_SIGNED_DATA_VERIFY_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bc8db48ee067e8d12bffa9dbff433384058013b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331053"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a>\_Enumerazione del flag di \_ Verifica dei dati firmati capicol \_ \_

L'enumerazione del **flag CApicol \_ signed \_ data \_ Verify \_** indica cosa viene verificato quando viene verificata una [*firma digitale*](../secgloss/d-gly.md) .

## <a name="members"></a>Membri



| Membro                                           | Descrizione                                                                                                 | Valore |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ verificare solo la \_ firma \_**             | Viene controllata solo la firma.<br/>                                                                   | 0     |
| **\_verificare la \_ firma e il \_ \_ certificato di CAPICOM** | Vengono controllati sia la firma che la validità del certificato utilizzato per creare la firma.<br/> | 1     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
