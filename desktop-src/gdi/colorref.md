---
Description: Il valore COLORREF viene usato per specificare un colore RGB.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (Windef.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 3e51b2a906af5939a5c7a8753e5fcc4fbcfae64590e62bcb6df1da2c2bd8426d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761894"
---
# <a name="colorref"></a>COLORREF

Il valore COLORREF viene usato per specificare un [colore RGB.](/windows/desktop/api/Wingdi/nf-wingdi-rgb)


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a>Commenti

Quando si specifica un colore [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) esplicito, il **valore COLORREF** ha il formato esadecimale seguente:

`0x00bbggrr`

Il byte meno significativo contiene un valore per l'intensità relativa del rosso. il secondo byte contiene un valore per il verde. e il terzo byte contiene un valore per il blu. Il byte di ordine elevato deve essere zero. Il valore massimo per un singolo byte è 0xFF.

Per creare un **valore di colore COLORREF,** usare la macro [RGB.](/windows/desktop/api/Wingdi/nf-wingdi-rgb) Per estrarre i singoli valori per i componenti rosso, verde e blu di un valore di colore, usare rispettivamente le macro [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)e [GetBValue.](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)

## <a name="example"></a>Esempio

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

Esempio di [Windows esempi classici](https://github.com/microsoft/Windows-classic-samples) in GitHub.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>Windef.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica dei colori](colors.md)
</dt> <dt>

[Strutture dei colori](color-structures.md)
</dt> <dt>

[GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




