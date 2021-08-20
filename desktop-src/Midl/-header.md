---
title: Opzione /header
description: L'opzione /header specifica il nome del file di intestazione.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- Opzione /header MIDL
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fde032d611cb09f3da2d048bfab85bd3b0a1c8aadebf251fe8c01ecd8630a36e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808971"
---
# <a name="header-switch"></a>Opzione /header

**L'opzione /header** specifica il nome del file di intestazione.

``` syntax
midl /header filename
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*Filename* 
</dt> <dd>

Specifica un nome di file di intestazione che esegue l'override del nome del file di intestazione predefinito. I nomi di file possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il nome file specificato sostituisce il nome file predefinito. Il nome file predefinito viene ottenuto sostituendo l'estensione del nome file IDL (in genere con estensione idl) con l'estensione h. Per le interfacce OLE, **l'opzione /header** esegue l'override del nome predefinito del file di intestazione dell'interfaccia.

Quando si importano file, il nome file specificato si applica a un solo file di intestazione, ovvero il file di intestazione che corrisponde al file IDL specificato nella riga di comando.

Se *filename* non include un percorso esplicito, il file viene scritto nella directory corrente o nella directory specificata dall'opzione [**/out.**](-out.md) Un percorso esplicito nel *nome file* esegue l'override della **specifica dell'opzione /out.**

## <a name="examples"></a>Esempio

**midl /header "bar.h" filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
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

 

 




