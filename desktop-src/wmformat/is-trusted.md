---
title: Is_Trusted
description: L'attributo Is Trusted è un attributo a livello di file che specifica se l'URL di acquisizione della \_ licenza nel file è attendibile.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted windows Media Format
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e255c91c5779eb44da8e587601fdfd9264f10888a46a7f216ae2af619ff9f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198277"
---
# <a name="is_trusted"></a>È \_ attendibile

**L'attributo Is \_ Trusted** è un attributo a livello di file che specifica se l'URL di acquisizione della licenza nel file è attendibile.

## <a name="global-constant"></a>Costante globale

g \_ wszWMTrusted

## <a name="data-type"></a>Tipo di dati

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Prima di passare a un URL di acquisizione della licenza contenuto in un file protetto da DRM, un'applicazione deve prima verificare che questa proprietà sia true. Se è false, l'applicazione deve notificare all'utente che l'URL è stato probabilmente manomesso.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene usato per un singolo flusso, verrà considerato come metadati personalizzati e non trasmetterà il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




