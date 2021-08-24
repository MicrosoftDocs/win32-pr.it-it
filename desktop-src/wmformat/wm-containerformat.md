---
title: WM/ContainerFormat
description: L'attributo WM/ContainerFormat specifica il tipo di file caricato nell'oggetto chiamante.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- WM/ContainerFormat windows Media Format
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e0d5cc430b0580c6719d212d664d8c19ddc65eee64e5877a8e6aba80d94a6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839441"
---
# <a name="wmcontainerformat"></a>WM/ContainerFormat

**L'attributo WM/ContainerFormat** specifica il tipo di file caricato nell'oggetto chiamante.

## <a name="global-constant"></a>Costante globale

g \_ wszWMContainerFormat

## <a name="data-type"></a>Tipo di dati

[**WMT \_ FORMATO \_ DI ARCHIVIAZIONE**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) ( FILE **\_ BINARIO DI TIPO \_ WMT**)

## <a name="remarks"></a>Commenti

Questo attributo viene usato al posto di **IWMProfile3::GetStorageFormat** e **IWMProfile3::SetStorageFormat,** che non sono più supportati.

Si tratta di un attributo codificato.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene usato per un singolo flusso, verrà considerato come metadati personalizzati e non trasmetterà il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




