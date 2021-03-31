---
title: input dcl_usage (SM1, SM2, SM3-vs ASM)
description: Dichiarare l'associazione tra l'utilizzo di un elemento vertice e un indice di utilizzo per un registro di input del vertex shader.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38113846fe62c37247bb2d3ca522a34dc9282441
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473534"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a>\_input utilizzo DCL (SM1, SM2, SM3-vs ASM)

Dichiarare l'associazione tra l'utilizzo di un elemento vertice e un indice di utilizzo per un registro di input del vertex shader.

## <a name="syntax"></a>Sintassi



|                                |
|--------------------------------|
| \_ \[ Indice utilizzo utilizzo \_ DCL \] v\# |



 

Dove:

-   \_l'utilizzo di DCL identifica il modo in cui verranno usati i dati del registro. Si tratta dello stesso valore dei membri di [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) senza il prefisso D3DDECLUSAGE.
-   Usage \_ index è un indice integer facoltativo compreso tra 0 e 15. Modifica i dati di utilizzo. L'indice corrisponde all'indice di utilizzo in una dichiarazione di vertice. Vedere [dichiarazione vertici (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration). L'indice viene aggiunto al valore di utilizzo ( \_ utilizzo di DCL) senza spazio. Se non viene specificato, si presuppone che sia 0.
-   v \# è un [Registro di input](dx9-graphics-reference-asm-vs-registers-input.md).

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| utilizzo di DCL \_             | x    | x    | x    | x     | x    | x     |



 

Tutte le \_ istruzioni di utilizzo di DCL devono essere visualizzate prima della prima istruzione eseguibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 