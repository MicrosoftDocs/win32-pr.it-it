---
description: Dichiara un oggetto come una costante pick-any, per evitare ricaricamenti ridondanti di tale oggetto se viene usato (e dichiarato) in più posizioni nella libreria DirectXMath.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: XMGLOBALCONST (macro)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309220"
---
# <a name="xmglobalconst-macro"></a>XMGLOBALCONST (macro)

Dichiara un oggetto come una costante *pick-any* , per evitare ricaricamenti ridondanti di tale oggetto se viene usato (e dichiarato) in più posizioni nella libreria DirectXMath.

## <a name="syntax"></a>Sintassi

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a>Osservazioni

L'uso di XMGLOBALCONST consente di specificare le costanti globali. Ciò consente di ridurre le dimensioni del segmento di dati di un'applicazione, evitare la creazione e l'eliminazione di oggetti ridondanti e ridurre le operazioni di caricamento e archiviazione.

## <a name="requirements"></a>Requisiti

**Intestazione:** Dichiarata in DirectXMath. h.

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

 

 
