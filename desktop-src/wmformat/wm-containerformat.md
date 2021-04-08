---
title: WM/ContainerFormat
description: L'attributo WM/ContainerFormat specifica il tipo di file caricato nell'oggetto chiamante.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- Formato di Windows Media WM/ContainerFormat
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718592"
---
# <a name="wmcontainerformat"></a>WM/ContainerFormat

L'attributo **WM/containerFormat** specifica il tipo di file caricato nell'oggetto chiamante.

## <a name="global-constant"></a>Costante globale

g \_ wszWMContainerFormat

## <a name="data-type"></a>Tipo di dati

[**WMT \_ \_formato di archiviazione**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**\_ \_ binario di tipo WMT**)

## <a name="remarks"></a>Commenti

Questo attributo viene usato al posto di **IWMProfile3:: GetStorageFormat** e **IWMProfile3:: SetStorageFormat**, che non sono più supportati.

Si tratta di un attributo codificato.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




