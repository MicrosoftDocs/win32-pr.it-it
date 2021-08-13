---
title: Ricercabile
description: L'attributo Seekable è un attributo a livello di file che specifica se un'applicazione può cercare punti all'interno del contenuto.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Formato windows Media ricercabile
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a254d06b36230bb6920f2f13d646edc5f1cdac75efe15864e0c84ba847cf50f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699987"
---
# <a name="seekable"></a>Ricercabile

**L'attributo Seekable** è un attributo a livello di file che specifica se un'applicazione può cercare punti all'interno del contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMSeekable

## <a name="data-type"></a>Tipo di dati

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene usato per un singolo flusso, verrà trattato come metadati personalizzati e non trasmetterà il significato normale agli oggetti di Windows Media Format SDK.

Il valore di questo attributo per un file può variare a seconda dell'oggetto che espone l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) o [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) usata per recuperarlo. Ciò è dovuto al fatto che gli oggetti lettore (sincroni e asincroni) eseguono un controllo più approfondito rispetto all'oggetto editor di metadati, per verificare se è possibile cercare un punto in un file. Il **valore dell'attributo Seekable** restituito da un oggetto reader è più accurato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




