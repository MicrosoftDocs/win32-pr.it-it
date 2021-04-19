---
title: CurrentBitrate
description: L'attributo CurrentBitrate contiene la velocità in bit totale corrente dei flussi attivi nel file.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- CurrentBitrate Windows Media Format
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299241"
---
# <a name="currentbitrate"></a>CurrentBitrate

L'attributo CurrentBitrate contiene la velocità in bit totale corrente dei flussi attivi nel file.

## <a name="global-constant"></a>Costante globale

g \_ wszWMCurrentBitrate

## <a name="data-type"></a>Tipo di dati

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Il valore recuperato per **CurrentBitrate** è diverso a seconda dell'oggetto utilizzato. Nell'oggetto Reader o Reader sincrono, il valore è la velocità in bit effettiva al momento della chiamata. Nell'oggetto dell'editor di metadati, il valore corrisponde alla velocità in bit media del file.

La velocità in bit effettiva di un file è uguale alla velocità in bit di tutti i flussi attivi, oltre a un sovraccarico. Questo è il valore, ad esempio, visualizzato quando si riproduce un file con Windows Media Player.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




