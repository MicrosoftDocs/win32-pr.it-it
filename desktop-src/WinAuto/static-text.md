---
title: Testo statico (riferimento all'elemento dell'interfaccia utente MSAA)
description: I controlli di testo statici rappresentano un modo pratico per visualizzare il testo nelle finestre di dialogo e altre finestre. I controlli di testo statici spesso vengono usati come etichette per altri controlli.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f35581a9b305f28782d8faeac81105afb0d5147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856858"
---
# <a name="static-text-msaa-ui-element-reference"></a>Testo statico (riferimento all'elemento dell'interfaccia utente MSAA)

I controlli di testo statici rappresentano un modo pratico per visualizzare il testo nelle finestre di dialogo e altre finestre. I controlli di testo statici spesso vengono usati come etichette per altri controlli.

Il nome della classe della finestra per un controllo testo statico è "STATIC".

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli di testo statici supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli di testo statici supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La proprietà **childCount** è zero.                                                                                                                                                                                                                                                          |
| [**ottenere \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La proprietà **KeyboardShortcut** è la chiave di accesso, ovvero il carattere sottolineato nel testo che attiva il controllo associato al testo statico. La stringa restituita contiene il carattere di chiave di accesso aggiunto alla stringa "Alt +".                                           |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La proprietà **Name** corrisponde al testo nel controllo testo statico.                                                                                                                                                                                                                     |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.                                                                                   |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è [**\_ \_ STATICTEXT del sistema Role**](object-roles.md).                                                                                                                                                                                             |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: sistema di stato di sola [**\_ \_ lettura stato sistema di stato**](object-state-constants.md) \| [**\_ \_ invisibile**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Note

-   Il metodo [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) restituisce disp \_ E \_ MEMBERNOTFOUND quando viene chiamato con [**SELFLAG \_ TAKEFOCUS**](selflag.md) su un oggetto testo statico.
-   I controlli statici con lo \_ stile dell'icona SS restituiscono dati non validi nella proprietà **Name** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





