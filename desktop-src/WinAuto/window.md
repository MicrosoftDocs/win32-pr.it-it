---
title: Finestra (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)
description: Microsoft Active Accessibility crea un oggetto finestra generico come contenitore per un altro oggetto. Gli sviluppatori client non comunicano le informazioni dagli oggetti finestra agli utenti finali perché questi oggetti non contengono informazioni utili.
ms.assetid: cc32528f-c454-4522-91b9-06f87cff8bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881eb863c6b12f8e72a9f48ba5ea290a2ad2f2471fa60683ee17e70c6271dad3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413271"
---
# <a name="window-msaa-ui-element-reference"></a>Finestra (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **Window ai** fini delle informazioni di riferimento sugli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti Window** in vari framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il framework dell'interfaccia utente in uso.

 

Microsoft Active Accessibility crea un oggetto finestra generico come contenitore per un altro oggetto. Gli sviluppatori client non comunicano le informazioni dagli oggetti finestra agli utenti finali perché questi oggetti non contengono informazioni utili.

Se un'applicazione server crea un controllo personalizzato, Microsoft Active Accessibility crea un oggetto finestra che contiene il controllo personalizzato, ma il server crea un oggetto accessibile per fornire informazioni sul contenuto del controllo. Il sistema genera eventi a livello di oggetto per l'oggetto finestra, ma il server deve inviare eventi per l'oggetto accessibile che fornisce informazioni sul controllo.

## <a name="iaccessible-methods"></a>Metodi IAccessible

L'oggetto window supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

L'oggetto window supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera [l'interfaccia IDispatch](idispatch-interface.md) dell'elemento figlio specificato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **proprietà ChildCount** è 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | L'oggetto finestra stesso non ha una **proprietà Description.** La **proprietà Description** per l'oggetto figlio può essere recuperata tramite l'oggetto finestra.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | L'oggetto finestra stesso non ha una **proprietà KeyboardShortcut.** La **proprietà KeyboardShortcut** per l'oggetto figlio viene recuperata tramite l'oggetto finestra.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **proprietà Name** dell'oggetto finestra è uguale all'oggetto figlio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ WINDOW.**](object-roles.md) Il **ruolo** dell'oggetto figlio viene recuperato tramite l'oggetto finestra.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| SIZEABLE STATE SYSTEM [**\_ \_**](object-state-constants.md) \| [**\_ \_ MOVEABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Note

Gli eventi [**EVENT \_ SYSTEM \_ DRAGDROPSTART,**](event-constants.md) [**EVENT SYSTEM \_ \_ DRAGDROPEND,**](event-constants.md) [**EVENT OBJECT \_ \_ HIDE**](event-constants.md)e [**EVENT OBJECT \_ \_ PARENTCHANGE**](event-constants.md) non vengono inviati dall'oggetto finestra. Si tratta di un problema noto che viene risolto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





