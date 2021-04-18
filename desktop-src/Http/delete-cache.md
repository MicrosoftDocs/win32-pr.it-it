---
title: delete cache
description: Scarica l'intera cache URL o Elimina le voci in base all'URL specificato.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- Elimina HTTP cache
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "106299274"
---
# <a name="delete-cache"></a>delete cache

Scarica l'intera cache URL o Elimina le voci in base all'URL specificato.

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[URL = \] * * * stringa*
</dt> <dd>

Obbligatorio. Specifica l'URL completo.

</dd> </dl>

<dl> <dt>

<span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[ricorsivo = \] {Yes \| No}**
</dt> <dd>

In caso affermativo, rimuove tutte le voci nell'URL specificato.

</dd> </dl>

## <a name="examples"></a>Esempio

**Elimina URL cache = https://www.contoso.com:80/myresource/ ricorsivo = Sì**

 

 




