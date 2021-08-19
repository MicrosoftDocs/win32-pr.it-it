---
title: CurrentBitrate
description: L'attributo CurrentBitrate contiene la velocità in bit totale corrente dei flussi attivi nel file.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- Formato multimediale Windows CurrentBitrate
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 028207ee152acac289da6608c682f5fc14a4fde69603a2aae05b841d0cfb46ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027949"
---
# <a name="currentbitrate"></a>CurrentBitrate

L'attributo CurrentBitrate contiene la velocità in bit totale corrente dei flussi attivi nel file.

## <a name="global-constant"></a>Costante globale

g \_ wszWMCurrentBitrate

## <a name="data-type"></a>Tipo di dati

**DWORD \_ DI \_ TIPO WMT**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Il valore recuperato per **CurrentBitrate** è diverso a seconda dell'oggetto usato. Nel lettore o nell'oggetto lettore sincrono, il valore è la velocità in bit effettiva al momento della chiamata. Nell'oggetto editor dei metadati il valore è la velocità in bit media del file.

La velocità in bit effettiva di un file è uguale alla velocità in bit di tutti i flussi attivi più un sovraccarico. Si tratta del valore visualizzato, ad esempio, quando si riproduce un file con il Windows Media Player.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene usato per un singolo flusso, verrà considerato come metadati personalizzati e non trasmetterà il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




