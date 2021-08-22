---
description: Dichiara un oggetto come costante pick-any, per evitare ricaricamenti ridondanti di tale oggetto se viene usato (e dichiarato) in più posizioni nella libreria DirectXMath.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: Macro XMGLOBALCONST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be72254865aed46de86955c2a27a4d73351311c5aa63a44a6e218be7a3915d1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118001"
---
# <a name="xmglobalconst-macro"></a>Macro XMGLOBALCONST

Dichiara un oggetto come costante *pick-any,* per evitare ricaricamenti ridondanti di tale oggetto se viene usato (e dichiarato) in più posizioni nella libreria DirectXMath.

## <a name="syntax"></a>Sintassi

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a>Osservazioni

L'uso di XMGLOBALCONST consente di specificare le costanti globali. In questo modo è possibile ridurre le dimensioni del segmento di dati di un'applicazione, evitare la creazione e la distruzione di oggetti ridondanti e ridurre le operazioni di caricamento e archiviazione.

## <a name="requirements"></a>Requisiti

**Intestazione:** Dichiarato in DirectXMath.h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Macro della libreria DirectXMath](ovw-xnamath-reference-macros.md)
</dt> <dt>

[Costanti globali nella libreria DirectXMath](pg-xnamath-internals.md)
</dt> <dt>

[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))
</dt> <dt>

[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))
</dt> </dl>

 

 
