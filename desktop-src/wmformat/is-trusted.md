---
title: Is_Trusted
description: L' \_ attributo is trusted è un attributo a livello di file che specifica se l'URL di acquisizione della licenza nel file è attendibile.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted formato Windows Media
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e8dd4fdd638bad0908bb1bbf50135cde5bad6c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103956018"
---
# <a name="is_trusted"></a>\_Attendibile

L'attributo **is \_ Trusted** è un attributo a livello di file che specifica se l'URL di acquisizione della licenza nel file è attendibile.

## <a name="global-constant"></a>Costante globale

g \_ wszWMTrusted

## <a name="data-type"></a>Tipo di dati

**\_tipo WMT \_ bool**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Prima di passare a un URL di acquisizione della licenza contenuto in un file protetto da DRM, un'applicazione deve prima verificare che la proprietà sia true. Se è false, l'applicazione deve notificare all'utente che è possibile che l'URL sia stato alterato.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




