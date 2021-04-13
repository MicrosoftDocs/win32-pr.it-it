---
title: Modalità di utilizzo degli ID figlio nei parametri
description: In questo argomento vengono descritti i parametri di input, i parametri di output e i casi speciali per interpretare gli ID figlio restituiti dai metodi IAccessible.
ms.assetid: 051ec5ba-540c-4ae1-b917-4c229557ca2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03026e6abf769efab95cc513231fad3af64511f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399272"
---
# <a name="how-child-ids-are-used-in-parameters"></a>Modalità di utilizzo degli ID figlio nei parametri

In questo argomento vengono descritti i parametri di input, i parametri di output e i casi speciali per interpretare gli ID figlio restituiti dai metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

## <a name="input-parameters"></a>Parametri di input

Molte delle funzioni di Microsoft Active Accessibility e la maggior parte delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) accettano una struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) come parametro di input. Per la maggior parte delle proprietà **IAccessible** , questo parametro consente agli sviluppatori di client di specificare se desiderano informazioni sull'oggetto stesso o su uno degli elementi semplici dell'oggetto.

Microsoft Active Accessibility fornisce la costante **CHILDID \_ self** per indicare che sono necessarie informazioni sull'oggetto stesso. Per ottenere informazioni su un elemento semplice, gli sviluppatori client specificano il relativo ID figlio nel parametro [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .

Quando si Inizializza un parametro [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , assicurarsi di specificare **VT \_ I4** nel membro **VT** , oltre a specificare il valore ID figlio (o **CHILDID \_ self**) nel membro **LVAL** .

Per ottenere, ad esempio, il nome di un oggetto e non uno degli elementi figlio dell'oggetto, inizializzare la [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) per il primo parametro di [**IAccessible:: Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) ( **CHILDID \_ self** nel membro **LVAL** e **VT \_ I4** nel membro **VT** ), quindi chiamare **IAccessible:: Get \_ accName**.

## <a name="output-parameters"></a>Parametri di output

Diverse funzioni e metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) hanno un [](/windows/win32/api/oaidl/ns-oaidl-variant) \* parametro di output Variant che contiene un ID figlio o un puntatore di interfaccia [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) a un oggetto figlio. Ci sono diversi passaggi che un client deve eseguire a seconda che ricevano un ID figlio **VT \_ I4** (elemento semplice) o un puntatore di interfaccia **IDispatch** con **CHILDID \_ self** (Full Object). Seguendo questi passaggi, fornirà un puntatore all'interfaccia **IAccessible** e un ID figlio che consentiranno ai client di usare i metodi e le proprietà **IAccessible** . Questi passaggi si applicano ai metodi [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest), [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)e [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) . Si applicano anche alle funzioni client [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)e [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) .

Nella tabella seguente sono elencati i possibili risultati restituiti e i passaggi di post-elaborazione necessari in modo che i client dispongano di un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e di un ID figlio.



| Risultato restituito                                      | Post-elaborazione per il valore restituito                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Puntatore all'interfaccia [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) | Si tratta di un oggetto completo. Chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per accedere al puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .<br/> Usare il puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) con **CHILDID \_ self** per accedere ai metodi e alle proprietà **IAccessible** .<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| \_ID figlio I4 VT                                      | Chiamare [**IAccessible:: Get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) usando l'ID figlio per verificare se si dispone di un puntatore a interfaccia [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) . Se si ottiene un puntatore a interfaccia [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , usarlo con **CHILDID \_ self** per accedere ai metodi e alle proprietà dell'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .<br/> Se la chiamata a [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) ha esito negativo, si ha un elemento semplice. Usare il puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) originale (quello usato nella chiamata al metodo o alla funzione menzionato in precedenza) con l'ID figlio **VT \_ I4** restituito dalla chiamata.<br/> |



 

Prima di poter usare un parametro [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , è necessario inizializzarlo chiamando la funzione [**VARIANTINIT**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (com). Al termine della struttura, chiamare [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear) per liberare la memoria riservata a tale **variante**.

## <a name="special-cases"></a>Casi speciali

Esistono eccezioni alle linee guida della tabella precedente, ad esempio quando un ID figlio viene restituito dal metodo [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) . I server devono restituire un'interfaccia [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) se l'elemento figlio è un oggetto accessibile. Se un ID figlio viene restituito da **IAccessible:: accHitTest**, l'elemento figlio è un elemento semplice.

Inoltre, esistono casi speciali per [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate). Per ulteriori informazioni, vedere **IAccessible:: accNavigate** e [navigazione spaziale e logica](spatial-and-logical-navigation.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[IDispatch (interfaccia)](idispatch-interface.md)
</dt> <dt>

[Struttura VARIANT](variant-structure.md)
</dt> </dl>

 

