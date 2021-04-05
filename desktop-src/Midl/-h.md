---
title: /h (opzione)
description: L'opzione/h è equivalente dal punto di vista funzionale all'opzione/header.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h switch MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ff2cd7aa5e4b8386e0c9faecfaccd860207403
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045837"
---
# <a name="h-switch"></a>/h (opzione)

L'opzione **/h** è equivalente dal punto di vista funzionale all'opzione [**/header**](-header.md) .

``` syntax
midl /h filename
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*filename* 
</dt> <dd>

Specifica un nome di file di intestazione che esegue l'override del nome del file di intestazione predefinito. I nomi di file possono essere racchiusi tra virgolette doppie (") per evitare che la shell interpreti caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'opzione **/h** specifica *filename* come nome di un file di intestazione che contiene tutte le definizioni contenute nel file IDL, senza la sintassi IDL. Questo file può essere usato come file di intestazione C o C++.

## <a name="examples"></a>Esempio

**MIDL/h tlibhead. h nomefile. idl**

**MIDL/h "MIDL. h" nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> </dl>

 

 




