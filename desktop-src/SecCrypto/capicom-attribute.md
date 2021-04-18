---
description: Definisce il tipo di attributo associato a una firma.
ms.assetid: 94f0dce4-0b32-4c39-ab2e-b01795432acd
title: Enumerazione CAPICOM_ATTRIBUTE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ATTRIBUTE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: b03f91d0737b29b98adeb7e6a56bf9eccd35cc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331782"
---
# <a name="capicom_attribute-enumeration"></a>\_Enumerazione dell'attributo CAPICOM

Il tipo di enumerazione dell' **\_ attributo CAPICOM** definisce il tipo di attributo associato a una [*firma*](../secgloss/d-gly.md).

## <a name="members"></a>Membri



| Membro                                                       | Descrizione                                                                | Valore |
|--------------------------------------------------------------|----------------------------------------------------------------------------|-------|
| **\_tempo di firma dell'attributo autenticato di CAPICOM \_ \_ \_**         | L'attributo contiene la data e l'ora di creazione della firma.<br/> | 0     |
| **\_nome del documento dell'attributo autenticato di CAPICOM \_ \_ \_**        | L'attributo contiene il nome del documento firmato.<br/>         | 1     |
| **\_Descrizione del documento dell'attributo autenticato CAPICOM \_ \_ \_** | L'attributo contiene una descrizione del documento firmato.<br/>    | 2     |



## <a name="remarks"></a>Commenti

Il tipo di enumerazione dell' **\_ attributo CAPICOM** viene usato dalla proprietà [**Attribute.Name**](attribute-name.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
