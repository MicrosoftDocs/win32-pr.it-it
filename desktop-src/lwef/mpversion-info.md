---
title: MPVERSION_INFO (MpClient.h)
description: Informazioni sulla versione per i componenti di Malware Protection Manager.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- MPVERSION_INFO funzionalità dell'ambiente Windows legacy
- PMPVERSION_INFO puntatore alla struttura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50a89b03b8b310416f9b0b496c055f732f4e83859bb7eba50b7891abebc27d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608701"
---
# <a name="mpversion_info-structure"></a>Struttura INFO \_ MPVERSION

Informazioni sulla versione per i componenti di Malware Protection Manager.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Prodotto**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versione del prodotto.

</dd> <dt>

**Servizio**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versione del componente del servizio.

</dd> <dt>

**Filtro FileSystemFilter**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versione del componente filtro del file system.

</dd> <dt>

**Motore**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versione del componente del motore.

</dd> <dt>

**AsSignature**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versione del componente di firma antispyware.

</dd> <dt>

**AvSignature**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versione del componente di firma antivirus.

</dd> <dt>

**NISEngine**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versione del motore NIS.

</dd> <dt>

**NISSignature**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versione del componente della firma NIS.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[**MPCOMPONENT \_ VERSIONE**](mpcomponent-version.md) \[ 4\]**

</dd> <dd>

Campi riservati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**VERSIONE \_ MPCOMPONENT**](mpcomponent-version.md)
</dt> </dl>

 

 





