---
title: opzione/header
description: L'opzione/header specifica il nome del file di intestazione.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- /header switch MIDL
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397878"
---
# <a name="header-switch"></a>opzione/header

L'opzione **/header** specifica il nome del file di intestazione.

``` syntax
midl /header filename
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*filename* 
</dt> <dd>

Specifica un nome di file di intestazione che esegue l'override del nome del file di intestazione predefinito. I nomi di file possono essere racchiusi tra virgolette doppie (") per evitare che la shell interpreti caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il nome file specificato sostituisce il nome file predefinito. Il nome file predefinito viene ottenuto sostituendo l'estensione del nome file IDL (in genere IDL) con l'estensione di file. h. Per le interfacce OLE, l'opzione **/header** sostituisce il nome predefinito del file di intestazione dell'interfaccia.

Quando si importano file, il nome file specificato si applica a un solo file di intestazione, ovvero il file di intestazione che corrisponde al file IDL specificato nella riga di comando.

Se *filename* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata dall'opzione [**/out**](-out.md) . Un percorso esplicito in *filename* esegue l'override della specifica del Commuter **/out** .

## <a name="examples"></a>Esempio

**MIDL/header "bar. h" nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/h**](-h.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> </dl>

 

 




