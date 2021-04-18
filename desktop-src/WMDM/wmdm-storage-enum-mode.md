---
title: Enumerazione WMDM_STORAGE_ENUM_MODE
description: Il \_ \_ \_ tipo di enumerazione WMDM storage enum Mode definisce il modo in cui deve essere enumerato il contenuto nell'archivio. Questa enumerazione viene utilizzata da IWMDMStorage3 SetEnumPreference.
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- Enumerazione WMDM_STORAGE_ENUM_MODE Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d886ade00289e655ae3323a70d01be96a09852b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324759"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a>\_Enumerazione della \_ modalità enum di archiviazione WMDM \_

Il tipo di enumerazione **WMDM \_ storage \_ enum \_ mode** definisce il modo in cui deve essere enumerato il contenuto nell'archivio. Questa enumerazione viene utilizzata da [**IWMDMStorage3:: SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**modalità di enumerazione non \_ \_ elaborata**
</dt> <dd>

Enumera il contenuto nell'archiviazione così come è organizzato nel file system dell'archiviazione.

**\_modalità enum \_ Usa \_ \_ pref dispositivo**

Enumera il contenuto nell'archiviazione in base alla preferenza del dispositivo come indicato dal parametro del dispositivo *UseMetadataViews* .

**\_ \_ viste dei metadati in modalità enum \_**

Enumera il contenuto nell'archivio organizzando il contenuto in base a una visualizzazione dei metadati.

</dd> <dt>

<span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**\_modalità enum \_ Usa \_ \_ pref dispositivo**
</dt> <dd>

Enumera il contenuto nell'archiviazione in base alla preferenza del dispositivo come indicato dal parametro del dispositivo *UseMetadataViews* .

**\_ \_ viste dei metadati in modalità enum \_**

Enumera il contenuto nell'archivio organizzando il contenuto in base a una visualizzazione dei metadati.

</dd> <dt>

<span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**\_ \_ viste dei metadati in modalità enum \_**
</dt> <dd>

Enumera il contenuto nell'archivio organizzando il contenuto in base a una visualizzazione dei metadati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





