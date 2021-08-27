---
title: Opzione /h
description: Dal punto di vista funzionale, l'opzione /h equivale all'opzione /header.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- Opzione /h MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71bf02668a583b330684338cbc3f639fbbda5a340c7226e10956233aa8dc9ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105611"
---
# <a name="h-switch"></a>Opzione /h

Dal punto di vista funzionale, l'opzione **/h** equivale all'opzione [**/header.**](-header.md)

``` syntax
midl /h filename
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*Filename* 
</dt> <dd>

Specifica un nome di file di intestazione che esegue l'override del nome del file di intestazione predefinito. I nomi di file possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

**L'opzione /h** specifica *filename* come nome di un file di intestazione che contiene tutte le definizioni contenute nel file IDL, senza la sintassi IDL. Questo file può essere usato come file di intestazione C o C++.

## <a name="examples"></a>Esempio

**midl /h tlibhead.h filename.idl**

**midl /h "midl.h" filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> </dl>

 

 




