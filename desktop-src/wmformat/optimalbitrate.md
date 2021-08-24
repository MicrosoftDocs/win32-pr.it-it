---
title: OptimalBitrate
description: L'attributo OptimalBitrate contiene la velocità in bit con cui viene riprodotto il file.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- OptimalBitrate windows Media Format
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f670c2acd2f2190a5ee2bfd76994c219c6f967dbbd933520a8d4627236a0d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930631"
---
# <a name="optimalbitrate"></a>OptimalBitrate

**L'attributo OptimalBitrate** contiene la velocità in bit con cui viene riprodotto il file.

## <a name="global-constant"></a>Costante globale

g \_ wszWMOptimalBitrate

## <a name="data-type"></a>Tipo di dati

**DWORD \_ DI TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Per i file che contengono flussi VBR (Variable Bit Rate), questo valore è la velocità in bit di picco per i flussi nel file. Per i file senza VBR, questo valore è uguale a [**Velocità in bit**](bit-rate.md).

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene usato per un singolo flusso, verrà considerato come metadati personalizzati e non trasmetterà il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




