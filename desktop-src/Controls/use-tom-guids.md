---
title: Come usare i GUID di TOM
description: I GUID di TOM (Text Object Model) sono forniti in Tom. h all'interno delle \_ istruzioni dell'interfaccia MIDL. Per usare le interfacce associate, è necessario prima dichiarare l'interfaccia usando il GUID.
ms.assetid: 48FF98C9-D42E-4E7F-874F-8E56F730E24E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c937d8b3c3612a3a49f27f18ac7c392b7a596
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "104472451"
---
# <a name="how-to-use-tom-guids"></a>Come usare i GUID di TOM

I GUID di TOM (Text Object Model) sono forniti in Tom. h all'interno delle \_ istruzioni dell'interfaccia MIDL. Per usare le interfacce associate, è necessario prima dichiarare l'interfaccia usando il GUID.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-a-tom-guid"></a>Usare un GUID di TOM

Nell'esempio di codice riportato di seguito viene illustrato come utilizzare l'interfaccia [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) .


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

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




