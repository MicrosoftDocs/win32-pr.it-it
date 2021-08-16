---
title: Use_DRM
description: "\\_L'attributo Use DRM indica all'oggetto writer di applicare la protezione DRM versione 1 al file corrente."
ms.assetid: ad959e4a-faf7-4b61-9988-6878afcf3a90
keywords:
- Use_DRM windows Media Format
topic_type:
- apiref
api_name:
- Use_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b802a7bef777fab4ed835aa3a1770169deaa6eeea9a7eddeb802fb2e4b0a9dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845302"
---
# <a name="use_drm"></a>Usare \_ DRM

**\_ L'attributo Use DRM** indica all'oggetto writer di applicare la protezione DRM versione 1 al file corrente.

## <a name="global-constant"></a>Costante globale

g \_ wszWMUse \_ DRM

## <a name="data-type"></a>Tipo di dati

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Commenti

Usare [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) per impostare questa proprietà su **TRUE** durante la creazione del contenuto DRM versione 1. Questa proprietà non è accessibile dall'oggetto reader.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




