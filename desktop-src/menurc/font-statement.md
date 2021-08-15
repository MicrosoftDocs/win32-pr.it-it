---
title: Istruzione FONT
description: Definisce il tipo di carattere con cui il sistema disegna testo nella finestra di dialogo. Il tipo di carattere deve essere stato caricato in precedenza. ad esempio chiamando la funzione LoadResource.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Menu e altre risorse dell'istruzione FONT
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad289923503866ba2bcd9338bb59a556d0e37cd0a839d4eede0f95a0bec5fd76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972070"
---
# <a name="font-statement"></a>Istruzione FONT

Definisce il tipo di carattere con cui il sistema disegna testo nella finestra di dialogo. Il tipo di carattere deve essere stato caricato in precedenza. ad esempio chiamando la [**funzione LoadResource.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*
</dt> <dd>

Dimensione del tipo di carattere, in punti.

</dd> <dt>

<span id="typeface"></span><span id="TYPEFACE"></span>*Carattere tipografico*
</dt> <dd>

Nome del carattere tipografico. Questo parametro deve essere racchiuso tra virgolette (").

</dd> <dt>

<span id="weight"></span><span id="WEIGHT"></span>*Peso*
</dt> <dd>

Spessore del tipo di carattere compreso tra 0 e 1000. Ad esempio, 400 è normale e 700 è in grassetto. Se questo valore è 0, viene usato il peso predefinito. Per un elenco di valori predefiniti, vedere i **valori FW \_ \*** definiti in WinGDI.h.

</dd> <dt>

<span id="italic"></span><span id="ITALIC"></span>*Corsivo*
</dt> <dd>

Indica un tipo di carattere corsivo se impostato su TRUE.

</dd> <dt>

<span id="charset"></span><span id="CHARSET"></span>*Charset*
</dt> <dd>

Set di caratteri. Per un elenco di valori, vedere il **membro lfCharSet** della [**struttura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'uso **dell'istruzione FONT:**

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 