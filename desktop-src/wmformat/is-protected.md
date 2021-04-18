---
title: Is_Protected
description: L' \_ attributo is protected è un attributo a livello di file che specifica se il contenuto del file è stato protetto mediante Digital Rights Management (DRM).
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected formato Windows Media
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299380"
---
# <a name="is_protected"></a>\_Protetto

L'attributo **is \_ protected** è un attributo a livello di file che specifica se il contenuto del file è stato protetto mediante Digital Rights Management (DRM).

## <a name="global-constant"></a>Costante globale

g \_ wszWMProtected

## <a name="data-type"></a>Tipo di dati

**\_tipo WMT \_ bool**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato. Il recupero di questa proprietà fornisce le stesse informazioni della chiamata a [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




