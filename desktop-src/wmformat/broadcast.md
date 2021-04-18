---
title: Trasmissione
description: L'attributo broadcast è un attributo a livello di file che indica se il contenuto può essere trasmesso. Si presuppone che qualsiasi contenuto per cui non è stato assegnato alcun copyright possa essere trasmesso legalmente.
ms.assetid: da2adf16-a9b5-4678-896e-2be8f5ca27e4
keywords:
- Trasmettere il formato Windows Media
topic_type:
- apiref
api_name:
- Broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbf9e7d94682f8dbf08850f87954a934fd909afe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299235"
---
# <a name="broadcast"></a>Trasmissione

L'attributo **broadcast** è un attributo a livello di file che indica se il contenuto può essere trasmesso. Si presuppone che qualsiasi contenuto per cui non è stato assegnato alcun copyright possa essere trasmesso legalmente.

## <a name="global-constant"></a>Costante globale

g \_ wszWMBroadcast

## <a name="data-type"></a>Tipo di dati

**\_tipo WMT \_ bool**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




