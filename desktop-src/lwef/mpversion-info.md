---
title: Struttura MPVERSION_INFO (MpClient. h)
description: Informazioni sulla versione per i componenti di malware Protection Manager.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- Struttura MPVERSION_INFO le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPVERSION_INFO
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
ms.openlocfilehash: f30153c427b880600a3d8aeb3c411a8679cd64b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341043"
---
# <a name="mpversion_info-structure"></a>Struttura delle informazioni di MPVERSION \_

Informazioni sulla versione per i componenti di malware Protection Manager.

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

Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Versione del prodotto.

</dd> <dt>

**Servizio**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Versione del componente del servizio.

</dd> <dt>

**FileSystemFilter**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Versione del componente filtro del file System.

</dd> <dt>

**Motore**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Versione del componente del motore.

</dd> <dt>

**ASSignature**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Versione del componente della firma antispyware.

</dd> <dt>

**AVSignature**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Versione del componente della firma antivirus.

</dd> <dt>

**NISEngine**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Versione del motore NIS.

</dd> <dt>

**NISSignature**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Versione del componente firma della firma NIS.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[**MPCOMPONENT \_ versione**](mpcomponent-version.md) \[ 4\]**

</dd> <dd>

Campi riservati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**versione di MPCOMPONENT \_**](mpcomponent-version.md)
</dt> </dl>

 

 





