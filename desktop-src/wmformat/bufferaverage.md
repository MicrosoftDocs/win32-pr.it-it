---
title: BufferAverage
description: L'attributo BufferAverage contiene le dimensioni medie del buffer necessarie per un flusso VBR (Variable Bit Rate).
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- BufferAverage windows Media Format
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd839bff96f5ba327e585f8608bd4612fc047d354c24fee972e507ea5ca681f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656121"
---
# <a name="bufferaverage"></a>BufferAverage

**L'attributo BufferAverage** contiene le dimensioni medie del buffer necessarie per un flusso VBR (Variable Bit Rate).

## <a name="global-constant"></a>Costante globale

g \_ wszBufferAverage

## <a name="data-type"></a>Tipo di dati

**DWORD \_ DI \_ TIPO WMT**

## <a name="remarks"></a>Commenti

Quando si accede **all'interfaccia IWMHeaderInfo3** dell'oggetto writer, è possibile aggiungere o modificare questo valore. In altri oggetti (editor di metadati, lettore e lettore sincrono), questo valore è di sola lettura.

Il writer scrive automaticamente un **valore BufferAverage** per ogni flusso VBR.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




