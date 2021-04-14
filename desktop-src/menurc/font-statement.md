---
title: Istruzione FONT
description: Definisce il tipo di carattere con cui il sistema trarrà il testo nella finestra di dialogo. Il tipo di carattere deve essere stato caricato in precedenza; ad esempio, chiamando la funzione LoadResource.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Menu di istruzioni dei tipi di carattere e altre risorse
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b31b280a5a973301e8410f1f74340138af07ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473051"
---
# <a name="font-statement"></a>Istruzione FONT

Definisce il tipo di carattere con cui il sistema trarrà il testo nella finestra di dialogo. Il tipo di carattere deve essere stato caricato in precedenza; ad esempio, chiamando la funzione [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*
</dt> <dd>

Dimensioni in punti del tipo di carattere.

</dd> <dt>

<span id="typeface"></span><span id="TYPEFACE"></span>*carattere tipografico*
</dt> <dd>

Nome del carattere tipografico. Questo parametro deve essere racchiuso tra virgolette (").

</dd> <dt>

<span id="weight"></span><span id="WEIGHT"></span>*peso*
</dt> <dd>

Spessore del tipo di carattere nell'intervallo compreso tra 0 e 1000. 400, ad esempio, è normale e 700 è in grassetto. Se questo valore è 0, viene utilizzato il peso predefinito. Per un elenco di valori predefiniti, vedere i valori **FW \_ \*** definiti in wingdi. h.

</dd> <dt>

<span id="italic"></span><span id="ITALIC"></span>*corsivo*
</dt> <dd>

Indica un tipo di carattere corsivo se impostato su TRUE.

</dd> <dt>

<span id="charset"></span><span id="CHARSET"></span>*charset*
</dt> <dd>

Set di caratteri. Per un elenco di valori, vedere il membro **lfCharSet** della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **font** :

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 