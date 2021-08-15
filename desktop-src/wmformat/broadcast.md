---
title: Trasmissione
description: L'attributo Broadcast è un attributo a livello di file che indica se il contenuto può essere trasmesso. Si presuppone che qualsiasi contenuto per cui non è stato assegnato alcun copyright possa essere trasmesso legalmente.
ms.assetid: da2adf16-a9b5-4678-896e-2be8f5ca27e4
keywords:
- Broadcast windows Media Format
topic_type:
- apiref
api_name:
- Broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b233a74deb71efe041ab5ad2f5e4ffa421d048a70c5b97e8f7ac38499bd18df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086166"
---
# <a name="broadcast"></a>Trasmissione

**L'attributo Broadcast** è un attributo a livello di file che indica se il contenuto può essere trasmesso. Si presuppone che qualsiasi contenuto per cui non è stato assegnato alcun copyright possa essere trasmesso legalmente.

## <a name="global-constant"></a>Costante globale

g \_ wszWMBroadcast

## <a name="data-type"></a>Tipo di dati

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene usato per un singolo flusso, verrà considerato come metadati personalizzati e non trasmetterà il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




