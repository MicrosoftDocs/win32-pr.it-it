---
title: DRM_SAPLEVEL (deprecato)
description: Specifica il livello SAP (Secure Audio Path) supportato dall'applicazione.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (obsoleto) formato Windows Media
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43711c6c394761f599271809419a46311265d8b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324057"
---
# <a name="drm_saplevel-deprecated"></a>DRM \_ SAPLEVEL (deprecato)

\[**DRM \_ SAPLEVEL** non è più disponibile per l'utilizzo in Windows Vista. In alternativa, usare l'audio della modalità utente protetto (PUMA) nella libreria Media Foundation. \]

La proprietà **DRM \_ SAPLEVEL** specifica il livello SAP (Secure Audio Path) supportato dall'applicazione.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ SAPLEVEL

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di sola scrittura impostata chiamando [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty). Il valore è una rappresentazione di stringa a caratteri wide del livello SAP, ad esempio L "200". I valori correnti supportati sono 200 e 300.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|--------------------------------|
| Fine del supporto client<br/> | Windows XP<br/>          |
| Fine del supporto server<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 





