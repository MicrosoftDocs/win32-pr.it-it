---
title: Opzione /tlb
description: L'opzione /tlb specifica un nome file per la libreria dei tipi generata dal compilatore MIDL.
ms.assetid: 7d5d9f92-ed1a-46bc-beb1-4be70d0a4813
keywords:
- Opzione /tlb MIDL
topic_type:
- apiref
api_name:
- /tlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 081723648788ec51fa65a4770deb336f665804a9527dc223000826870dbe1ee0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643751"
---
# <a name="tlb-switch"></a>Opzione /tlb

**L'opzione /tlb** specifica un nome file per la libreria dei tipi generata dal compilatore MIDL.

``` syntax
midl /tlb filename
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*Filename* 
</dt> <dd>

Specifica il nome del file della libreria dei tipi di output (TLB). Per impostazione predefinita, se non si usa l'opzione **/tlb** , il file TLB ha lo stesso nome del file IDL, con estensione . Tlb.

</dd> </dl>

## <a name="examples"></a>Esempio

**midl /tlb newname.tlb**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/notlb**](-notlb.md)
</dt> </dl>

 

 




