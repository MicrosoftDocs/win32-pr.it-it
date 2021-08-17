---
title: WM/MCDI
description: L'attributo WM/MCDI contiene l'identificatore cd musicale. Si tratta di un dump binario del sommario del CD usato per identificare in modo univoco il CD.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- Formato windows media WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bccf4a081141c1902fe93680937a3196e015e6690acf76d69f3a3d8a016c092e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963750"
---
# <a name="wmmcdi"></a>WM/MCDI

**L'attributo WM/MCDI** contiene l'identificatore cd musicale. Si tratta di un dump binario del sommario del CD usato per identificare in modo univoco il CD.

## <a name="global-constant"></a>Costante globale

g \_ wszWMMCDI

## <a name="data-type"></a>Tipo di dati

**FILE \_ BINARIO DI TIPO WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo è compatibile con il frame ID3, MCDI. La specifica ID3 per il frame MCDI richiede che esista solo un frame di questo tipo per ogni file e che esista un frame TRCK valido. L'editor dei metadati non esegue alcuna convalida per queste regole. Inoltre, le dimensioni di WM/MCDI non sono limitate a 804 byte, così come il frame MCDI ID3.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




