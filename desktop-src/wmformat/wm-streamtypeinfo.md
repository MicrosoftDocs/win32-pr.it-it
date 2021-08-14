---
title: WM/StreamTypeInfo
description: L'attributo WM/StreamTypeInfo contiene le informazioni di configurazione per il flusso specificato nel file ASF.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- WM/StreamTypeInfo windows Media Format
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb40926d5ecba3aea2c7f2db64850152c66a25861d4422fddf04670c76d8148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698273"
---
# <a name="wmstreamtypeinfo"></a>WM/StreamTypeInfo

**L'attributo WM/StreamTypeInfo** contiene le informazioni di configurazione per il flusso specificato nel file ASF.

## <a name="global-constant"></a>Costante globale

g \_ wszWMStreamTypeInfo

## <a name="data-type"></a>Tipo di dati

[**WM \_ INFORMAZIONI \_ SUL TIPO DI \_ FLUSSO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**FILE \_ BINARIO DI TIPO \_ WMT**)

## <a name="remarks"></a>Commenti

Questo attributo si applica a flussi specifici. Non è possibile recuperare questo attributo per il flusso 0.

Questo attributo è di sola lettura.

**WM/StreamTypeInfo** è accessibile dall'oggetto dell'editor di metadati. Questo è l'unico modo per accedere alle informazioni di configurazione del flusso senza aprire il file con l'oggetto lettore (o l'oggetto lettore sincrono).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




