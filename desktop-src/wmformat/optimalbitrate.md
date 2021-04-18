---
title: OptimalBitrate
description: L'attributo OptimalBitrate contiene la velocità in bit in cui è possibile riprodurre il file.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- OptimalBitrate Windows Media Format
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299197"
---
# <a name="optimalbitrate"></a>OptimalBitrate

L'attributo **OptimalBitrate** contiene la velocità in bit in cui è possibile riprodurre il file.

## <a name="global-constant"></a>Costante globale

g \_ wszWMOptimalBitrate

## <a name="data-type"></a>Tipo di dati

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Per i file che contengono flussi di velocità in bit variabili (VBR), questo valore è la velocità in bit massima per i flussi nel file. Per i file senza VBR, questo valore è uguale a quello della [**velocità in bit**](bit-rate.md).

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




