---
title: Is_Protected
description: L'attributo Is Protected è un attributo a livello di file che specifica se il contenuto del file è \_ stato protetto tramite DRM (Digital Rights Management).
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected windows Media Format
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0759dfc781409a1331403c3b02c2645f6ad843925584eab2a55f31a0c8d31af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847418"
---
# <a name="is_protected"></a>È \_ protetto

**\_ L'attributo Is Protected** è un attributo a livello di file che specifica se il contenuto del file è stato protetto tramite DRM (Digital Rights Management).

## <a name="global-constant"></a>Costante globale

g \_ wszWMProtected

## <a name="data-type"></a>Tipo di dati

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato. Il recupero di questa proprietà fornisce le stesse informazioni della chiamata [**a WMIsContentProtected.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene usato per un singolo flusso, verrà considerato come metadati personalizzati e non trasmetterà il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




