---
title: DRM_SAPLEVEL (deprecato)
description: Specifica il livello di percorso audio sicuro (SAP) supportato dall'applicazione.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (deprecato) Windows Media Format
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80b43cfcf0c89283237f8ff2d3e4f8612050296d7462f54890c3efa908fa9be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930891"
---
# <a name="drm_saplevel-deprecated"></a>DRM \_ SAPLEVEL (deprecato)

\[**DRM \_ SAPLEVEL** non è più disponibile per l'uso a Windows Vista. Usare invece PUMA (Protected User Mode Audio) nella libreria Media Foundation dati. \]

La **proprietà \_ DRM SAPLEVEL** specifica il livello di percorso audio sicuro (SAP) supportato dall'applicazione.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ SAPLEVEL

## <a name="data-type"></a>Tipo di dati

**STRINGA DI \_ TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di sola scrittura impostata chiamando [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty). Il valore è una rappresentazione di stringa di caratteri wide del livello SAP, ad esempio L"200". I valori attualmente supportati sono 200 e 300.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|--------------------------------|
| Fine del supporto client<br/> | Windows XP<br/>          |
| Fine del supporto server<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 





