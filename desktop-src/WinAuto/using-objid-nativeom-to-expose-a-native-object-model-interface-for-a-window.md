---
title: Usare OBJID \_ NATIVEOM per esporre un'interfaccia nativa per una finestra
description: Questa tecnica consente ai client di ottenere un oggetto personalizzato per una finestra. I server possono usare questo oggetto per esporre un puntatore a un oggetto documento personalizzato per una finestra.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed99db4641235ceee57688865710c19a41f0a517d70d4601d138150cb88dd470
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098091"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a>Usare OBJID \_ NATIVEOM per esporre un'interfaccia nativa per una finestra

Questa tecnica consente ai client di ottenere un oggetto personalizzato per una finestra. I server possono usare questo oggetto per esporre un puntatore a un oggetto documento personalizzato per una finestra.

**Per esporre un'interfaccia del modello a oggetti nativa per una finestra (server)**

1.  Gestire il [**messaggio WM \_ GETOBJECT**](wm-getobject.md) nella routine della finestra. Quando il *valore lParam* è [**OBJID \_ NATIVEOM,**](object-identifiers.md)restituisce un puntatore a interfaccia all'oggetto personalizzato [**usando LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
2.  Rilasciare il puntatore di interfaccia [**dopo aver chiamato LresultFromObject,**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)se appropriato. Per altre informazioni, vedere **LresultFromObject.**

I client possono ottenere un puntatore a questo oggetto personalizzato.

**Per ottenere un puntatore per un oggetto personalizzato per una finestra (client)**

-   Chiamare [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e passare [**OBJID \_ NATIVEOM**](object-identifiers.md) come secondo parametro.

Tenere presente i problemi seguenti per questa tecnica:

-   Questa tecnica è simile alla restituzione di un puntatore di interfaccia [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ad eccezione dell'ID oggetto usato e del fatto che [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) restituisce un oggetto personalizzato anziché **IAccessible.**
-   Gli sviluppatori di server potrebbero dover pubblicare informazioni che consentano ai client di identificare in modo univoco **l'oggetto HWND** in modo che possano trovarlo prima di chiamare [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) sul relativo handle di finestra.
-   Non implementare [**l'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sull'oggetto personalizzato restituito. In caso contrario, OLEACC lo tratterà come **IAccessible** standard e potrebbe impedire l'uso delle interfacce personalizzate.
-   Per poter essere usate in più processi, potrebbe essere necessario registrare le interfacce nell'oggetto restituito con Component Object Model (COM).

Questa tecnica è supportata da diversi Microsoft Office componenti. Per altre informazioni, vedere [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)

 

 




