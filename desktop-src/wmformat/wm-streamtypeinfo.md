---
title: WM/StreamTypeInfo
description: L'attributo WM/StreamTypeInfo contiene le informazioni di configurazione per il flusso specificato nel file ASF.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- Formato di Windows Media WM/StreamTypeInfo
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397486"
---
# <a name="wmstreamtypeinfo"></a>WM/StreamTypeInfo

L'attributo **WM/StreamTypeInfo** contiene le informazioni di configurazione per il flusso specificato nel file ASF.

## <a name="global-constant"></a>Costante globale

g \_ wszWMStreamTypeInfo

## <a name="data-type"></a>Tipo di dati

[**WM \_ \_ \_ informazioni sul tipo di flusso**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**\_ \_ Binary di tipo WMT**)

## <a name="remarks"></a>Commenti

Questo attributo si applica a flussi specifici. Non è possibile recuperare questo attributo per il flusso 0.

Questo attributo è di sola lettura.

È possibile accedere a **WM/StreamTypeInfo** dall'oggetto dell'editor di metadati. Questo è l'unico modo per accedere alle informazioni di configurazione del flusso senza aprire il file con l'oggetto Reader (o l'oggetto Reader sincrono).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




