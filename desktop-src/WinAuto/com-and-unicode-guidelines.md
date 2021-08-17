---
title: Linee guida COM e Unicode
description: Poiché Microsoft Active Accessibility è basato su Component Object Model (COM), gli sviluppatori devono avere un livello moderato di comprensione degli oggetti e delle interfacce COM e devono sapere come eseguire attività di base, ad esempio come inizializzare la libreria COM.
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023b1d58a1a31997142097d02d8fc7d80881111e08f0020d967c1984d9946c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133904"
---
# <a name="com-and-unicode-guidelines"></a>Linee guida COM e Unicode

Poiché Microsoft Active Accessibility è basato su Component Object Model (COM), gli sviluppatori devono avere un livello moderato di comprensione degli oggetti e delle interfacce COM e devono sapere come eseguire attività di base, ad esempio come inizializzare la libreria COM. Gli sviluppatori di server devono comprendere come progettare classi che implementano [**l'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e come creare oggetti accessibili.

È anche necessario un livello moderato di comprensione di Unicode per usare molte delle funzioni Microsoft Active Accessibility che restituiscono stringhe.

Per usare Microsoft Active Accessibility in modo efficace, è necessario comprendere le funzioni, le strutture, i tipi di dati e le interfacce COM e Unicode seguenti. In questa documentazione vengono fornite informazioni limitate su alcuni di questi elementi.

### <a name="functions"></a>Funzioni:

-   [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
-   [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [ **IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)
-   [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) e [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)
-   [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
-   [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) e [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

### <a name="structures-and-data-types"></a>Strutture e tipi di dati:

-   [**Variante**](variant-structure.md)
-   [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)
-   [**BSTR**](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a>Interfacce COM:

-   [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [**Idispatch**](idispatch-interface.md)
-   [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a>Contenuto della sezione

-   [Struttura VARIANT](variant-structure.md)
-   [Interfaccia IDispatch](idispatch-interface.md)
-   [Conversione di stringhe Unicode e ANSI](converting-unicode-and-ansi-strings.md)

 

 