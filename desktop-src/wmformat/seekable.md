---
title: Ricercabile
description: L'attributo seekable è un attributo a livello di file che specifica se un'applicazione può cercare punti all'interno del contenuto.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Formato Windows Media ricercabile
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104336626"
---
# <a name="seekable"></a>Ricercabile

L'attributo **seekable** è un attributo a livello di file che specifica se un'applicazione può cercare punti all'interno del contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMSeekable

## <a name="data-type"></a>Tipo di dati

**\_tipo WMT \_ bool**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.

Il valore di questo attributo per un file può variare a seconda dell'oggetto che espone l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) o [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) utilizzata per recuperarla. Ciò è dovuto al fatto che gli oggetti Reader (sincroni e asincroni) eseguono un controllo più approfondito rispetto all'oggetto dell'editor di metadati, per verificare se è possibile cercare un punto in un file. Il valore dell'attributo **cercabile** restituito da un oggetto Reader è più accurato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




