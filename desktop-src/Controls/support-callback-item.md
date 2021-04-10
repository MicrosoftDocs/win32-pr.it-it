---
title: Come supportare gli elementi di callback
description: In questo argomento viene illustrato come fornire supporto per gli elementi di callback.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056f64c086aeda94ccf928d93ae2c5db5e2187a4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963570"
---
# <a name="how-to-support-callback-items"></a>Come supportare gli elementi di callback

In questo argomento viene illustrato come fornire supporto per gli elementi di callback.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Se l'applicazione userà gli elementi di callback in un controllo ComboBoxEx, è necessario prepararsi a gestire il codice di notifica [ \_ GETDISPINFO CBEN](cben-getdispinfo.md) . Un controllo ComboBoxEx Invia questa notifica ogni volta che è necessario che il proprietario fornisca informazioni specifiche sull'elemento. Per altre informazioni sugli elementi di callback, vedere [elementi callback](comboboxex-controls.md).

La funzione definita dall'applicazione seguente elabora [CBEN \_ GETDISPINFO](cben-getdispinfo.md) fornendo attributi per un determinato elemento. Si noti che imposta il membro **mask** della struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) in ingresso su CBEIF \_ di \_ elemento. Impostando **mask** su questo valore, il controllo mantiene le informazioni sull'elemento in modo che non sia necessario richiedere nuovamente le informazioni.

## <a name="complete-example"></a>Esempio completo


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Riferimento al controllo ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Uso di controlli ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 