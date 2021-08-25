---
title: show urlacl
description: Elenca gli ELENCHI DACL per l'URL riservato specificato o tutti gli URL riservati.
ms.assetid: 8428583c-b420-408f-974f-670b6809fa3c
keywords:
- show urlacl HTTP
topic_type:
- apiref
api_name:
- show urlacl
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f6e2443f4cdb489f8deb6e8b61d3a808e8a0711ce13c8d71edc57001787617
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900621"
---
# <a name="show-urlacl"></a>show urlacl

Elenca gli ELENCHI DACL per l'URL riservato specificato o tutti gli URL riservati.

``` syntax
show urlacl [url=]string
 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[ url= \]**_stringa_
</dt> <dd>

Specifica l'URL completo. Se non specificato, implica tutti gli URL.

</dd> </dl>

## <a name="examples"></a>Esempio

**show urlacl url=https://+:80/MyUrl**

**show urlacl url=https://www.contoso.com:80/MyUrl**

 

 




