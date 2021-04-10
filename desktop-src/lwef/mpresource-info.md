---
title: Struttura MPRESOURCE_INFO (MpClient. h)
description: Struttura delle informazioni sulle risorse.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- Struttura MPRESOURCE_INFO le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPRESOURCE_INFO
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964488"
---
# <a name="mpresource_info-structure"></a>Struttura delle informazioni di MPRESOURCE \_

Struttura delle informazioni sulle risorse.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Schema**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Identificatore dello schema di risorsa, ad esempio "file" o "dir".

</dd> <dt>

**Percorso**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Percorso assoluto della risorsa, in base allo **schema**.

</dd> <dt>

**Classe**
</dt> <dd>

Tipo: **\_ classe MPRESOURCE**

</dd> <dd>

Questo campo viene impostato quando la risorsa viene identificata come parte della minaccia. Specifica la classe di risorse, principalmente concreta rispetto alla latenza. Può essere una combinazione di questi valori possibili:



| Valore                                                                                                                                                                                                                                                                        | Significato                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <dt>**MP \_ Classe di risorse \_ \_ sconosciuta**</dt> <dt>0x0000</dt> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <dt>**MP \_ 0x0001 \_ \_ concrete della classe di risorse**</dt> <dt></dt> </dl>           | Si escludono a vicenda con la **\_ classe di risorse MP \_ \_ latente**.<br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <dt>**MP \_ Classe di risorse \_ \_ latenza**</dt> <dt>0x0002</dt> </dl>                 | Si escludono a vicenda con la **\_ classe di risorse MP \_ \_ concreta**.<br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <dt>**MP \_ Classe di risorse \_ \_ \_ file di esempio**</dt> <dt>0x0004</dt> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <dt>**MP \_ Classe di risorse \_ \_ Shared**</dt> <dt>0x0100</dt> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





