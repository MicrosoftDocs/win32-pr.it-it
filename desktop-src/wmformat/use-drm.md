---
title: Use_DRM
description: L' \_ attributo use DRM indica all'oggetto writer di applicare la protezione DRM versione 1 al file corrente.
ms.assetid: ad959e4a-faf7-4b61-9988-6878afcf3a90
keywords:
- Use_DRM formato Windows Media
topic_type:
- apiref
api_name:
- Use_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fcb010855ac4660792a7c579556001d5d7c4c96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516591"
---
# <a name="use_drm"></a>USA \_ DRM

L'attributo **use \_ DRM** indica all'oggetto writer di applicare la protezione DRM versione 1 al file corrente.

## <a name="global-constant"></a>Costante globale

g \_ wszWMUse \_ DRM

## <a name="data-type"></a>Tipo di dati

**\_tipo WMT \_ bool**

## <a name="remarks"></a>Commenti

Usare [**IWMHeaderInfo:: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) per impostare questa proprietà su **true** quando si crea contenuto DRM versione 1. Questa proprietà non è accessibile dall'oggetto Reader.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




