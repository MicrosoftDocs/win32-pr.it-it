---
title: dcl_usage input (sm1, sm2, sm3 - vs asm)
description: Dichiarare l'associazione tra l'utilizzo di un elemento vertice e un indice di utilizzo per un registro di input vertex shader.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae4b024bbce0636127b0ed0fc5f42bc466e1b7fd
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129688"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a>dcl \_ usage input (sm1, sm2, sm3 - vs asm)

Dichiarare l'associazione tra l'utilizzo di un elemento vertice e un indice di utilizzo per un registro di input vertex shader.

## <a name="syntax"></a>Sintassi

dcl \_ usage usage index \[ \_ \] v\#



 

Dove:

-   dcl \_ usage identifica il modo in cui verranno usati i dati del registro. Si tratta dello stesso valore dei membri di [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) senza il prefisso D3DDECLUSAGE.
-   usage \_ index è un indice integer facoltativo compreso tra 0 e 15. Modifica i dati di utilizzo. L'indice corrisponde all'indice di utilizzo in una dichiarazione di vertice. Vedere [Dichiarazione dei vertici (Direct3D 9).](/windows/desktop/direct3d9/vertex-declaration) L'indice viene aggiunto al valore di utilizzo (utilizzo dcl \_ ) senza spazio. Se non viene fornito, si presuppone che sia 0.
-   v \# è un registro di [input.](dx9-graphics-reference-asm-vs-registers-input.md)

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dcl \_ usage             | x    | x    | x    | x     | x    | x     |



 

Tutte le istruzioni dcl \_ usage devono essere visualizzate prima della prima istruzione eseguibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
