---
title: MPRESOURCE_INFO struttura (MpClient.h)
description: Struttura delle informazioni sulle risorse.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- MPRESOURCE_INFO struttura Legacy Windows Environment Features
- PMPRESOURCE_INFO puntatore alla struttura Legacy Windows Environment Features
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
ms.openlocfilehash: c399beceba4551ba3269e86f5f3c30c6967f31b4dbc5f303225e8cbfc1667df4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747424"
---
# <a name="mpresource_info-structure"></a>Struttura MPRESOURCE \_ INFO

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

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Identificatore dello schema di risorse, ad esempio "file" o "dir".

</dd> <dt>

**Percorso**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Percorso assoluto della risorsa, in base a **Schema**.

</dd> <dt>

**Classe**
</dt> <dd>

Tipo: **CLASSE \_ MPRESOURCE**

</dd> <dd>

Questo campo viene impostato quando la risorsa viene identificata come parte della minaccia. Specifica la classe di risorse, principalmente concreta e latente. Può essere una combinazione di questi valori possibili:



| Valore                                                                                                                                                                                                                                                                        | Significato                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <dt>**MP \_ CLASSE \_ DI RISORSE \_ UNKNOWN**</dt> <dt>0x0000</dt> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <dt>**MP \_ CLASSE \_ DI RISORSE \_ CONCRETE**</dt> <dt>0x0001</dt> </dl>           | Si escludono a **vicenda con MP RESOURCE CLASS \_ \_ \_ LATENT**.<br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <dt>**MP \_ CLASSE \_ \_ DI RISORSE LATENT**</dt> <dt>0x0002</dt> </dl>                 | Si escludono a vicenda **con MP RESOURCE CLASS \_ \_ \_ CONCRETE**.<br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <dt>**MP \_ FILE DI ESEMPIO DELLA CLASSE \_ \_ \_ DI**</dt> <dt>RISORSE 0x0004</dt> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <dt>**MP \_ CLASSE \_ RESOURCE \_ SHARED**</dt> <dt>0x0100</dt> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





