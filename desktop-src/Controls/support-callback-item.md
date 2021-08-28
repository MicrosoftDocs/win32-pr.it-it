---
title: Come supportare gli elementi di callback
description: Questo argomento illustra come fornire supporto per gli elementi di callback.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df078b8be8cd02f56592a74de4242b515974a740df01d3cd4bd36074d5f8e022
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968221"
---
# <a name="how-to-support-callback-items"></a>Come supportare gli elementi di callback

Questo argomento illustra come fornire supporto per gli elementi di callback.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Se l'applicazione userà elementi di callback in un controllo ComboBoxEx, deve essere preparata per gestire il codice di notifica [ \_ GETDISPINFO CBEN.](cben-getdispinfo.md) Un controllo ComboBoxEx invia questa notifica ogni volta che il proprietario deve fornire informazioni specifiche sull'elemento. Per altre informazioni sugli elementi di callback, vedere [Elementi di callback](comboboxex-controls.md).

La funzione definita dall'applicazione seguente elabora [CBEN \_ GETDISPINFO](cben-getdispinfo.md) fornendo attributi per un determinato elemento. Si noti che imposta il **membro mask** della struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) in ingresso su CBEIF \_ DI \_ SETITEM. Se **si imposta mask** su questo valore, il controllo mantiene le informazioni sull'elemento in modo che non sia necessario richiedere nuovamente le informazioni.

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

[Informazioni di riferimento sul controllo ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Uso dei controlli ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 