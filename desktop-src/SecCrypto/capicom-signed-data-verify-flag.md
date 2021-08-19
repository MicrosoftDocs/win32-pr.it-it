---
description: Indica ciò che viene controllato quando viene verificata una firma digitale.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: CAPICOM_SIGNED_DATA_VERIFY_FLAG di controllo (Capicom.h)
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
ms.openlocfilehash: 8f087a9a28d06e63bc19d75974bccba05da4c77658f81401fd994a7eadb9726a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772085"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a>Enumerazione CAPICOM \_ SIGNED \_ DATA VERIFY \_ \_ FLAG

**L'enumerazione CAPICOM \_ SIGNED DATA VERIFY \_ \_ \_ FLAG** indica ciò che viene controllato quando [*viene verificata*](../secgloss/d-gly.md) una firma digitale.

## <a name="members"></a>Membri



| Membro                                           | Descrizione                                                                                                 | Valore |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| **VERIFICA SOLO \_ \_ FIRMA \_ CAPICOM**             | Viene verificata solo la firma.<br/>                                                                   | 0     |
| **VERIFICA FIRMA \_ \_ E \_ \_ CERTIFICATO CAPICOM** | Vengono controllati sia la firma che la validità del certificato usato per creare la firma.<br/> | 1     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
