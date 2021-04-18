---
title: Linee guida per COM e Unicode
description: Poiché Microsoft Active Accessibility si basa su Component Object Model (COM), gli sviluppatori hanno bisogno di un livello moderato di informazioni sugli oggetti e sulle interfacce COM e devono sapere come eseguire le attività di base, ad esempio come inizializzare la libreria COM.
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2312b6177891c31c0987b846f7adfc1aa08abc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299936"
---
# <a name="com-and-unicode-guidelines"></a>Linee guida per COM e Unicode

Poiché Microsoft Active Accessibility si basa su Component Object Model (COM), gli sviluppatori hanno bisogno di un livello moderato di informazioni sugli oggetti e sulle interfacce COM e devono sapere come eseguire le attività di base, ad esempio come inizializzare la libreria COM. Gli sviluppatori di server devono comprendere come progettare classi che implementano l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e come creare oggetti accessibili.

È anche necessario un livello moderato di informazioni su Unicode per usare molte delle funzioni di Microsoft Active Accessibility che restituiscono stringhe.

Per utilizzare Microsoft Active Accessibility in modo efficace, è necessario comprendere le funzioni, le strutture, i tipi di dati e le interfacce COM e Unicode seguenti. In questa documentazione vengono fornite informazioni limitate su alcuni di questi elementi.

### <a name="functions"></a>Funzioni:

-   [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
-   [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [ **IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)
-   [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) e [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)
-   [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
-   [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) e [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

### <a name="structures-and-data-types"></a>Strutture e tipi di dati:

-   [**VARIANTE**](variant-structure.md)
-   [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)
-   [**BSTR**](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a>Interfacce COM:

-   [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [**IDispatch**](idispatch-interface.md)
-   [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a>Contenuto della sezione

-   [Struttura VARIANT](variant-structure.md)
-   [IDispatch (interfaccia)](idispatch-interface.md)
-   [Conversione di stringhe Unicode e ANSI](converting-unicode-and-ansi-strings.md)

 

 