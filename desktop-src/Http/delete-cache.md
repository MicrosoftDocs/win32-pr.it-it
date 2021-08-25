---
title: delete cache
description: Scarica l'intera cache url o elimina le voci in base all'URL specificato.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- http di eliminazione della cache
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c41f2147f0101f312a7fa76796032ec8c821fcea9c08cf89bb3174ddace43d47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870561"
---
# <a name="delete-cache"></a>delete cache

Scarica l'intera cache url o elimina le voci in base all'URL specificato.

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[ url= \]**_stringa_
</dt> <dd>

Obbligatorio. Specifica l'URL completo.

</dd> </dl>

<dl> <dt>

<span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive= \] {sì \| no}**
</dt> <dd>

In caso affermativa, rimuove tutte le voci nell'URL specificato.

</dd> </dl>

## <a name="examples"></a>Esempio

**delete cache url= https://www.contoso.com:80/myresource/ recursive=yes**

 

 




