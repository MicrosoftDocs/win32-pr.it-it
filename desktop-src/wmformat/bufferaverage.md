---
title: BufferAverage
description: L'attributo BufferAverage contiene la dimensione media del buffer necessaria per un flusso di velocità in bit variabile (VBR).
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- BufferAverage Windows Media Format
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce5767ed329fde43cc1022af54d937fc99e0e323
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117104"
---
# <a name="bufferaverage"></a>BufferAverage

L'attributo **BufferAverage** contiene la dimensione media del buffer necessaria per un flusso di velocità in bit variabile (VBR).

## <a name="global-constant"></a>Costante globale

g \_ wszBufferAverage

## <a name="data-type"></a>Tipo di dati

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Commenti

Quando si accede all'interfaccia **IWMHeaderInfo3** dell'oggetto writer, è possibile aggiungere o modificare questo valore. In altri oggetti (editor di metadati, lettore e lettore sincrono), questo valore è di sola lettura.

Il writer scrive automaticamente un valore **BufferAverage** per ogni flusso VBR.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




