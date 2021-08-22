---
title: Come vengono usati gli ID figlio nei parametri
description: Questo argomento descrive i parametri di input, i parametri di output e casi speciali per l'interpretazione degli ID figlio restituiti dai metodi IAccessible.
ms.assetid: 051ec5ba-540c-4ae1-b917-4c229557ca2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc0c3be970fb4a688a0a5447b72719428e78e074cbc7a17f2b6b698fcca177f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052722"
---
# <a name="how-child-ids-are-used-in-parameters"></a>Come vengono usati gli ID figlio nei parametri

Questo argomento descrive i parametri di input, i parametri di output e casi speciali per l'interpretazione degli ID figlio restituiti dai [**metodi IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

## <a name="input-parameters"></a>Parametri di input

Molte delle funzioni Microsoft Active Accessibility e la maggior parte delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) accettano una [**struttura VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) come parametro di input. Per la maggior parte **delle proprietà IAccessible,** questo parametro consente agli sviluppatori client di specificare se desiderano informazioni sull'oggetto stesso o su uno degli elementi semplici dell'oggetto.

Microsoft Active Accessibility fornisce la costante **CHILDID \_ SELF** per indicare che sono necessarie informazioni sull'oggetto stesso. Per ottenere informazioni su un elemento semplice, gli sviluppatori client specificano il relativo ID figlio nel [**parametro VARIANT.**](/windows/win32/api/oaidl/ns-oaidl-variant)

Quando si inizializza un parametro [**VARIANT,**](/windows/win32/api/oaidl/ns-oaidl-variant) assicurarsi di specificare **VT \_ I4** nel membro **vt** oltre a specificare il valore ID figlio (o **CHILDID \_ SELF)** nel membro **lVal.**

Ad esempio, per ottenere il nome di un oggetto e non uno degli elementi figlio dell'oggetto, inizializzare [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) per il primo parametro di [**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) ( **CHILDID \_ SELF** nel membro **lVal** e **VT \_ I4** nel membro **vt)** e quindi chiamare **IAccessible::get \_ accName**.

## <a name="output-parameters"></a>Parametri di output

Diversi metodi e funzioni [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) hanno un parametro di output [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) che contiene un ID figlio o un puntatore a interfaccia \* [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) a un oggetto figlio. Esistono diversi passaggi che un client deve eseguire a seconda che ricevano un ID figlio **\_ VT I4** (elemento semplice) o un puntatore a interfaccia **IDispatch** con **CHILDID \_ SELF** (oggetto completo). Seguendo questi passaggi verranno forniti un puntatore di interfaccia **IAccessible** e un ID figlio che insieme consentono ai client di usare i metodi e le proprietà **IAccessible.** Questi passaggi si applicano ai [**metodi IAccessible::accHitTest,**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)e [**get \_ accSelection.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) Si applicano anche alle funzioni client [**AccessibleObjectFromEvent,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)e [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)

Nella tabella seguente sono elencati i possibili risultati restituiti e i passaggi di post-elaborazione necessari in modo che i client dia un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e un ID figlio.



| Risultato restituito                                      | Post-elaborazione per il valore restituito                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Puntatore a interfaccia IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) | Si tratta di un oggetto completo. Chiamare [**QueryInterface per**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) accedere al [**puntatore di interfaccia IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)<br/> Usare il [**puntatore di interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) **con CHILDID \_ SELF** per accedere ai metodi e alle proprietà **IAccessible.**<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| ID figlio \_ VT I4                                      | Chiamare [**IAccessible::get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) usando l'ID figlio per verificare se è disponibile un [**puntatore a interfaccia IDispatch.**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) Se si ottiene un [**puntatore a interfaccia IDispatch,**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) usarlo con **CHILDID \_ SELF** per accedere ai metodi e alle proprietà [**dell'interfaccia IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)<br/> Se la chiamata a [**get \_ accChild ha**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) esito negativo, si dispone di un elemento semplice. Usare il puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) originale (quello usato nella chiamata al metodo o alla funzione indicata in precedenza) con l'ID figlio **\_ I4 VT** restituito dalla chiamata.<br/> |



 

Prima di poter usare un [**parametro VARIANT,**](/windows/win32/api/oaidl/ns-oaidl-variant) è necessario inizializzarlo chiamando la funzione [**Component Object Model VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) (COM). Al termine della struttura , chiamare [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear) per liberare la memoria riservata per **tale VARIANT.**

## <a name="special-cases"></a>Casi speciali

Esistono eccezioni alle linee guida nella tabella precedente, ad esempio quando un ID figlio viene restituito dal [**metodo IAccessible::accHitTest.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) I server devono restituire [**un'interfaccia IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) se l'elemento figlio è un oggetto accessibile. Se un ID figlio viene restituito **da IAccessible::accHitTest,** l'elemento figlio è un elemento semplice.

Esistono anche casi speciali per [**accNavigate.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) Per altre informazioni, vedere **IAccessible::accNavigate** e [Navigazione spaziale e logica.](spatial-and-logical-navigation.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia IDispatch](idispatch-interface.md)
</dt> <dt>

[Struttura VARIANT](variant-structure.md)
</dt> </dl>

 

