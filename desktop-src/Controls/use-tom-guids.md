---
title: Come usare i GUID TOM
description: I GUID TOM (Text Object Model) vengono dati in Tom.h all'interno delle istruzioni MIDL \_ INTERFACE. Per usare le interfacce associate, è necessario prima dichiarare l'interfaccia usando il GUID.
ms.assetid: 48FF98C9-D42E-4E7F-874F-8E56F730E24E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c5c892ecac4b13a6e74aedad6c2a373908d2173c105ab0dbb0ec49c1439c36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828532"
---
# <a name="how-to-use-tom-guids"></a>Come usare i GUID TOM

I GUID TOM (Text Object Model) vengono dati in Tom.h all'interno delle istruzioni MIDL \_ INTERFACE. Per usare le interfacce associate, è necessario prima dichiarare l'interfaccia usando il GUID.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="use-a-tom-guid"></a>Usare un GUID TOM

Il codice di esempio seguente illustra come usare [**l'interfaccia ITextDocument.**](/windows/desktop/api/Tom/nn-tom-itextdocument)


```C++
#define DEFINE_GUIDXXX(name, l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8) \
        EXTERN_C const GUID CDECL name \
                = { l, w1, w2, { b1, b2,  b3,  b4,  b5,  b6,  b7,  b8 } }

DEFINE_GUIDXXX(IID_ITextDocument,0x8CC497C0,0xA1DF,0x11CE,0x80,0x98,
                0x00,0xAA,0x00,0x47,0xBE,0x5D);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del modello a oggetti di testo](using-the-text-object-model.md)
</dt> <dt>

[Uso dei controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




